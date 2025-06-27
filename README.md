# Go Greetings

Repository for learning Go

Using Go Tutorial: [Create a Go Module](https://go.dev/doc/tutorial/create-module)

_Code changes omitted: Use git history to explore._

## Create a Go Module

```sh
mkdir greetings
cd greetings
go mod init github.com/tacoda/greetings
```

Add code to `greetings.go`

## Call your Code from Another Module

```sh
mkdir hello
go mod init github.com/tacoda/hello
go mod edit -replace github.com/tacoda/greetings=../greetings
go mod tidy
go run .
```

Add code to `hello.go` and run

## Return and Handle an Error

- Add code to `greetings.go`
- Add code to `hello.go` and run

```sh
cd hello
go run .
```
