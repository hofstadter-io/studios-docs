---
title: "helpers"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1000
---

Helpers:

- [APP_NAME_BLACKLIST](#APP_NAME_BLACKLIST)
- [AUTHOR_REGEX](#AUTHOR_REGEX)
- [NPM_IMPORT_REGEX](#NPM_IMPORT_REGEX)
- [NPM_VERSION_REGEX](#NPM_VERSION_REGEX)

---

### APP_NAME_BLACKLIST

__Spec__

```yaml

blacklist:
- hof
- hofstadter
name: APP_NAME_BLACKLIST
path: helper-types
type: NAME_REGEX

```

### AUTHOR_REGEX

__Spec__

```yaml

name: AUTHOR_REGEX
path: helper-types
regex: ^[[:alpha:]][[:word:] -\<\>\@\.]*$
type: string

```

### NPM_IMPORT_REGEX

__Spec__

```yaml

name: NPM_IMPORT_REGEX
path: helper-types
regex: ^[[:alpha:]][[:word:]-]*$
type: string

```

### NPM_VERSION_REGEX

__Spec__

```yaml

name: NPM_VERSION_REGEX
path: helper-types
regex:
- ^[\~\^]?[[:digit:]]+\.[[:digit:]]+\.[[:digit:]]+$
- ^[\~\^]?[[:digit:]]+\.[[:digit:]]+$
- ^[\~\^]?[[:digit:]]+$
type: string

```
