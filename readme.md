## How to modify 

- Update protobuf file at proto/message.proto

- Generate grpc and interface type 

    `export PATH="$PATH:$(go env GOPATH)/bin"`

    `protoc --proto_path=./proto --go_out=./ --go-grpc_out=./  message.proto`


