---
title: "main"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1
---

Fields:

- [name](#name)
- [title](#title)
- [version](#version)
- [author](#author)
- [license](#license)
- [keywords](#keywords)
- [modules](#modules)
- [user](#user)
- [auth](#auth)
- [imports](#imports)
- [components](#components)
- [pages](#pages)

---

### name

__Spec__

```yaml

name: name
type: APP_NAME_BLACKLIST

```

__Example__

my app

### title

__Spec__

```yaml

name: title
type: TEXT_REGEX

```

### version

__Spec__

```yaml

name: version
type: SEMVER_REGEX

```

### author

__Spec__

```yaml

name: author
type: AUTHOR_REGEX

```

### license

__Spec__

```yaml

name: license
type: TEXT_REGEX

```

### keywords

__Spec__

```yaml

items:
  type: TEXT_REGEX
name: keywords
type: list

```

### modules

__Spec__

```yaml

items:
  type: NAME_REGEX
name: modules
type: list

```

### user

__Spec__

```yaml

fields:
- name: translations
  optional: true
  type: I18N_SNIPPET
- name: hooks
  optional: true
  type: ignore
name: user
type: object

```

### auth

__Spec__

```yaml

fields:
- fields:
  - name: enabled
    type: boolean
  name: password
  type: object
- fields:
  - name: enabled
    type: boolean
  name: apikey
  type: object
- fields:
  - name: google
    optional: true
    type: boolean
  - name: facebook
    optional: true
    type: boolean
  - name: linkedin
    optional: true
    type: boolean
  - name: github
    optional: true
    type: boolean
  name: oauth
  type: object
- fields:
  - name: disabled
    type: boolean
  name: registration
  optional: true
  type: object
name: auth
type: object

```

### imports

__Spec__

```yaml

items:
  fields:
  - name: library
    type: NPM_IMPORT_REGEX
  - name: version
    type: NPM_VERSION_REGEX
  type: object
name: imports
optional: true
type: list

```

### components

__Spec__

```yaml

name: components
optional: true
type: COMPONENT_SNIPPET

```

### pages

__Spec__

```yaml

name: pages
optional: true
type: PAGES_SNIPPET

```

