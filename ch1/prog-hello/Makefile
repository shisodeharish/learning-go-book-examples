
.PHONY: build run fmt vet clean

build:
	go build -o app main.go

run: build
	./app

fmt:
	go fmt .

vet:
	go vet .

clean:
	rm -f app
