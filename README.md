# ecflow-proto

Protobuf for ecflow gRPC client using by:

- perillaroc/ecflow-client-cpp
- perillaroc/ecflow-client-go

# Building

## c++

```bash
mkdir -p build/cpp
cd build/cpp
protoc -I ../../ --grpc_out=. --plugin=protoc-gen-grpc=`which grpc_cpp_plugin` ../../ecflow_client.proto
protoc -I ../../ --cpp_out=. ../../ecflow_client.proto
```

## go

```bash
mkdir -p build/go
cd build/go
protoc -I ../../ ../../ecflow_client.proto --go_out=plugins=grpc:.
```

## python

```bash
mkdir -p build/python
cd build/python
python -m grpc_tools.protoc -I ../../ ../../ecflow_client.proto --python_out=. --grpc_python_out=.
```

# LICENSE

Copyright &copy; 2019-2020, Perilla Roc.

`ecflow-proto` is licensed under [the MIT License](./LICENSE)