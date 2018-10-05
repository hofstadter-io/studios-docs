---
title: "db"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 2
---

These commands give you control over the
database backing your application.
For now, migrate does not work as expected.
Instead run `hof db reset` when you change the shape of data,
and `hof db seed` when you are only changing the seed data.

```
Work with your Studios DB

Usage:
  hof db [command]

Available Commands:
  migrate     Migrates the DB
  reset       Reset the DB to the latest schema
  seed        Reseed the DB
  status      Get the status of your DB

Flags:
  -h, --help   help for db

Use "hof db [command] --help" for more information about a command.
```


