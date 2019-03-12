### docopt.go
---
https://github.com/docopt/docopt.go

```go
package main

import (
  "fmt"
  "github.com/docopt/docopt-go"
)

func main() {
  usage := `Naval Fata.
  `
  
    arguments, _ := docopt.ParseDoc(usage)
    fmt.Println(arguments)
}

import "github.com/docopt/docopt-go"

docopt.ParseDoc(usage)

docopt.ParseArgs(usage, argv, "1.2.3")

parser := &docopt.Parser{
  HelpHandler: docopt.PrintHelpOnly,
  OptionsFirst: true,
}
opts, err := parser.ParseArgs(usage, argv, "")

flag, _ := opts.Bool("--flag")
secs, _ := opts.Int("<seconds>")

var config struct {
  Command string `docopt:"<cmd>"`
  Tries int `docopt:"-n"`
  Force bool
}
opts.Bind(&config)

```

```
go get github.com/docopt/docopt-go
```

```
```


