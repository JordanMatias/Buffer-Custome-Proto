## How to modify 

- Update protobuf file at proto/message.proto

- Generate grpc and interface type 

    `export PATH="$PATH:$(go env GOPATH)/bin"`

    `protoc --proto_path=./proto --go_out=./ --go-grpc_out=./  message.proto`

- Update module 

    `git tag v0.1.0`

    `git push origin v0.1.0`

    `GOPROXY=proxy.golang.org go list -m github.com/krushn/protobuf@v0.1.0`

    `go get github.com/krushn/protobuf@v0.1.0`

