---
title: "Configuration"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 2
---


Applications have a set of top-level configuration.
Here we will see the basic ones.
You can find more details in the advanced and reference sections.

While the following files can be just one file,
we have split them into several files.
Notice that they all start with:

```
app:
  name: "hof-starter-app"
```

where "__name__" will match your applications own name.
"__name__" is an important reference point in Hofstadter Studios,
enabling you to spread your designs across files and directories
to keep things organized and managebale.

Also, file names are not important, however their location
and contents will be. More on this at the end of the "basics" section.

### app.yaml

This file holds the name, title, and version of your application.

```
app:
  name: "hof-starter-app"
  title: "Hof Starter App"
  version: "0.0.1"
```

### meta.yaml

This file contains meta information about your application.

```
app:
  name: "hof-starter-app"

  author: "Hofstadter <support@hofstadter.io>"
  license: "BSD 3-Clause"

  homepage: "https://hof-starter-app.live.hofstadter.io"

  keywords:
    - "Hofstadter"
    - "Studios"
    - "HofStarterApp"
    - "hof-starter-app"
```

### config.yaml

This file contains configuration for your application.
There is related information in the secrets folder
for holding the sensative information and keys.

```
app:
  name: "hof-starter-app"

  mode: live

  config:
    gaTracking: "UA-000000-23"

    oauth:
      google: true
      facebook: true
      linkedin: false
      github: false

    mailer:
      provider: mailgun
      sender: "support@hofstadter.io"

    multilang:
      picker: true
      languages:
        - short: en
          code: en-US
        - short: es
          code: es-ES
```

_mode will eventuall disappear_
