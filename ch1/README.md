# Chapter 1 – Setting Up Your Go Environment

This folder contains fully working examples and exercises from **Chapter 1** of the book *Learning Go* by Jon Bodner.

## 📘 What This Chapter Covers
✅ Installing Go  
✅ Writing your first Go program  
✅ Understanding `go mod`, `go build`, `go fmt`, `go vet`  
✅ Makefiles for automation  
✅ Using IDEs (VS Code / GoLand)  
✅ Running Go in the Playground

## 🧪 Program 1: `hello.go`
```bash
make run
```
Expected Output:
```
Hello, world!
```

## 🧪 Program 2: `hello_bad.go`
Deliberate formatting error to test `go vet`.

## 🧰 Makefile Commands
| Command     | Description                             |
|-------------|-----------------------------------------|
| `make fmt`  | Format code using `go fmt`              |
| `make vet`  | Check for subtle bugs using `go vet`    |
| `make build`| Compile program to native binary        |
| `make run`  | Build and run `hello.go`                |
| `make clean`| Clean compiled binaries                 |

## 💻 Go Playground
Run your code online at: [https://go.dev/play](https://go.dev/play)

## 📦 Output Binary
After `make build`, binary `hello_world` will be generated in this folder.

Run:
```bash
./hello_world
```

## 🧼 Clean Up
```bash
make clean
```
