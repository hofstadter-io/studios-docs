---
title: "Installing the Hof Tool"
date: 2019-01-03T11:58:26-06:00
draft: false
type: "page"

weight: 3
---

To work with __Hofstadter Studios__ you will need the __hof__ tool.
__hof__ is available for all major operation systems
and architectures. Thank You Golang Developers and Community!

##### Precompiled Binaries

Download a precompiled binary__hof__ from the github
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

#### Connecting to Studios

The `hof` CLI requires a configuration file to
connect with the Studios server.

```
hof config set-context <context-name> <username> <apikey> https://studios.studios.live.hofstadter.io
```

- `context-name` can be anything
- `username` is your username
- `apikey` can be found in your [profile](https://studios.studios.live.hofstadter.io/profile)


You can verify your configuration with:

```
hof config view all
hof app status
```

_The second command will fail. Go to the next step to create and deploy your first application_
