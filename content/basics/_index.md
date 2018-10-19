---
title: "Studios Basics"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 5
---

This section will teach you the basics of
working with Hofstadter studios.
We'll start with the layout of the
application directory structure
and then go through the various files and folders.


#### Application Stack

The application stack is:

- React / React Native
- Apollo GraphQL
- NodeJS with Express
- Postgres Database
- Docker and Kubernetes


#### Main Commands

Update the application code:

```
hof push
```

Update the database:

```
hof db reset
```

This will reset and reseed your database.
(seemless migrations are coming soon!)

Application restart:

```
hof app reset
```

#### Updating Fields

To update or add new fields to users or types:

- add the field "migrations"
- `hof push`
- `hof db reset`
- remove the "migrations" field
- `hof push`

```
fields:
  - name: someField
    type: string
    length: 64
    migrations: true
```

You can shortcut this, but you may see errors
or your application can break until the database is reset.


