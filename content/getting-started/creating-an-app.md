---
title: "Creating an App"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 5
---

Hofstadter Studios enables you to create and deploy applications with ease.
The development version is a real-time, hot-reloading, full-stack JS application
based on the [Apollo Universal Starter Kit](https://github.com/sysgears/apollo-universal-starter-kit).


#### Creating an Application

There are a number of starting applications available on GitHub.
A known list is maintained on [Studios Universe - Applications](/universe/applications).

To create a new application from the default, run:

```
hof app create <name>
```

You should see a response that indicates the app was created.

Now change to this directory.

```
cd <app-name>
```

#### Pushing and Deploying

The first time you create an application,
you will also need to push and deploy it.
You can do that now, or wait a
[couple of sections](../deploying).

#### Full Create Command

The create command can work off of a URL supporting git like
GitHub, GitLab, or Bitbucket.

```
hof app create <name> <version> <template-url>
```

example:

```
hof app create my-app beta https://github.com/hofstadter-io/hof-starter-app
```

- `name` is a kebab-style-name
- `version` is a Studios version
- `template-url` is a URL to a git repository

Studios versions can be found by running:

```
hof app versions
```

##### Private Repositories

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.

