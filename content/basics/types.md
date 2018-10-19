---
title: "Types"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 20
---

Types are the resources in your application
that users can interact with.
We'll be using the types from the
hof-starter-app [blog module](https://github.com/hofstadter-io/hof-starter-app/tree/master/design/modules/blog).

Here is the __post__ type:

```
type:
  name: post

  owned:
    name: author
    type: has-many

  visibility:
    enabled: true
    default: false
    public: published
    private: draft

  fields:
  - name: title
    type: string
    length: 128
  - name: content
    type: text

  relations:
  - name: comments
    type: type.modules.blog.comment
    relation: one-to-many
  - name: tags
    type: type.modules.blog.tag
    relation: many-to-many

  auth:
    view:
      private: ['admin']
    create: ['user']
    update: ['admin']
    delete: ['admin']

  pages:
    list:
      route: "/posts"
      style: "design/modules/blog/pages/list/style.scss"
    view:
      route: "/post/:id"
      style: "design/modules/blog/pages/view/style.scss"
      custom: true
      files:
        - "design/modules/blog/pages/view/content.html"
```


#### fields

Fields are the attributes for your types or resources.
The field types can be:

- __string__, with a maximum length.
- __text__, with no limit.
- __boolean__
- __integer__
- __decimal__
- __date__
- __time__
- __datetime__

You will need to use the database update process
from [updating fields](/basics/#updating-fields).


#### owned

Owned means that a user is the owner of the type.
Owned itself has a "name" and a "type".

```
  owned:
    name: author
    type: has-many
```

__name__ is the word used for the user owner.

__type__ can be one of:

- has-one
- has-many


#### visibility

Visibility enables a public/private control
on the type when enabled.

```
  visibility:
    enabled: true
    default: false
    public: published
    private: draft
```

__default__ specifies the default setting.

__public__ and __private__ are the words
used for the visibility settings.


#### relations

Relations are how you connect types to each other.
There are __one-to-one__, __one-to-many__, and __many-to-many__
relationships.

```
  relations:
  - name: comments
    type: type.modules.blog.comment
    relation: one-to-many
  - name: tags
    type: type.modules.blog.tag
    relation: many-to-many
```

__name__ is the name of the relationship
and will be used within the data returned to the client.

__relation__ is one of the relation types.

__type__ is `type.path.to.thing`. It starts with "type"
and then is generally "module.<mod-name>", and then
the actual type name.
This is driven by the file path to the type.


#### auth

Auth provides controls over the
actions which can be taken on the your type.
If the type is __owned__, the owner
(currently) has permissions for all of the actions
(so you don't have to include it).

```
  auth:
    view: ['admin']
    # or
    view:
      public: ['user']
      private: ['admin']
    create: ['user']
    update: ['admin']
    delete: ['admin']
```

Each action under auth accepts an array of roles.
Currently, there is "user" and "admin",
with owner being automatic.

If your type has visibility enabled,
then view has two subfields for the
public and private access settings.

#### pages

Pages are where you specify the routes
and assets tied to the views and actions
for your types.


```
  pages:
    list:
      route: "/posts"
      style: "design/modules/blog/pages/list/style.scss"
    view:
      route: "/post/:id"
      style: "design/modules/blog/pages/view/style.scss"
      custom: true
      files:
        - "design/modules/blog/pages/view/content.html"
```

The pages subfields are:

- list
- view
- add
- update

each page has:

- __route__, for the client url location
- __style__, for custom styling
- __custom__, to enable custom html for the React render function
- __files__, a list of files to inject when using custom

The next section will show you how to work with the pages.

