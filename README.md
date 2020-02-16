# go-ipfs-stack - a mono repo for working on go-ipfs

To get started, clone this repo and initialize its submodules

```
git submodule update --init --recursive
```

You will need a go compiler. I used go1.13 to do this work. See the output of `go env` below
```
GO111MODULE=""
GOARCH="amd64"
GOBIN=""
GOCACHE="${HOME}/Library/Caches/go-build"
GOENV="${HOME}/Library/Application Support/go/env"
GOEXE=""
GOFLAGS=""
GOHOSTARCH="amd64"
GOHOSTOS="darwin"
GONOPROXY=""
GONOSUMDB=""
GOOS="darwin"
GOPATH="${HOME}/go"
GOPRIVATE=""
GOPROXY="https://proxy.golang.org,direct"
GOROOT="/usr/local/Cellar/go/1.13.6/libexec"
GOSUMDB="sum.golang.org"
GOTMPDIR=""
GOTOOLDIR="/usr/local/Cellar/go/1.13.6/libexec/pkg/tool/darwin_amd64"
GCCGO="gccgo"
AR="ar"
CC="clang"
CXX="clang++"
CGO_ENABLED="1"
GOMOD="${HOME}/GUN/fissioncodes/go-ipfs/go.mod"
CGO_CFLAGS="-g -O2"
CGO_CPPFLAGS=""
CGO_CXXFLAGS="-g -O2"
CGO_FFLAGS="-g -O2"
CGO_LDFLAGS="-g -O2"
PKG_CONFIG="pkg-config"
GOGCCFLAGS="-fPIC -m64 -pthread -fno-caret-diagnostics -Qunused-arguments -fmessage-length=0 -fdebug-prefix-map=/var/folders/w6/lzdcttwd7tdctw0bv31xy5x00000gn/T/go-build707216868=/tmp/go-build -gno-record-gcc-switches -fno-common"

```

To make a build, cd into go-ipfs and run `make build`. The main repo, go-ipfs, should have a
 `replace` directives with relative paths to the go-ipfs-cmds and go-ipfs-files packages.


# How do I know if I'm building against the right package?
You can use to the go list tool to see which packages are being used in your build.

```
go list -json all | less
```

