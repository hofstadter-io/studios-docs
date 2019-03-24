---
title: "Deploying"
date: 2019-03-13
draft: false
type: "page"

weight: 8
---


Before you can use your applicate,
you must first deploy it.

#### Deploy your Application

The `hof` CLI commands are run from your application directory.

```sh
hof app push
hof app deploy
```

The first deployment will take about 5 minutes.
You can check the status with:

```sh
hof app status
```

Once you see:

```sh
https://<app-name>.<username>.live.hofstadter.io
<username> <app-name>
Client:   running
Server:   running
System:   running
```

your application is running.

Now we can migrate and seed the database with entries using:

```sh
hof db seed
```

Once this is complete,
you can follow the link
from `hof app status`
to use your app.

#### Shutdown an Application

To shutdown an application, run

```
hof app shutdown
```

You can later redeploy your application
and pick up where you left off,
with your data and configuration still in place.


#### Custom Deployments

__Private Hofstadter Studios__ can be deployed to any cloud or in your data center.
[Contact Sales to learn more](https://hofstadter.io/contact/).

