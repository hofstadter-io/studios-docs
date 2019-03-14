---
title: "Lifecycle"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 9
---

Most `hof app` commands are run from the application directory.
The following commands are used in the application lifecycle.

### Application Lifecycle

__Deploy, Shutdown__

```sh
hof app deploy
hof app shutdown
```

__Moving code__

```sh
hof app push
hof app pull
```

_Note, push and pull do_ __not__ _require the application to be deployed._


__Updating to a new Studios version__

```sh
hof app update "<version>"
```

__Resetting the application__

```sh
hof app reset
```

### Database Lifecycle

When you change the data model within your types
you will need to run a database migration.

_note this is not all changes, the following, and maybe some undocumented ones_

```yaml
type:
  owned: ...
  visibility: ...
  fields: ...
  relations: ...
```

__Only migrate__

```sh
hof db migrate
```

__Migrate and reset the data__

```sh
hof db seed
```

__Completely reset the database__

```sh
hof db reset
```

__This will reset the tables, migration history,
and restore to the current desired state with seed data.__


#### Renaming fields and other design

Renaming fields and other design paths
often requires adding a "rename" field.

```yaml
  ...
  name: <old-name>
  rename: <new-name>
```

Then, do the app and database updates:

```sh
hof app push
hof db seed
```

and then making then name
the new name.

```yaml
  ...
  name: <new-name>
```

and finally

```sh
hof app push
```

See the more advanced section
for further details.


#### Complex changes

Changing the type of a field, possibly with the name as well,
can create changes which would destroy existing data.
In these cases, it is often better to

1. create new field
1. migrate database
1. transform data
1. delete old field
1. migrate database

As we find more of these cases,
we will add extra configuration and transformations
to enable the process to become more smooth.



### Function Lifecycle

coming soon, though you can push them today

