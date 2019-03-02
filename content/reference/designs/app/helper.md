---
title: "helpers"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1000
---

### APP_NAME_BLACKLIST

#### spec

```yaml
blacklist:
- hof
- hofstadter
ctx_path: dsl.0-0-1.app.docs.helper-types.[0]
name: APP_NAME_BLACKLIST
parent: app
parent_path: dsl.0-0-1.app.docs
path: helper-types
pkg_path: 0-0-1/app/docs/helper-types
pkgPath: app/APP_NAME_BLACKLIST
type: NAME_REGEX

```

### AUTHOR_REGEX

#### spec

```yaml
ctx_path: dsl.0-0-1.app.docs.helper-types.[1]
name: AUTHOR_REGEX
parent: app
parent_path: dsl.0-0-1.app.docs
path: helper-types
pkg_path: 0-0-1/app/docs/helper-types
pkgPath: app/AUTHOR_REGEX
regex: ^[[:alpha:]][[:word:] -\<\>\@\.]*$
type: string

```

### NPM_IMPORT_REGEX

#### spec

```yaml
ctx_path: dsl.0-0-1.app.docs.helper-types.[2]
name: NPM_IMPORT_REGEX
parent: app
parent_path: dsl.0-0-1.app.docs
path: helper-types
pkg_path: 0-0-1/app/docs/helper-types
pkgPath: app/NPM_IMPORT_REGEX
regex: ^[[:alpha:]][[:word:]-]*$
type: string

```

### NPM_VERSION_REGEX

#### spec

```yaml
ctx_path: dsl.0-0-1.app.docs.helper-types.[3]
name: NPM_VERSION_REGEX
parent: app
parent_path: dsl.0-0-1.app.docs
path: helper-types
pkg_path: 0-0-1/app/docs/helper-types
pkgPath: app/NPM_VERSION_REGEX
regex:
- ^[\~\^]?[[:digit:]]+\.[[:digit:]]+\.[[:digit:]]+$
- ^[\~\^]?[[:digit:]]+\.[[:digit:]]+$
- ^[\~\^]?[[:digit:]]+$
type: string

```

