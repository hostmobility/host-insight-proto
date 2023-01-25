# Protobuf definitions for Host Insight

This repository is meant to be used as a git submodule in projects
that depend on the Host Insight protocol which makes use of gRPC.

## Usage

There is no requirement to use Rust since multiple languages are
supported. Usage and compilation will vary depending on the language
used. See https://grpc.io/ for more details.

To add this repository as a submodule to an existing project:

```
git submodule add git@gitlab.com:hostmobility/ada/proto.git
```

This will automatically pull the main branch. If you pull a repository
dependent on this submodule you need to init the submodule and pull
the latest version.

```
git submodule update --init --recursive
```
