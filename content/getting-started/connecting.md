---
title: "Connecting to Studios"
date: 2019-01-03T11:58:26-06:00
draft: false
type: "page"

weight: 4
---

The `hof` CLI requires a configuration file to
connect with the __Hofstadter Studios__ servers.

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