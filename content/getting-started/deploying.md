---
title: "Deploying"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 8
---


#### Deploying your app to Studios

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

Now we can create some initial data with:

```sh
hof db seed
```

Once this is complete,
you can follow the link to use your app.


#### Custom Deployments

__Private Hofstadter Studios__ can be deployed to any cloud or in your data center.
[Contact Sales to learn more](https://hofstadter.io/contact/).

