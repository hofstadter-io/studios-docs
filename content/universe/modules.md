---
title: "Modules"
date: 2018-03-12T00:00:00-06:00
draft: false
type: "page"

weight: 10
---

Modules are git repositories with prefigured functionality for __Studios__ applications.


#### Hofstadter Modules:

- [studios-modules](https://github.com/hofstadter-io/studios-modules)
    - account-default
    - simple-blog


#### Community Modules:

- Be the first!

Make a Pull Request to have your __Studios__ module added here!

(there is a link at the bottom of this page)


#### Using the import command

```sh
hof import "<bundle>"
```

- `bundle`: `<repo-url>@<git-ref>#<sub-dir>`
    - repo-url: `https://...` or a local path. If local, git-ref is ignored.
    - git-ref: a branch, tag, or commit hash.
    - sub-dir: into the repository, this is how collection repos are handled.

This will place the bundles design in the `design-vendor` directory.

#### Custom and Private Repositories

The import command has a longer format enabling the use
any git based repository or the local filesystem.
See the [Studios Universe - Modules documentation](/universe/modules) for more information.

Private repositories are supported for GitHub using
the `GITHUB_TOKEN` environment variable.

