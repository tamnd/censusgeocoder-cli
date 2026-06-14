---
title: "Installation"
description: "Install geocoder from a release, with go install, or from source."
weight: 20
---

## Prebuilt binaries

Every [release](https://github.com/tamnd/censusgeocoder-cli/releases) carries archives for Linux, macOS,
and Windows on amd64 and arm64, plus deb, rpm, and apk packages for Linux.
Download, unpack, put `geocoder` on your `PATH`, done. The `checksums.txt`
on each release is signed with keyless [cosign](https://docs.sigstore.dev/) if
you want to verify before running.

## With Go

```bash
go install github.com/tamnd/censusgeocoder-cli/cmd/geocoder@latest
```

That puts `geocoder` in `$(go env GOPATH)/bin`, which is `~/go/bin` unless
you moved it. Make sure that directory is on your `PATH`.

## From source

```bash
git clone https://github.com/tamnd/censusgeocoder-cli
cd censusgeocoder-cli
make build        # produces ./bin/geocoder
./bin/geocoder version
```

## Container image

```bash
docker run --rm ghcr.io/tamnd/geocoder:latest --help
```

## Checking the install

```bash
geocoder version
```

prints the version and exits.
