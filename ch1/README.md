# 📘 Chapter 1: Setting Up Your Go Environment

Welcome to Chapter 1 of my Go learning journey! This chapter focuses on setting up the Go development environment and understanding the essential CLI tools, formatting, and build workflows.

---

## ✅ What You'll Learn

- How to install and verify Go on any OS
- Understanding Go’s CLI tooling (`go build`, `go run`, `go fmt`, `go vet`)
- Writing and running your first Go application
- Using a `Makefile` for automation
- Recommended IDEs and Go Playground
- Installing tools like Chocolatey and Make on Windows
- Go Compatibility Promise and upgrade practices

---

## 🛠 Setup Instructions

### 🔗 Official Installation (Recommended)
Install Go from the official source:  
➡️ [https://go.dev/dl](https://go.dev/dl)

#### For Linux:
```bash
sudo tar -C /usr/local -xzf go1.20.5.linux-amd64.tar.gz
export PATH=$PATH:/usr/local/go/bin
```

#### For Windows:
- Use the `.msi` installer or Chocolatey:
```powershell
choco install golang
```

#### Verify Installation:
```bash
go version
```

---

## 🧪 Go Toolchain Essentials

| Tool      | Description                                      |
|-----------|--------------------------------------------------|
| `go build` | Compiles code to binary                         |
| `go run`  | Compiles + runs in one step                      |
| `go fmt`  | Formats code using Go standards                  |
| `go vet`  | Finds suspicious or buggy code patterns          |
| `go mod`  | Manages dependencies in Go modules               |

---

## 👋 First Go Program

### 📁 Folder Setup
```bash
mkdir ch1 && cd ch1
go mod init hello_world
```

### ✍️ `hello.go`
```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, world!")
}
```

---

## 🔧 Build and Run

```bash
go build
./hello_world
```

Or using `go run`:
```bash
go run hello.go
```

---

## 🧹 Code Formatting and Validation

### Format code:
```bash
go fmt ./...
```

### Validate code:
```bash
go vet ./...
```

Example:
```go
fmt.Printf("Hello, %s!\n", "world") // ✅ Correct
```

---

## ⚙ Makefile for Automation

```make
.DEFAULT_GOAL := build
.PHONY: fmt vet build clean

fmt:
	go fmt ./...

vet: fmt
	go vet ./...

build: vet
	go build -o hello_world

clean:
	rm -f hello_world
```

### 🧪 Run:
```bash
make         # Runs fmt → vet → build
make clean   # Deletes binary
```

---

## 💡 Development Tools

| Tool       | Description                                      |
|------------|--------------------------------------------------|
| **VS Code** | Free, lightweight. Use with Go extension         |
| **GoLand**  | JetBrains IDE (paid, but robust)                 |
| **Go Playground** | Browser-based Go runner: [go.dev/play](https://go.dev/play) |

---

## 🔄 Go Compatibility Promise

- No breaking changes across Go 1.x versions
- New versions improve tools, performance, and debugging
- Safely upgrade using `.tar.gz`, Chocolatey, or Homebrew

---

## 🧠 Must-Do Exercises

1. Run `hello.go` in [Go Playground](https://go.dev/play)
2. Add a `clean` target in the `Makefile`
3. Deliberately break formatting and test `go fmt`
4. Introduce a `vet` warning and fix it

---

## 🎯 Wrap-Up

- Go builds native binaries—no VM needed.
- Use `go fmt` and `go vet` before every build.
- Use `Makefile` to automate toolchain commands.
- Prefer official installation methods for stability.
- Chocolatey helps Windows users install `make`, `go`, and other tools efficiently.

---

🧠 _“Simplicity is the soul of Go — this chapter proves it.”_
