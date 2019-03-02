---
title: "Installing the Hof Tool"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 3
---

To work with __Hofstadter Studios__ you will need the __hof__ CLI tool.
__hof__ is available for all major operation systems
and architectures. Thank You Golang Developers and Community!

##### Precompiled Binaries

Download a precompiled binary from the github
[releases page](https://github.com/hofstadter-io/hof/releases).

##### Homebrew

```bash
brew install hofstadter-io/homebrew-tap/hof
```

##### Build from source

You can go get and compile the latest version with:

```bash
go get github.com/hofstadter-io/hof
```

Dependencies are vendored and committed to the repository
to ensure compatibility and simplicity.
You will also need your `GOPATH` and `$GOPATH/bin`
added to your `PATH`.

##### Test the installation

Run `hof help` to make sure the tool is available.

You can now configure the __hof__ tool to connect to the
__Hofstadter Studios__ system.

