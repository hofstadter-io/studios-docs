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


#### Application Commands

Update the application code:

```
hof push
```

#### Database Commands

Update the database schema:

```
hof db migrate
# or
hof db seed
```

(seed will run migrations too, but will destroy existing data)

Updating Fields:

Update or add new fields to your types, then

- `hof push`
- `hof db migrate`

Hofstadter Studios handles schema updates and database migrations
seemlessly in the background for you


#### Function Commands

Deploy a Serverless function:

```
hof func deploy my-fn
```

Delete a function:

```
hof func delete my-fn
```
