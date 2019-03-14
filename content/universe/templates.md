---
title: "Templates"
date: 2018-03-12T00:00:00-06:00
draft: false
type: "page"

weight: 15
---

Templates are used for the creation of "new" things.


#### Hofstadter Templates:

- [studios-templates](https://github.com/hofstadter-io/studios-templates)


#### Community Templates:

- Be the first!

Make a Pull Request to have your __Studios__ module added here!

(there is a link at the bottom of this page)


#### Using the new command

```sh
hof new "<what>" "<where/name>" "<template>"
```

- `what`: `[module,type,page,component]`
- `where`: `design/.../<name>`
    - module: `design/modules/<name>`
    - type: `design/modules/some-module/<name>`
    - app page: `design/<name>`
    - module page: `design/modules/some-module/<name>`
    - app component: `design/<name>`
    - module component: `design/modules/some-module/<name>`
- `template`: `<repo-url>@<git-ref>#<sub-dir>`
    - repo-url: `https://...` or a local path. If local, git-ref is ignored.
    - git-ref: a branch, tag, or commit hash.
    - sub-dir: into the repository, this is how collection repos are handled.

#### Custom and Private Repositories

The new command has a longer format enabling the use
any git based repository or the local filesystem.
See the [Studios Universe - Templates documentation](/universe/templates) for more information.

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.

