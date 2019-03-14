---
title: "Creating an App"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 5
---

Hofstadter Studios enables you to create and deploy applications with ease.
Your development server is a real-time, cloud-native, hot-reloading, full-stack JS application
based on the [Apollo Universal Starter Kit](https://github.com/sysgears/apollo-universal-starter-kit).

#### Creating an Application

There are a number of starting applications available on GitHub.
A known list is maintained on [Studios Universe - Applications](/universe/applications).

To create a new application from the default, run:

```sh
hof app create "<app-name>"
```

You should see a response that indicates the app was created.

Now change to this directory.

```sh
cd "<app-name>"
```

##### Pushing and Deploying

Before you can use your application,
you will also need to push and deploy it.
We will do this in a couple of sections
after making some initial changes and updates.

#### Full Create Command

The create command can work off of a URL supporting git like
GitHub, GitLab, or Bitbucket.

```sh
hof app create "<name>" "<version>" "<template-url>"
```

example:

```sh
hof app create my-app beta "https://github.com/hofstadter-io/hof-starter-app"
```

- `name` is a kebab-style-name
- `version` is a Studios version
- `template-url` is a URL to a git repository

Studios versions can be found by running:

```sh
hof app versions
```

#### Custom and Private Repositories

The create command has a longer format enabling the use
any git based repository or the local filesystem.
See the [Studios Universe - Applications documentation](/universe/applications) for more information.

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.

