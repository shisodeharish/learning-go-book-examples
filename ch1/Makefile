.DEFAULT_GOAL := build

.PHONY: fmt vet build clean run

fmt:
	go fmt ./...

vet: fmt
	go vet ./...

build: vet
	go build -o hello_world

run: build
	./hello_world

clean:
	go clean
	rm -f hello_world hello_world.exe
