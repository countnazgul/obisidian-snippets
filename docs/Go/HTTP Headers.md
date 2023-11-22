## Description

How to add http headers on the server side when making http requests
## Code

```go
req, err := http.NewRequest("GET", "some-url.com", http.NoBody)
if err != nil {
	log.Fatal()
}

// add as many headers as we need in the following format:
req.Header.Add("HeaderKey", "header-value")
```