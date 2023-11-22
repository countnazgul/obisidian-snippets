## Description

Sometimes there is a need to generate self-signed certificates. For example to be used with https server

## Code

```go
func generateCertificates(commonName string) ([]byte, []byte, []byte, error) {

    bits := 4096
    privateKey, err := rsa.GenerateKey(rand.Reader, bits)
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "rsa.GenerateKey")
    }

    tpl := x509.Certificate{
        SerialNumber:          big.NewInt(1),
        Subject:               pkix.Name{CommonName: commonName},
        NotBefore:             time.Now(),
        NotAfter:              time.Now().AddDate(10, 0, 0),
        BasicConstraintsValid: true,
        ExtKeyUsage: []x509.ExtKeyUsage{
            x509.ExtKeyUsageClientAuth,
            x509.ExtKeyUsageServerAuth,
        },
        KeyUsage: x509.KeyUsageDigitalSignature | x509.KeyUsageCertSign,
    }

    derCert, err := x509.CreateCertificate(
        rand.Reader,
        &tpl,
        &tpl,
        &privateKey.PublicKey,
        privateKey,
    )
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "x509.CreateCertificate")
    }
  
    buf := &bytes.Buffer{}
    err = pem.Encode(buf, &pem.Block{
        Type:  "CERTIFICATE",
        Bytes: derCert,
    })
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "pem.Encode")
    }

    pemCert := buf.Bytes()
    buf = &bytes.Buffer{}
    err = pem.Encode(buf, &pem.Block{
        Type:  "RSA PRIVATE KEY",
        Bytes: x509.MarshalPKCS1PrivateKey(privateKey),
    })
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "pem.Encode")
    }
    pemKey := buf.Bytes()

    cert, err := x509.ParseCertificate(derCert)
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "x509.ParseCertificate")
    }

    pubDER, err := x509.MarshalPKIXPublicKey(cert.PublicKey.(*rsa.PublicKey))
    if err != nil {
        return nil, nil, nil, errors.Wrap(err, "x509.MarshalPKIXPublicKey")
    }

    sum := sha256.Sum256(pubDER)
    pin := make([]byte, base64.StdEncoding.EncodedLen(len(sum)))
    base64.StdEncoding.Encode(pin, sum[:])
  
    return pemCert, pemKey, pin, nil
}
```

## Usage

Once the function is called it will return the `byte` values for the certificate, key and pin. Certificate and the certificate key then can be used and stored as `pem` files:

```go
    cert, key, pin, err := generateCertificates("something")
    if err != nil {
        log.Fatal(err)
    }

    os.WriteFile("/cert.pem", cert, 0644)
    os.WriteFile("./cert_key.pem", key, 0644)
    fmt.Println(string(pin))
```