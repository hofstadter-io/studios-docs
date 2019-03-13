---
title: "Updating"
date: 2019-03-02T11:58:26-06:00
draft: false
type: "page"

weight: 9
---


#### Update the App

This is the main command used to push application updates.
Run the following from your application directory:

```
hof app push
```

you can also

```
hof app pull
```

to get your application from __Studios__.

#### Update the database

When you change the model for your types,
you will need to run a database migration.

Run this to only migrate:

```
hof db migrate
```

and this to migrate and reset the data:

```
hof db seed
```

If you need to reset the database completely, run:

```
hof db reset
```


#### Renaming fields and other design

Renaming fields and other design paths
often requires adding a "rename" field.

```
  ...
  name: <old-name>
  rename: <new-name>
```

Then, do the app and database updates:

```
hof app push
hof db seed
```

and then making then name
the new name.

```
  ...
  name: <new-name>
```

and finally

```
hof app push
```

See the more advanced section
for further details.

