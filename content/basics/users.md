---
title: "Users"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 15
---

Your application comes with `users` out of the box.
This includes:

- login and oauth
- password management
- access permissions
- admin controls

Hofstadter Studios handles the common user attributes:

- email
- username
- password
- role
- isActive

With users, you can change the profile fields or attributes,
as well as the translation files.

```
app:
  name: "hof-starter-app"

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
    translations:
      - name: en
        file: "translations/user/en.json"
      - name: es
        file: "translations/user/es.json"
```

The field types can be:

- __string__, with a maximum length.
- __text__, with no limit.
- __boolean__
- __integer__
- __decimal__
- __date__
- __time__
- __datetime__




