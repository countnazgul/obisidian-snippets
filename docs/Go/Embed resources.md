### Description

This section is targeting mostly web apps (Svelte, React, Vue, static html pages etc). And it is a way to embed the web app into the Go binary itself.

The variable, that holds the folder content, is passed to http handler to be served by an http server.
### Code

Create the package file into the root folder of the frontend. The frontend should be located into a subfolder of the main Go project.

```go
package frontend

import (
    "embed"
    "io/fs"
    "net/http"
)

//go:generate npm i
//go:generate npm run build
//go:embed dist/*
var BuildFs embed.FS
// the few lines above will run "npm i", "npm run build" and will embed the content of "dist" folder into BuildFs variable

func BuildHTTPFS() http.FileSystem {
    build, err := fs.Sub(BuildFs, "dist")
    if err != nil {
        log.Fatal().Err(err).Msg(err.Error())
    }

    return http.FS(build)
}
```

### Usage

Once the `frontend` package is imported then we can call it and pass the output from it to a file server handler `http.FileServer`. This will serve the frontend content on `http://localhost:8080`.

Edit the `http.Handle` path to change the path where the static content is served.

```go
package main

import (
	"log"
	"net/http"
	
	"github.com/someone/some-repo/static" // "static" is the folder where the "frontent" package is located
)

func main() {
	fs := http.FileServer(frontend.BuildHTTPFS())

	http.Handle("/", fs)
	
	err := http.ListenAndServe(":8080", nil)
	if err != nil {
        log.Fatal(err)
    }
}
```