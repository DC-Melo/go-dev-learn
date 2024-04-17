# go-dev-learn
go dev learn base on https://go.dev/learn/#tutorials

## Table of Contents

- [Installing Go](#installing-go)
- [Tutorial: Getting started](#tutorial-getting-started)
- [Tutorial: Create a module](#tutorial-create-a-module)
- [Tutorial: Getting started with multi-module workspaces](#tutorial-getting-started-with-multi-module-workspaces)
- [Tutorial: Developing a RESTful API with Go and Gin](#tutorial-developing-a-restful-api-with-go-and-gin)
- [Tutorial: Getting started with generics](#tutorial-getting-started-with-generics)
- [Tutorial: Getting started with fuzzing](#tutorial-getting-started-with-fuzzing)
- [Writing Web Applications](#writing-web-applications)
- [How to write Go code](#how-to-write-go-code)
- [A Tour of Go](#a-tour-of-go)


## Installing Go
Instructions for downloading and installing Go.

## Tutorial: Getting started
- Create a hello directory for your first Go source code. Tag: v0.01.1
For example, use the following commands:
```sh
❯ mkdir hello
❯ cd hello
❯ go mod init example/hello
go: creating new go.mod: module example/hello
```

- Paste the following code into your hello.go file. 

```
package main

import "fmt"

func main() {
    fmt.Println("Hello, World!")
}
```
- Run your code
```sh
$ go run .
Hello, World!
```

- Use the following command to get a list of the others:

```sh
$ go help
```
- Call code in an external package. Tag: v0.01.2
Change file name: hello.go

```go
package main

import "fmt"

import "rsc.io/quote"

func main() {
    fmt.Println(quote.Go())
}

```
- Add new module requirements and sums.

```sh
# When you ran go mod tidy, it located and downloaded the rsc.io/quote module that contains the package you imported
❯ go mod tidy
go: finding module for package rsc.io/quote
go: found rsc.io/quote in rsc.io/quote v1.5.2
# run the code 
❯ go run .
Don't communicate by sharing memory, share memory by communicating.
```





## Tutorial: Create a module
A tutorial of short topics introducing functions, error handling, arrays, maps, unit testing, and compiling.

## Tutorial: Getting started with multi-module workspaces
Introduces the basics of creating and using multi-module workspaces in Go. Multi-module workspaces are useful for making changes across multiple modules.

## Tutorial: Developing a RESTful API with Go and Gin
Introduces the basics of writing a RESTful web service API with Go and the Gin Web Framework.

## Tutorial: Getting started with generics
With generics, you can declare and use functions or types that are written to work with any of a set of types provided by calling code.

## Tutorial: Getting started with fuzzing
Fuzzing can generate inputs to your tests that can catch edge cases and security issues that you may have missed.

## Writing Web Applications
Building a simple web application.

## How to write Go code
This doc explains how to develop a simple set of Go packages inside a module, and it shows how to use the go command to build and test packages.

## A Tour of Go
An interactive introduction to Go in four sections. The first section covers basic syntax and data structures; the second discusses methods and interfaces; the third is about Generics; and the fourth introduces Go's concurrency primitives. Each section concludes with a few exercises so you can practice what you've learned. You can take the tour online or install it locally with:

$ go install golang.org/x/website/tour@latest

This will place the tour binary in your GOPATH's bin directory.

Effective Go
A document that gives tips for writing clear, idiomatic Go code. A must read for any new Go programmer. It augments the tour and the language specification, both of which should be read first.

Frequently Asked Questions (FAQ)
Answers to common questions about Go.

Editor plugins and IDEs
A document that summarizes commonly used editor plugins and IDEs with Go support.

Diagnostics
Summarizes tools and methodologies to diagnose problems in Go programs.

A Guide to the Go Garbage Collector
A document that describes how Go manages memory, and how to make the most of it.

Managing dependencies
When your code uses external packages, those packages (distributed as modules) become dependencies.

Fuzzing
Main documentation page for Go fuzzing.

Coverage for Go applications
Main documentation page for coverage testing of Go applications.

Profile-guided optimization
Main documentation page for profile-guided optimization (PGO) of Go applications.
