# Proto

Protobuf definition for gRPC

## Usage

This repository is meant to be used as a git submodlue in projects that needs to use Ada specific protobufs and gRPCs.
There is no specific limitation to use rust since multiple languages are supported. Usage and compilation will vary depending on language used refer to https://grpc.io/ for additional information.

To add this repository as a submodule to an existing project:

````
git submodule add git@gitlab.com:hostmobility/ada/proto.git
````
This will automatically pull the main branch. If you pull a repository dependent on this submodule you need to init the submodule and pull the latest version.

````
git submodule update --init --recursive
````

## Roadmap
- Figure out how to pass metadata from units. With rpc or as added data on packages?
-  Define some remote SW update flow that can be used by the server to verify that SW update was successful
- Check if protobuf files should be divided by functionality instead of by project to avoid duplication. e.g. a SWUpdate.proto file could be used by many different projects and or functionalities. This would allow projects to include functionality rather than a project specific proto file. This would also allow the server to implement functionality rather than projects. e.g. our server now supports the elevator.proto which consists of GPS, Digital values and SW update. A server implementation could be instead that it supports Digital values, GPS and SW updates. Then the elevator project should be dependent on a server that supports digital gps and sw update. Meaning any other project can reuse needed functionality e.g. An escalator  project that only needs Digital and SW update would only include these proto files and the server would already support it. For this to work smoothly meta data would be needed in some form identifying units to project.