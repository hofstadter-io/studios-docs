---
title: "main"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1
---

contents:

- [name](#name)
- [owned](#owned)
- [auth](#auth)
- [fields](#fields)
- [relations](#relations)
- [lookup](#lookup)
- [visibility](#visibility)
- [files](#files)
- [seeds](#seeds)
- [translations](#translations)
- [components](#components)
- [pages](#pages)

---

### name

__Spec__

```yaml

name: name
type: NAME_BLACKLIST

```

### owned

__Spec__

```yaml

name: owned
optional: true
type: OWNED_SNIPPET

```

### auth

__Spec__

```yaml

name: auth
type: variant
variants:
- fields:
  - name: default
    type: boolean
  type: object
- fields:
  - name: view
    type: variant
    variants:
    - items:
        type: AUTH_ROLE_REGEX
      type: list
    - fields:
      - items:
          type: AUTH_ROLE_REGEX
        name: public
        type: list
      - items:
          type: AUTH_ROLE_REGEX
        name: private
        type: list
      type: object
  - items:
      type: AUTH_ROLE_REGEX
    name: create
    type: list
  - items:
      type: AUTH_ROLE_REGEX
    name: update
    type: list
  - items:
      type: AUTH_ROLE_REGEX
    name: delete
    type: list
  type: object

```

### fields

__Spec__

```yaml

items:
  type: variant
  variants:
  - fields:
    - name: name
      type: NAME_REGEX
    - name: type
      regex: ^(string)
      type: string
    - name: default
      optional: true
      type: TEXT_REGEX
    - name: length
      optional: true
      type: integer
    - name: unique
      optional: true
      type: boolean
    - name: nullable
      optional: true
      type: boolean
    - name: notNullable
      optional: true
      type: boolean
    type: object
  - fields:
    - name: name
      type: NAME_REGEX
    - name: type
      regex: ^(text|integer|decimal|boolean|date|time|datetime|json|jsonb)
      type: string
    - name: default
      optional: true
      type: ignore
    - name: unique
      optional: true
      type: boolean
    - name: nullable
      optional: true
      type: boolean
    - name: notNullable
      optional: true
      type: boolean
    type: object
name: fields
type: list

```

### relations

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_BLACKLIST
  - name: type
    type: TYPEPATH_REGEX
  - name: relation
    type: RELATION_TYPE_REGEX
  type: object
name: relations
optional: true
type: list

```

### lookup

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_REGEX
  - name: field
    type: NAME_REGEX
  type: object
name: lookup
optional: true
type: list

```

### visibility

__Spec__

```yaml

name: visibility
optional: true
type: variant
variants:
- fields:
  - name: enabled
    type: boolean
  - name: default
    type: boolean
  type: object
- fields:
  - name: enabled
    type: boolean
  - name: default
    type: boolean
  - name: public
    type: NAME_REGEX
  - name: private
    type: NAME_REGEX
  type: object

```

### files

__Spec__

```yaml

name: files
optional: true
type: FILES_SNIPPET

```

### seeds

__Spec__

```yaml

name: seeds
optional: true
type: SEEDS_SNIPPET

```

### translations

__Spec__

```yaml

name: translations
optional: true
type: I18N_SNIPPET

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

