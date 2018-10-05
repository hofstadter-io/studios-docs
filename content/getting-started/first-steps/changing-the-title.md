---
title: "1. Changing the Title"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1
---

The first thing we will do is to change the title of your application.
This will demonstrate editing a design file and pushing the updates
to your Hofstadter Studios Live server.

In your favorite text editor,
open the `design/app.yaml` file
(It may also be the `design/config.yaml`).

You will see somthing like:

```
app:
  ...
  title: "Hof Starter App"
  ...
```

Change the title string to anything you want
and save the file.

Now, back in the terminal, run:

```
hof push
```

You should see a list of files that get uploaded.
(This is currently everything, but we're working on making it minimal :)

Now, go back to your application in the browser at
https://your-app-name.live.hofstater.io
and watch as the page and title
automatically refresh with the latest updates!

