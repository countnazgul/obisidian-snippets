### Description

How to use certificates to create HTTPS web server

### Code

NOTE: We can use the code from [[Generate self-signed pem certificates]] to generate local, self-signed certificates.

```go
package main

import (
	"log"
	"net/http"
	"os"
	"fmt"
)

func hello(w http.ResponseWriter, req *http.Request) {
	fmt.Fprintf(w, "Hello World!\n")
}

func main() {
	cert, err := os.ReadFile("/path/to/cert.pem")
    if err != nil {
        log.Fatal(err)
    }	

	key, err := os.ReadFile("/path/to/cert_key.pem")
    if err != nil {
        log.Fatal(err)
    }
    
	http.HandleFunc("/hello", hello)

    err = http.ListenAndServeTLS(":8080", string(cert), string(key), nil)
    if err != nil {
        log.Fatal(err)
    }
}
```

Once the above code is ran we will be able to visit `https://localhost:8080/hello` and will get `Hello World!` as a response.

NOTE: If using self-signed (or not trusted) certificates then the browser will "complain" about it and we'll have to press couple of buttons to continue browsing.
