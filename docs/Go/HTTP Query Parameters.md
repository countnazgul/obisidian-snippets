## Description

How to add http query parameters that will be correctly URI encoded
## Code

```go
baseUrl := "https://my-server.com"

// encoded will hold all query parameters
encoded := url.Values{}
encoded.Set("queryParam1", "param value goes here")
encoded.Set("someOtherParameter", "(another thing)")

req, err := http.NewRequest(
	"GET", 
	fmt.Sprintf("%s?%s", baseUrl, encoded.Encode()),
	http.NoBody,
)
if err != nil {
	log.Fatal()
}
```
