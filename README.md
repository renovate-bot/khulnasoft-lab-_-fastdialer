# Fastdialer

[![License](https://img.shields.io/github/license/khulnasoft-labs/fastdialer)](LICENSE.md)
![Go version](https://img.shields.io/github/go-mod/go-version/khulnasoft-labs/fastdialer?filename=go.mod)
[![Release](https://img.shields.io/github/release/khulnasoft-labs/fastdialer)](https://github.com/khulnasoft-labs/fastdialer/releases/)
[![Checks](https://github.com/khulnasoft-labs/fastdialer/actions/workflows/build-test.yml/badge.svg)](https://github.com/khulnasoft-labs/fastdialer/actions/workflows/build-test.yml)
[![GoDoc](https://pkg.go.dev/badge/khulnasoft-labs/fastdialer)](https://pkg.go.dev/github.com/khulnasoft-labs/fastdialer/fastdialer)


Fastdialer is implementation of `net.Dialer` with lot of features like DNS Cache , Dial History etc

# Features

- DNS Cache
- Dial History
- Supports Memory/Hybrid/Disk Cache.
- Supports Old/New TLS and x509 versions
- Supports Resolution Using Hosts File
- Cross Platform and more..

For more details and documentation refer [GoDoc](https://pkg.go.dev/github.com/khulnasoft-labs/fastdialer/fastdialer).


### ZTLS Fallback

fastdialer by default fallbacks to using zcrypto when there is an error in TLS handshake (insufficient security level etc ). This is done to support older TLS versions and ciphers. This can be disabled in fastdialer options or by using `DISABLE_ZTLS_FALLBACK=true` environment variable. when falling back to ztls, ChromeCiphers are used

# Example

An Example showing usage of fastdialer as a library is specified [here](./example/main.go)

```
cd example/
go run main.go
```

# License

fastdialer is distributed under MIT License
