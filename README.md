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
- Add code to `hello.go`

```sh
cd hello
go run .
```

## Return a Random Greeting

- Add code to `greetings.go`
- Add code to `hello.go`

```sh
cd hello
go run .
go run .
go run .
```

## Return Greetings for Multiple People

- Add code to `greetings.go`
- Add code to `hello.go`

```sh
cd hello
go run .
```

## Add a Test

- Add a `greetings_test.go` file

```sh
cd greetings
go test
go test -v
```

## Compile and Install the Application

```sh
cd hello
go build
./hello

go list -f '{{.Target}}'

export PATH=$PATH:/path/to/your/install/directory
# OR
go env -w GOBIN=/path/to/your/bin

go install
hello
```
