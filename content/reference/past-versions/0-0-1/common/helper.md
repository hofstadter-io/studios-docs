---
title: "helpers"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1000
---

Helpers:

- [SEMVER_REGEX](#SEMVER_REGEX)
- [NAME_REGEX](#NAME_REGEX)
- [TEXT_REGEX](#TEXT_REGEX)
- [NAME_BLACKLIST](#NAME_BLACKLIST)
- [SEEDFILE_REGEX](#SEEDFILE_REGEX)
- [SEEDS_SNIPPET](#SEEDS_SNIPPET)
- [I18NFILE_REGEX](#I18NFILE_REGEX)
- [I18N_SNIPPET](#I18N_SNIPPET)
- [FILEPATH_REGEX](#FILEPATH_REGEX)
- [FILES_SNIPPET](#FILES_SNIPPET)
- [TYPEPATH_REGEX](#TYPEPATH_REGEX)
- [COMPONENT_REGEX](#COMPONENT_REGEX)
- [DATA_SNIPPET](#DATA_SNIPPET)
- [COMPONENT_SNIPPET](#COMPONENT_SNIPPET)
- [PAGE_ROUTE_REGEX](#PAGE_ROUTE_REGEX)
- [PAGE_COMPONENT_SNIPPET](#PAGE_COMPONENT_SNIPPET)
- [PAGES_SNIPPET](#PAGES_SNIPPET)

---

### SEMVER_REGEX

__Spec__

```yaml

name: SEMVER_REGEX
path: helper-types
regex: ^[[:digit:]]+\.[[:digit:]]+\.[[:digit:]]+$
type: string

```

### NAME_REGEX

__Spec__

```yaml

name: NAME_REGEX
path: helper-types
regex: ^[[:alpha:]][[:word:]-]*$
type: string

```

### TEXT_REGEX

__Spec__

```yaml

name: TEXT_REGEX
path: helper-types
regex: ^[[:alpha:]][[:word:] -]*$
type: string

```

### NAME_BLACKLIST

__Spec__

```yaml

blacklist:
- cookies
- debug
- graphqlTypes
- i18n
- mailer
- proxy
- user
- components
- defaultRouter
- favicon
- layout
- pageNotFound
- pages
name: NAME_BLACKLIST
path: helper-types
type: NAME_REGEX

```

### SEEDFILE_REGEX

__Spec__

```yaml

lookup-file: true
name: SEEDFILE_REGEX
path: helper-types
regex: ^([[:word:]-]+\/)+[[:word:]-]+\.json$
type: string

```

### SEEDS_SNIPPET

__Spec__

```yaml

fields:
- name: file
  type: SEEDFILE_REGEX
- items:
    fields:
    - name: name
      type: NAME_BLACKLIST
    - name: data
      type: NAME_REGEX
    - name: type
      type: TYPEPATH_REGEX
    - name: lookup
      optional: true
      type: ignore
    type: object
  name: types
  type: list
name: SEEDS_SNIPPET
path: helper-types
type: object

```

### I18NFILE_REGEX

__Spec__

```yaml

lookup-file: true
name: I18NFILE_REGEX
path: helper-types
regex: ^([[:word:]-]+\/)+[[:word:]-]+\.json$
type: string

```

### I18N_SNIPPET

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_REGEX
  - name: file
    type: I18NFILE_REGEX
  type: object
name: I18N_SNIPPET
path: helper-types
type: list

```

### FILEPATH_REGEX

__Spec__

```yaml

lookup-file: true
name: FILEPATH_REGEX
path: helper-types
regex: ^(design|custom|pages|seeds|translations)\/([[:word:]-]+\/)+[[:word:]-]+\.[[:lower:]]{1,4}$
type: string

```

### FILES_SNIPPET

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_BLACKLIST
  - name: src
    type: FILEPATH_REGEX
  - name: dst
    type: FILEPATH_REGEX
  type: object
name: FILES_SNIPPET
path: helper-types
type: list

```

### TYPEPATH_REGEX

__Spec__

```yaml

lookup-design: true
name: TYPEPATH_REGEX
path: helper-types
regex: ^type\.modules\.[[:word:]-]+\.[[:word:]-]+$
type: string

```

### COMPONENT_REGEX

__Spec__

```yaml

lookup-design: true
name: COMPONENT_REGEX
path: helper-types
regex: ^(type|module)\.modules\.([[:word:]-]+\.){1,2}components\.[[:word:]-]+$
type: string

```

### DATA_SNIPPET

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_BLACKLIST
  - name: type
    type: TYPEPATH_REGEX
  - fields:
    - name: type
      regex: ^(view|list)$
      type: string
    - name: sync
      optional: true
      type: boolean
    - name: filter
      optional: true
      type: ignore
    - name: variables
      optional: true
      type: ignore
    name: query
    optional: true
    type: object
  - items:
      regex: ^(create|update|delete)$
      type: string
    name: mutations
    optional: true
    type: list
  type: object
name: DATA_SNIPPET
path: helper-types
type: list

```

### COMPONENT_SNIPPET

__Spec__

```yaml

name: COMPONENT_SNIPPET
path: helper-types
type: variant
variants:
- fields:
  - name: default
    type: boolean
  type: object
- items:
    fields:
    - name: name
      type: NAME_BLACKLIST
    - items:
        type: FILEPATH_REGEX
      name: style
      optional: true
      type: list
    - items:
        type: FILEPATH_REGEX
      name: content
      optional: true
      type: list
    - name: current-user
      optional: true
      type: boolean
    - name: data
      optional: true
      type: DATA_SNIPPET
    type: object
  type: list

```

### PAGE_ROUTE_REGEX

__Spec__

```yaml

name: PAGE_ROUTE_REGEX
path: helper-types
regex:
- ^\/$
- ^(\/[[:alpha:]][[:word:]-]*)+$
- ^(\/[[:alpha:]][[:word:]-]*)+\/\:[[:alpha:]][[:word:]-]*$
type: string

```

### PAGE_COMPONENT_SNIPPET

__Spec__

```yaml

items:
  fields:
  - name: name
    regex: ^[[:alpha:]][[:word:]-]*$
    type: string
  - name: component
    type: COMPONENT_REGEX
  - name: current-user
    optional: true
    type: boolean
  - name: data
    optional: true
    type: DATA_SNIPPET
  type: object
name: PAGE_COMPONENT_SNIPPET
path: helper-types
type: list

```

### PAGES_SNIPPET

__Spec__

```yaml

name: PAGES_SNIPPET
path: helper-types
type: variant
variants:
- fields:
  - name: default
    type: boolean
  type: object
- items:
    fields:
    - name: name
      type: NAME_BLACKLIST
    - name: route
      optional: true
      type: PAGE_ROUTE_REGEX
    - items:
        type: FILEPATH_REGEX
      name: style
      optional: true
      type: list
    - items:
        type: FILEPATH_REGEX
      name: content
      optional: true
      type: list
    - name: current-user
      optional: true
      type: boolean
    - name: data
      optional: true
      type: DATA_SNIPPET
    - name: components
      optional: true
      type: PAGE_COMPONENT_SNIPPET
    - name: translations
      optional: true
      type: I18N_SNIPPET
    - name: imports
      optional: true
      type: ignore
    type: object
  type: list

```
