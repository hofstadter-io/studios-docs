---
title: "Getting Started"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1
---

## Installation

`geb` is available for all major operation systems
and architectures. Thank You Golang Developers and Community!

##### Precompiled Binaries

Download a precompiled binary`geb` from the github
[releases page](https://github.com/hofstadter-io/geb/releases).

##### Homebrew

```bash
brew install hofstadter-io/homebrew-tap/geb
```

##### Build from source

You can go get and compile the latest version with:

```bash
go get github.com/hofstadter-io/geb
```

## geb Commands

The `geb` tool has many commands available,
with `geb gen` being the main, project oriented command.
There is a built in help system and running `geb` without
arguments will output the following:

```
Usage:
  geb [command]

Available Commands:
  add         Add a design, dsl, or generator to a project.
  adhoc       Generate something from data and a template.
  gen         Generate a project.
  help        Help about any command
  new         Create new stuff.
  run         Run a run-config pipeline for a project.
  system      Manage the geb system and congiuration
  view        View information known to the geb tool.

Flags:
  -h, --help   help for geb

Use "geb [command] --help" for more information about a command.
```

The `geb` command is created with to the awesome [Spf13 Cobra Project](https://github.com/spf13/cobra).

## Where to go next

[A First Example](./first-example) will introduce you to the
`design + template = anything` concept through the `geb adhoc` command.

[A First Project](./first-project) will introduce you to the
`geb gen` command and show you around the workflow of projects, designs, implementation, and (re)generation.

[A First DSL](./first-dsl) will expand on the first project
and introduce you to writing your own DSLs and generators.

Obviously, there is a ton of content in the navigation menu.
[Awesome Geb](./awesome-geb) has categories and links to all things `geb` related too!


