---
title: "Applications"
date: 2018-03-12T00:00:00-06:00
draft: false
type: "page"

weight: 5
---

Applications are starting points for a __Studios__ application.
They act as templates and have all the things needed for a
`hof app create, push, deploy, enjoy` out-of-the-box.

#### Hof Starter Apps:

- [hof-starter-app-minimal](https://github.com/hofstadter-io/hof-starter-app-minimal) (the default)
- [hof-starter-app](https://github.com/hofstadter-io/hof-starter-app)

#### Community Starter Apps:

- Be the first!

Make a Pull Request to have your __Studios__ starter app added here!

(there is a link at the bottom of this page)

#### Using the Create Command

The create command can work off of a URL supporting git like
GitHub, GitLab, or Bitbucket.

```
hof app create <name> <version> <template-url>
```

example:

```
hof app create my-app beta https://github.com/hofstadter-io/hof-starter-app
```

- `name` is a kebab-style-name
- `version` is a Studios version
- `template-url` is a URL to a git repository

Studios versions can be found by running:

```
hof app versions
```

##### Private Repositories

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.
