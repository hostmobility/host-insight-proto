# HOST Insight Proto

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

# Copying

HOST Insight Proto is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
(at your option) any later version.

HOST Insight Proto is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software Foundation,
Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301  USA
