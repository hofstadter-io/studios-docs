---
title: "First Changes"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 8
---

The first steps will walk you through some
of the Hofstadter Studios basic concepts.

- [Changing the title](#changing-the-title)
- [Customizing the Home page](#customizing-the-home-page)

### Changing the title

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

Back in the terminal, run:

```
hof app push
```

Now, go back to your application in the browser
and watch as the page and title
automatically refresh with the latest updates!

_you can view the browser console to see some logs and progress_


### Customizing the Home page
