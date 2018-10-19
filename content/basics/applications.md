---
title: "Applications"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 2
---

To work with Hofstadter Studios,
you have a local working directory
with a number of files and folders

```
project-dir/
  hof.yaml       # Config for connecting to Studios
  design/        # Main application design

  pages/         # for page content and layouts
  translations/  # and multilingual assets
  seeds/         # application seed data

  # not used yet
  secrets/       # for application secrets
  custom/        # for custom UI components
  funcs/         # for serverless functions
```

#### hof.yaml

The `hof.yaml` contains configuration
for the `hof` tool to talk to Hofstadter Studios.

```
app:
  name: "<app-name>

auth:
  username: "..."
  apikey: "..."

host: "https://<app-name>.live.hofstadter.io/studios"
```

#### design

The design folder is the main place
you will specify you application.
There are a number of files at the root
for describing you application, users,
layouts, pages, and configuration.

```
design/
  app.yaml
  meta.yaml
  config.yaml
  layout.yaml
  uaers.yaml
  pages.yaml
  modules.yaml

  modules/
    blog/
    todos/
    etc...
```

The modules folder is where you
describe the various modules
which make your application.
Each modules folder contains
its own configuration,
language files, and the
types that make up the module.

```
blog/
  module.yaml
  post.yaml
  comment.yaml
  tag.yaml

  pages/
    post/
      list/
        content.html
        style.scss
      view/
        content.html
        style.scss
      ...
  locales/
    en.json
    es.json
    ...
```

We'll get to the various file contents
in upcoming sections.


#### pages

The pages directory is where
you can create custom pages
(static at this point
with custom data feeds and syncs coming)

```
pages/
  home/
    home.html
    home.scss
    locales/
      en.json
      es.json
```

You will use these file locations
in the `pages.yaml` in your design folder,
so the naming and organization is flexible.


#### seeds

The seeds directory holds seed data for your application.
The main file here is the `users.json` file
used to define your initial users in the database.
Currently, this file cannot move.
If you change the user profile fields,
you can then add the new fields to this file.

For your modules, you can place your seeds
in the seed file, or place them in the modules
directory, as the location is configurable.

#### translations

The translations directory is similar in nature to the seeds directory,
and is for internationalization, or __i18n__.

### other

The other directories are not used at the moment,
and will be describes as they are incorporated
into Hofstadter Studios.

