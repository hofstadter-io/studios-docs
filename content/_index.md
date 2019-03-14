---
title: "Hofstadter Studios Documentation"
date: 2019-03-14
draft: false
type: "page"
---

# Hofstadter Studios


##### The Declarative Programming and Rapid Development Platform

__Hofstadter Studios__ is a
declarative programming and rapid development platform.
You describe your idea as "designs",
_the single-source of truth_, and
your real-time application updates to reflect the changes.
__Hofstadter Studios__ will generate a
full implementation and handle the management
so you can rapidly iterate on your ideas.

[Getting Started](./getting-started)
🐢
[Basics](./basics)
🐢
[Tutorials](./tutorials)
🐢
[Universe](./universe)
🐢
[Reference](./reference)
🐢
[Open Source](https://github.com/hofstadter-io)

The following demo video follows along with the Getting Started section

<div class="embed-responsive embed-responsive-16by9">
  <iframe src="https://www.youtube.com/embed/CI4355YizBA" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></iframe>
</div>



### Hofstadter Studios

In Hofstadter Studios you describe your application.
You design users and their profiles,
the kinds of things they can do,
the relations they have with their resources and each other,
the rules around who can do what given their roles.
You then specify how
data is visualized,
interfaces look and feel,
the user flows and much more,
all while having control down to the pixel.
An event and serverless system enables you
to customize the logic and take extra actions.

Hofstadter Studios will build you a live, real-time
application that you can rapidly iterate on.
Just __hof app push__ and your application is sent
to Studios where the changes are understood
and applied as neccessary throught the technology stack.
Databases will be migrated, code will be updated, clients will be refreshed.

{{<mermaid align="left">}}
graph TB;
    Designs -.->|hof app push| H(Hofstadter Studios)
    H -.->|client update & refresh| C[React/Native, SDKs]
    H -.->|server update & scaling| S[GraphQL, REST APIs]
    H -.->|migrations & management| DB[Databases & Proxies]
    H -.->|triggers, events & flows| SS[Serverless System]
{{< /mermaid >}}

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

### Resources and Designs

Designs are the central concept in __Hofstadter Studios__
with which you describe your application.
Designs express your idea in special languages,
commonly referred to as Domain Specific Languages (DSL).
__Studios__ has DSLs for __apps__, __modules__, and __types__.
Apps group modules, modules group types,
and all three can have pages and components.

Here is an eample design for
an "Item" for a Todo application:

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

  owned:
    name: author
    type: has-many

  relations:
    - name: labels
      type: type.modules.todo.Label
      relation: many-to-many

  auth:
    default: true

  pages:
    default: true

  components:
    default: true

  search:
    fields:
      - name
      - description
      - content
    relations:
      - labels.value
```

DSLs are used to drastically increase
the word to powering technology ratio.
In a few hundred lines you can create applications
full of features and ready for users.
Change your design, do a __hof app push__
and the application updates itself
automatically on all the devices.

The following are the top-level specification for the
__app__, __module__, __type__, and __page__/__component__ DSLs.
Check out the [getting started with Designs](/getting-started/designs) to learn more.

##### Application Design

```yaml
app:
  name: my-app
  title: My Studios App

  config: ...
  modules: ...

  layouts: ...
  pages: ...
  components: ...
  forms: ...

  imports: ...
  files: ...
  translations: ...
  seeds: ...
```

##### Module Design

```yaml
module:
  name: notes
  types: ...

  pages: ...
  components: ...
  forms: ...

  files: ...
  translations: ...
  seeds: ...
```

##### Type Design

```yaml
type:
  name: note

  fields: ...
  relations: ...

  owned: ...
  auth: ...
  visibility: ...

  pages: ...
  components: ...
  forms: ...

  files: ...
  translations: ...
  seeds: ...
```

##### Page & Component Design

```yaml
# can appear in app, module, or type
app|module|type:
  name: ...

  # pages and components have the same sub-design or DSL
  pages|component:
    - name: page-view
      route: "/page/:id"

      style: ...         # list of SCSS files
      content: ...       # list of JSX files

      imports: ...       # custom imports, pages only
      components: ...    # custom components
      translations: ...  # internationalization files

      # Inject the user and data into the page or component
      #   the current user in the page data
      current-user: ...
      data: ...
```



### Building with Studios



