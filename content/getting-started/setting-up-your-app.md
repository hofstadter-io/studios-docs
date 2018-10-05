---
title: "Setting Up Your App"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 3
---

Once you have an account and the __hof__ tool [installed](../installation/),
you can setup your local working copy.


#### Setting up the working directory

There are two main methods for setting up your application.
In either case, `app-name` is the name of your application
when it was setup initially in Hofstadter Studios.

##### Using the Hof tool

You can follow wither of these two sub-methods:

```
mkdir app-name
cd app-name
hof app create
```

or

```
hof app create app-name
cd app-name
```


##### Clone the hof-starter-app

The initial version of your application will match
[hof-starter-app](https://github.com/hofstadter-io/hof-starter-app).


```
git clone https://github.com/hofstadter-io/hof-starter-app app-name
cd app-name
```

You can also use any starter-app you or anyone else creates.


#### Connecting your app to Studios

Open the `hof.yaml` file that is in your application directory.
Place your username and API Key in the appropriate fields.

Run:

```
hof app status
hof app version
```

to test that you are connected.
If you used the __hof__ tool method for setting up your application,
run:

```
hof pull
```

to get the initial design, code, and data.


#### Community Starter Apps

Make a Pull Request to have your starter app added here!

(there is a link at the bottom of this page)


