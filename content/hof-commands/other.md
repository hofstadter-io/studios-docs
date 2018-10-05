---
title: "other & upcoming"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 10
---


#### Early Adopter commands

There is a hidden `dsl` command
for making capability updates much faster.
In the future this will go away,
once things become more stable.
These mirror the app version and update commands,
but only work on the DSL version without updating
the live servers.

```
Work with your Studios DSL version

Usage:
  hof dsl [command]

Available Commands:
  set         Sets the DSL version for your Application
  version     Gets the DSL version for your Application

Flags:
  -h, --help   help for dsl

Use "hof dsl [command] --help" for more information about a command.
```

#### validate

This will be the next command we work on.
It's purpose will be to validate your
designs and other pieces while changing things locally.
It will always be called by `hof push` before
actually sending the updates.

