# hbench releases

hbench is a single-binary benchmark runner for coding-agent harnesses: it runs tasks in Docker, drives 40+ agents,
grades them with the tasks' own tests, and reports rewards, tokens and cost. This repository carries the release
binaries for [Harness Playground](https://nodeq.tech) participants; it holds no source.

## Install

Linux or macOS, x86_64 or arm64:

```sh
curl -fsSL https://nodeq.tech/install.sh | sh
```

The script installs the hbench version the arenas pin into `~/.local/bin` and checks it against the release's
`SHA256SUMS`. Set `HBENCH_VERSION=vX.Y.Z` to install another release, or `HBENCH_INSTALL_DIR` to put it somewhere
else. You also need Docker.

## Verify a download by hand

Download the archive for your platform and `SHA256SUMS` from the same release, then:

```sh
grep " hbench-v0.2.2-aarch64-apple-darwin.tar.gz$" SHA256SUMS | shasum -a 256 -c -   # macOS
grep " hbench-v0.2.2-x86_64-unknown-linux-musl.tar.gz$" SHA256SUMS | sha256sum -c -  # Linux
```

## Licence

The binaries are distributed under the Apache License 2.0; see [LICENSE](LICENSE) and [NOTICE](NOTICE).
