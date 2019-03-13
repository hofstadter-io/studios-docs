---
title: "Importing"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 7
---

You can import modules from any Git repository like GitHub, GitLab, or Bitbucket.
These are preconfigured __Studios__ modules which contain:

- types
- pages
- components
- translations

With modules, you can quickly expand the functionality
within your application.

You can find a list and help for the import command at:
[Studios Universe - Modules](/universe/modules).


#### Import a "simple-blog" Module

The `simple-blog` has
types, pages, and components for
posts, comments, and tags.
This module shows many of the configurable
options within the designs.

To import the `simple-blog`:

```
hof import "#simple-blog"
```

You can now find the `blog` module
at `design-vendor/modules/blog/`

Update your `design/modules.yaml` file
to include the following line:

```
app
  name: ...

  modules:
    - blog
```

If you have deployed your application,
you will need to push and migrate
to see the changes.

#### Module Overview

The following is the directory layout
of your new blog module.

```
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

#### Extending & Overriding

You can extend and override an imported module by
writing types, pages, and component files
in your application's `design` folder.

##### Extend the Design



##### Override a Page



