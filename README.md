# test-go-wasm

## Installing wasmtime

[Installing wasmtime](https://docs.wasmtime.dev/cli-install.html#installing-wasmtime)

### Windows

```shell
scoop install wasmtime
```

### MacOS

```shell
brew install wasmtime
```

## Compile

### Linux

```shell
GOOS=wasip1 GOARCH=wasm go build -o main.wasm main.go
```

### Windows

```shell
SET CGO_ENABLED=0 ;`
SET GOOS=wasip1 ;`
SET GOARCH=wasm ;`
go build -o main.wasm main.go
```
go version
## Run

```shell
wasmtime main.wasm --default-encoding=utf-8
```
