# echo-logrus
[![Build Status](https://travis-ci.org/neko-neko/echo-logrus.svg?branch=master)](https://travis-ci.org/neko-neko/echo-logrus)
[![Go Report Card](https://goreportcard.com/badge/github.com/neko-neko/echo-logrus)](https://goreportcard.com/report/github.com/neko-neko/echo-logrus)
[![License](http://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/neko-neko/echo-logrus/master/LICENSE)

## Overview
Middleware echo-logger is a [logrus](https://github.com/sirupsen/logrus) logger support for [Echo](https://github.com/labstack/echo).  
This middleware is working on Echo v4.

## Getting Started
### For [dep](https://github.com/golang/dep) users
When your project top dir run this.  
```bash
$ dep ensure -add github.com/mudphilo/echo-logger
```

### Modules users
```bash
$ go get github.com/mudphilo/echo-logger
```

## Example
```go
package main

import (
	"os"
	"time"

	"github.com/labstack/echo/v4"
	echoLogger "github.com/mudphilo/echo-logger"
)

func main() {
	e := echo.New()

	// enable logging
	e.Use(echoLogger.Logger())

	e.Logger.Fatal(e.Start(":1323"))
}
```
