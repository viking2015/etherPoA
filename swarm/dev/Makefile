.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/Exgibichi/go-etf/cmd/swarm
	go build -o bin/geth     github.com/Exgibichi/go-etf/cmd/geth
	go build -o bin/bootnode github.com/Exgibichi/go-etf/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/Exgibichi/go-etf/swarm/...
