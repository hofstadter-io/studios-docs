---
title: "Layout"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 26
---

Hofstadter Studios gives you the ability
to customize the major layout components.

```
app:
  name: "hof-starter-app"

  layout:

    site:
      style: "pages/layout/site.scss"

    navbar:
      custom: false
      file: "pages/layout/navbar/content.html"
      style: "pages/layout/navbar/navbar.scss"
      translations:
        - name: en
          file: pages/layout/navbar/locales/en.json
        - name: es
          file: pages/layout/navbar/locales/es.json

      logo:
        type: image
        source: "https://hofstadter.io/images/hof-logo.png"
        # type: text
        # value: "HofStarterKit"

      leftItems:
        - name: posts
          href: "/posts"
          roles:
            - user
            - admin
        - name: users
          href: "/users"
          roles:
            - admin
        - name: about
          href: "/about"
        - name: contact
          href: "/contact"

    center:
      file: "pages/layout/content/content.html"
      translations:
        - name: en
          file: pages/layout/content/locales/en.json
        - name: es
          file: pages/layout/content/locales/es.json

    footer:
      file: "pages/layout/footer/content.html"
      style: "pages/layout/footer/footer.scss"
      translations:
        - name: en
          file: pages/layout/footer/locales/en.json
        - name: es
          file: pages/layout/footer/locales/es.json
```


### site

### layout

### drawer

https://bootstrapious.com/p/bootstrap-sidebar

### navbar

### center

### footer

