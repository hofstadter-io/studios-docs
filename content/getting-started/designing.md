---
title: "Designing"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 6
---

The first steps will walk you through some
of the Hofstadter Studios basic concepts.

- [Overview](#overview)
- [Changing the Title](#changing-the-title)
- [Customizing the Home page](#customizing-the-home-page)
- [Creating New Functionality](#creating-new-functionaliity)
  - [Creating a Module](#creating-a-module)
  - [Creating a Type](#creating-a-type)
  - [Custom Page](#custom-page)
  - [Custom Component](#custom-component)

### Overview

At the root of your application,
you will see a very important
directory named `design`.
This is the "design" of your application.
You will see a number of files here,
for configuring the app features,
as well as a `modules` directory,
where your modules will go.

The directory overview:

```sh
app-dir/
  design/        # Main application design
  design-vendor/ # Imported modules' design

  pages/         # for page content and layouts
  translations/  # and multilingual assets
  seeds/         # application seed data
  custom/        # for custom UI components

  # secrets are not uploaded with a push
  # these are handled differently
  secrets/       # for application secrets

  # used seperately, coming soon
  funcs/         # for serverless functions
```


### Designs

Design represent the state you wish your application to be in.
They are data files written in specific formats, called DSLs.
While the examples are in yaml, you can intermix json, xml, toml, and hof-lang as well.
[Documentation for Designs](/reference/designs) are found in the reference section of these docs.

The layout for design (and design-vendor) is as follows:

```sh
design/
  app.yaml         # and other files...
  modules/
    account/       # ...same as blog...
    blog/
      module.yaml
      type.yaml    # per type files...
      pages/
      componets/
      locales/
      seeds/
```

You will find design files, html, css, jsx componets, translation files and seed data.

There are many 

We will start by making our own updates to the app, modules, types, pages, and components.

### Changing the Title

The first thing you may want to do is
change the Title of your application.
You can do this by editing:

__design/app.yaml__ and changing the "title" field.

```yaml
app:
  name: my-app
  title: "My Studios App"
```

### Customizing the Home Page

Let's change the home page to
greet the user if logged in.

##### Update the design

You can find the design in __design/pages.yaml__

```yaml
app:
  name: my-app

  pages:

    - name: home
      route: "/"
      style:
        - "pages/home/home.scss"
      content:
        - "pages/home/home.html"
      translations:
        - name: en
          file: pages/home/locales/en.json
        - name: es
          file: pages/home/locales/es.json
```
Add the following
```yaml
      current-user: true
```

##### Update the content

and the content in __pages/home/content.html__

```jsx
<div id="home-content">

<h1>{ t('title') }</h1>

<p>{ t('messages.hello') } from Hof Starter App</p>

</div>
```

##### What we did

In a few lines,
we injected the current user into
the home page and created a personalize geeting.
You can also inject other data related to the user
or create reusable components the same way.

What we didn't do was create a user,
setup an auth system or database,
or link it to the front end.
__Hofstadter Studios__ handles all that for you.

You can focus on your application.
Start with modules and types,
create pages and components,
declare the data and rules,
design the layout and styling.


### Creating New Functionality

You can create five main objects in __Studios__:

- modules - collections of types, pages, and components.
- types - the objects in your system

##### Creating a Module

```sh
hof new module "design/modules/<module-name>"
```

##### Creating a Type

```sh
hof new type "design/modules/<module-name>/<type-name>"
```

##### Custom Page

App page:

```sh
hof new module "design/<page-name>"
```

Module page:

```sh
hof new module "design/modules/<module-name>/<page-name>"
```

Type page:

```sh
hof new module "design/modules/<module-name>/<type-name>/<page-name>"
```

##### Custom Component

App component:

```sh
hof new component "design/<component-name>"
```

Module component:

```sh
hof new component "design/modules/<module-name>/<component-name>"
```

Type component:

```sh
hof new component "design/modules/<module-name>/<type-name>/<component-name>"
```

##### Custom Logic

Serverless functions as well as built-in hooks, handlers and, integrations.

```sh
hof new func "<name>" "<template>"
hof func create "<name>" "<runtime>"
hof func "<command>" "<name>"
```

coming soon!


##### Custom and Private Repositories

The new command has a longer format enabling the use
any git based repository or the local filesystem.
See the [Studios Universe - Templates](/universe/templates) documentation for more information.

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.



