# Chillis & Associates chillisd Repository
This repository contains the source code for validators on the Chillis network. The source is based on the wasmd variant of the Cosmos-SDK, which includes a virtual machine that compiles to WebAssembly. It contains Chillis&Associates-specific updates required for the test networks and future mainnet, including a decentralized random beacon (DRB) and a novel, compact multi-signatures scheme. Versions of this repository are not currently syncrhonised with either wasmd or the Cosmos-SDK. Please refer to the releases section for the compatiblity with upstream versions.

Note: Requires Go 1.16+

Supported Systems
The supported systems are limited by the dlls created in go-cosmwasm. In particular, we only support MacOS and Linux. For linux, the default is to build for glibc, and we cross-compile with CentOS 7 to provide backwards compatibility for glibc 2.12+. This includes all known supported distributions using glibc (CentOS 7 uses 2.12, obsolete Debian Jessy uses 2.19).

As of 0.5.x we support muslc Linux systems, in particular Alpine linux, which is popular in docker distributions. Note that we do not store the static muslc build in the repo, so you must compile this yourself, and pass -tags muslc. Please look at the Dockerfile for an example of how we build a static Go binary for muslc. (Or just use this Dockerfile for your production setup).
