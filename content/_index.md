---
title: "Hofstadter Studios Documentations"
date: 2018-10-08
draft: false
type: "page"
---

# Hofstadter Studios Documentation


#### The Declarative Programming and Rapid Development Platform

Hofstadter Studios is a flexible and extensible
declarative programming and rapid development platform.
Express your application through focused languages, via designs,
describing the data shape, flow, and presentation.
Studios will generate the majority of the implementation
leaving you to focus on the concept and experience for
your application or business.

[Getting Started](./getting-started)
🐢
[Basics](./basics)
🐢
[Concepts](./concepts)
🐢
[Videos](https://www.youtube.com/channel/UCG-DPa80f649-KP_LNzAmSQ/playlists)
🐢
[Downloads](https://github.com/hofstadter-io/hof/releases)

#### Overview

In Hofstadter Studios, you describe your application.
You can talk about users and their profiles,
the kinds of things they can do,
the relations they have with their resources and each other,
the rules around who can do what given their roles.
You will also talk about how data and information
is visualized, how interfaces look and feel,
to how the user flow and interactions work.

Hofstadter Studios will build you a live, real-time
application that you can rapidly iterate on.
Domain Specific Languages are used to drastically increase
the word to powering technology ratio.
In a few hundred lines you can create applications
full of features and ready for users.
Change your design, do a __hof push__
and the application updates itself
automatically on all the devices.
When your ready to send the latest version
just do a __hof deploy__ and it does.

Behind the scenes Hofstadter Studios
is creating and managing
a code base and technology stack.
Infrastructure, DevOps, databases,
backend API servers, authentication,
frontend web and mobile apps,
all generated to let you focus on the
important parts.

Your ability to configure and customize
is what makes your app yours
and is built into the core of Hofstadter Studios.
From the look, layout, and feel,
to the business logic and data sources,
you have the ability to style your
application and create that
desired experience or process.

Enough of the high-level,
let's see some designs.

#### Designs

Designs express and idea in special languages,
as a group referred to as Domain Specific Languages (DSL).
For example, here is a design for a user:

```yaml
user:
  profile:
    fields:
      - name: first_name
        type: string
        length: 64
      - name: middle_name
        type: string
        length: 64
      - name: last_name
        type: string
        length: 64
      - name: title
        type: string
        length: 16
      - name: suffix
        type: string
        length: 16
      - name: age
        type: int
        validation:
          - type: >=
            value: 0
      - name: language
        type: enum
        choices:
          - en_US
          - es_ES
      - name: picture
        type: image
```

"__user__" is the name of a DSL.
All users have a profile, composed
of a number of fields.
Each field has a required name and a type,
as well as extra details or configuration,
depending on the type.
Every DSL will have its own
words, components, and options.
One important commonality between
the languages, designs, and sub-details
is the use of "__name__".
"__name__" is used for significant pieces
of your designs and files.

What you don't see here are typical fields,
ones like `id`, `email`, `password`, or `role`.
Hofstadter Studios has a number of fields
pre-included so that users can
manage thier account and credentials
and the platform can manage
authentication and permissions.
You can also configure OAuth and Payments.

Let's look at the design for an "Item"
such as in a todo application:

```yaml
type:
  name: Item

  fields:
    - name: name
      type: string
    - name: description
      type: string
    - name: contentType
      type: string
    - name: content
      type: text
    - name: data
      type: json

  owners:
    - type: user
      relation: has-many

  relations:
    - name: categories
      type: type.modules.todo.ItemCategory
      relation: many-to-many
    - name: tags
      type: type.modules.todo.ItemTag
      relation: many-to-many

  auth:
    edit: ["admin", "owner"]
    view: ["public"]

  search:
    fields:
      - name
      - description
      - content
    relation-fields:
      - categories.value
      - tags.value
```

"__type__" is an important DSL
and is central to data shape and flow.
We see types can have have fields,
like the user profile,
as well as owners and relations to
other types or data.
You also specify the auth or permissions
as well as advanced functionalities
like searching, social, and privacy.

As you work with Hofstadter Studios
and update your designs,
just __hof push__ to send the latest
out to your live application server.
Here's what it's like...


### Demo


# INSERT VIDEO




