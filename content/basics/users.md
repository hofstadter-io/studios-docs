---
title: "Users"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 15
---

Your application comes with __Users__ out of the box.
The main thing you will do with users
is give them ownership of types
and assign auth permissions.
This happens at the __Type__ level,
where you design the details.

Hofstadter Studios handles the common user attributes:

- id
- email
- username
- password
- role
- isActive

As well as the user flow related to authenication and authorization:

- login and oauth
- password management
- account recovery
- access permissions
- admin controls

There are hooks and notifications for changes and other events...
coming soon.

```
app:
  name: "hof-starter-app"

  user:
    events:
      ...
    hooks:
      ...

    translations:
      - name: en
        file: "translations/user/en.json"
      - name: es
        file: "translations/user/es.json"
```

