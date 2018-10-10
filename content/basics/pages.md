---
title: "Pages"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 25
---

__Pages__ enable you to create custom
content, layouts, and data interactions.
While many of the types or resources you create
will have many pages automatically generated,
__pages__ allows you to extend those defaults.

For now, the pages consist of static content.
Later, data sources and much more will be incorporated.

#### Overview

Pages have two main parts, design and files.
Design is where you specify the high-level portion of the page,
and files will hold the specific content.

The __pages__ resource was "designed" by Hofstadter Studios
to be flexible, reusable, and extensible with the rest of the system.

Let's take a look.


#### Design

Here is the design for a couple of pages:

```yaml
app:
  name: "hof-starter-app"

  pages:

    - name: home
      route: "/"
      files:
        - "pages/home/home.html"
        - "pages/common/footer.html"
      translations:
        - name: en
          file: pages/home/locales/en.json
        - name: es
          file: pages/home/locales/es.json

    - name: about
      route: "/about"
      files:
        - "pages/about/about.html"
        - "pages/common/footer.html"
      translations:
        - name: en
          file: translations/translations.json
        - name: es
          file: translations/translations.json
```

Each page starts with a "__name__" and a "__route__".
The route is the part that will show up in the browser.
__Overriding a route from a resource, module, or type
will cause issues and break your application.
There will be similar machanisms for customizing
those pages coming soon.__

To specify the content of the page,
we reference a list of "__files__" and "__translations__".
Files are rendered in order on the page, in the main section.
Notice that you can share html content between pages.

Translations enable you to create multi-lingual content.
The translations themselves are just data
which is then referenced in the html files.
This means you can have a single layout for consitency
and have the language filled in from the data.
More on this a little further down this page.


#### Content

Hofstadter Studios enables you to create
any number of pages to accompany your application.
At a minimum, you will need to have the home page.

Currently, the frameworks available are
React + Bootstrap through the
[reactstrap](https://reactstrap.github.io/components/) library.
You may use any of the components there.
The thing to know is that you must prepend
"__RS.__" to the component's opening and closing tags.
For example:

```html
<RS.Alert color="primary">
  This is a primary alert — check it out!
</RS.Alert>

<RS.Container>
  <RS.Row>
    <RS.Col>Look, a column!</RS.Col>
  </RS.Row>
</RS.Container>
```

#### Translations

Translations provide you the method to have
internationalization content, also known as "i18n."
In Hofstadter Studios, the language content is data.
To see how this works, lets look at the existing home page files.

__pages/home/locale/en.json__

```json
{
  "title": "Home",
  "meta": "Home example page",
  "loading": "Loading...",
  "messages": {
    "hello": "Hello"
  }
}
```

__pages/home/locale/es.json__

```json
{
  "title": "Inicio",
  "meta": "Página de Inicio",
  "loading": "Cargando...",
  "messages": {
    "hello": "Hola"
  }
}
```

Notice that the json object fileds are the same,
and it's the calues that change. While the field
names are in english, this does not matter,
only that they have the same shape.
How to use the language data in your pages,
use the `t()` function like so:

__pages/home/home.html__

```html
<h1>{ t('title') }</h1>

<p>{ t('messages.hello') } from Hof Starter App</p>

```

Notice that the format is:

```
{ t('path.to.language.data') }
```

There are curly braces (beacuse this is actually injected into JSX code)
and the `t('...')` function is inside of the `{ ... }`.

_Another note, you need to close all of your html tags,
including <br /> and <hr></hr>. Either form is OK.__



