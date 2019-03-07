---
title: "Creating an App"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 5
---

Once you have an account and the __hof__ tool [installed](../installation/),
you can setup your local working copy.

#### Creating an Application

To create a new application:

```
hof app create <name> <version> <template-url>

hof app create my-app beta https://github.com/hofstadter-io/hof-starter-app
```

- `name` is a kebab-style-name
- `version` is a Studios version
- `template-url` is a URL to a git repository

Studios versions can be found by running:

```
hof app versions
```

#### Deploying your app to Studios

The `hof` CLI commands are run from your application directory.

```
hof app push
hof app deploy
```

The first deployment will take about 5 minutes.
You can check the status with:

```
hof app status
```

Once you see:

```
https://<app-name>.<username>.live.hofstadter.io
<username> <app-name>
Client:   running
Server:   running
System:   running
```

your application is running.

Now we can create some initial data with:

```
hof db seed
```

Once this is complete,
you can follow the link to use your app.


#### Community Starter Apps

Hofstadter Starter Apps:

- [hof-starter-app](https://github.com/hofstadter-io/hof-starter-app)
- [hof-starter-app-minimal](https://github.com/hofstadter-io/hof-starter-app-minimal)

Community Starter Apps:

- Be the first!

Make a Pull Request to have your starter app added here!

(there is a link at the bottom of this page)

