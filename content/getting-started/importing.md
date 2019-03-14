---
title: "Importing"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 7
---

You can import modules from any Git repository like GitHub, GitLab, or Bitbucket.
These are preconfigured __Studios__ bundles which contain:
modules, types, pages, components, and translations.

Modules can be used to quickly expand
your application functionality.

A module list and usage instructions can be found at:
[Studios Universe - Modules](/universe/modules).

- [Import a Module](#import-a-module)
  - [Import command](#import-command)
  - [Enable in the App](#enable-in-the-app)
  - [Create a Menu Entry](#create-a-menu-entry)
- [Module Overview](#module-overview)
- [Extending and Overriding](#extending-and-overriding)
  - [Extending the Design](#extending-the-design)
  - [Overriding a Page](#overriding-a-page)
  - [Updating the Application](#updating-the-application)
- [Custom and Private Repositories](#custom-and-private-repositories)


#### Import a Module

The `simple-blog` has
types, pages, and components for
posts, comments, and tags.
This module shows many of the configurable
options within the designs.

##### Import command

```sh
hof import "#simple-blog"
```

Pulls the latest `studios-modules` and
imports designs from the `simple-blog` folder.

The full import command is available in
[Studios Universe - Modules documentation](/universe/modules#using-the-import-command).

##### Enable in the App

Update your `design/modules.yaml` file
to include the following line:

```yaml
app:
  name: ...

  modules:
    - account
    - blog
```

##### Create a Menu Entry

You can create menu links
for the modules in navbar,
by editing the file:

```sh
design/layout.yaml
```

add the following:

```yaml
app:
  name: ...

  layout:
    navbar:
      ...
      leftItems:
        ...
        - name: posts
          route: "/posts"
          roles:
            - user
            - admin
```


##### Push the Changes

If you have deployed your application,
you will need to push and migrate
to see the changes.

#### Module Overview

The following is the directory layout
of your new blog module.

```sh
blog/
│
├── module.yaml
├── post.yaml
├── comment.yaml
├── tag.yaml
│
├── pages
│   ├── all-posts.yaml
│   ├── edit-post.yaml
│   ├── new-post.yaml
│   ├── user-posts.yaml
│   ├── view-post.yaml
│   └── post
│       ├── edit
│       │   ├── content.html
│       │   └── style.scss
│       ├── list
│       │   ├── content.html
│       │   └── style.scss
│       ├── new
│       │   ├── content.html
│       │   └── style.scss
│       ├── user
│       │   ├── content.html
│       │   └── style.scss
│       └── view
│           ├── content.html
│           └── style.scss
│
├── components
│   └── CommentOwnerEditable.jsx
│
├── locales
│   ├── en.json
│   └── es.json
│
└── seeds
    └── posts.json
```

- `module.yaml` is the module design.
- `[post,comment,tag].yaml` are type designs.
- `pages/` contains a number of custom pages.
- `components/` has a custom components.
- `locales` has i18n translations.
- `seeds` has some initial data for the module.

#### Extending and Overriding

You can extend and override an imported module by
writing types, pages, and component files
in your application's `design` folder.

##### Extend the Design

Designs from the `design-vendor` directory
can be extended and overriden.
This means you can write just the new design
for your desired changes.
Create the same folder / file structure,
as well as the same, minimal object structure,
to extend and override.

__Start the mirrored directories__

```sh
mkdir -p design/modules/blog/locales
```

__Create the file: `design/modules/blog/post-mods.yaml`__

```yaml
type:
  name: post

  # extend by adding field 'blurb'
  fields:
  - name: blurb
    type: string
    length: 256
```

__Create the file: `design/modules/blog/locales/en.js`__

```sh
cp design-vendor/modules/blog/locales/en.js design/modules/blog/locales/en.js
```

and add

```sh
"blurb": "Blurb",
```

to the json

```json
{

  "post": {
    "fields": {

      "blurb": "Blurb",

    }
  }
    
}
```

##### Overriding a Page


__Create the mirrored directory__

```sh
mkdir -p design/modules/blog/pages/list
```

__Create the file: `design/modules/blog/pages/post/list/content.html`__

```sh
cp design-vendor/modules/blog/pages/post/list/content.html design/modules/blog/pages/post/list/content.html
```

and change (around line 32)

```jsx
<p className="mb-1">{ post.content.substring(0,64) }</p>
```

to

```jsx
<p className="mb-1">{ post.blurb }</p>
```

##### Updating the Application

The next section is all about this.
It assumes we are deploying for the first time,
so if you already have deployed your application,
you can skip some steps.

_Note_ that because we have changed the shape of the data,
we will need to both:

- push the application code
- migrate the database

_(TODO dev note, add a flag to push, so one can migrate as well)_

#### Custom and Private Repositories

The import command has a longer format enabling the use
any git based repository or the local filesystem.
See the [Studios Universe - Modules documentation](/universe/modules) for more information.

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.

