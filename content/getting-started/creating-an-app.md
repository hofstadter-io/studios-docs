---
title: "Creating an App"
date: 2019-01-03T11:58:26-06:00
draft: false
type: "page"

weight: 5
---

Once you have an account and the __hof__ tool [installed](../installation/),
you can setup your local working copy.

#### Creating an Application

Applications are created through the
[Studios App Form](https://studios.studios.live.hofstadter.io/app/new).
Go there to create your app.

#### Clone the hof-starter-app

To get the initial version of your application clone the
[hof-starter-app](https://github.com/hofstadter-io/hof-starter-app).

```
git clone https://github.com/hofstadter-io/hof-starter-app app-name
cd app-name
```

You can also use any starter-app you or anyone else creates.

_there is a list of starting applications at the bottom of the page_

#### Updaing your app name

Look through all of the yaml files at the root of the directory.
Change all of the top-level name fields to the name you created your application with.

```yaml
app:
  name: "<app-name>"
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

you can follow the link to use your app.


#### Community Starter Apps

Hofstadter Starter Apps:

- [hof-starter-app](https://github.com/hofstadter-io/hof-starter-app)
- [hof-starter-app-minimal](https://github.com/hofstadter-io/hof-starter-app-minimal)

Community Starter Apps:

- Be the first!

Make a Pull Request to have your starter app added here!

(there is a link at the bottom of this page)

