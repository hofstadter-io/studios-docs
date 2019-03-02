---
title: "helpers"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1000
---

Helpers:

- [AUTH_ROLE_REGEX](#auth-role-regex)
- [RELATION_TYPE_REGEX](#relation-type-regex)
- [OWNED_SNIPPET](#owned-snippet)

---

### AUTH_ROLE_REGEX

__Spec__

```yaml

name: AUTH_ROLE_REGEX
path: helper-types
regex: ^(user|admin)$
type: string

```

### RELATION_TYPE_REGEX

__Spec__

```yaml

name: RELATION_TYPE_REGEX
path: helper-types
regex: ^(one-to-one|one-to-many|many-to-many|belongs-to-one|belongs-to-many)$
type: string

```

### OWNED_SNIPPET

__Spec__

```yaml

fields:
- name: type
  regex: ^(has-one|has-many)$
  type: string
- name: name
  optional: true
  type: NAME_REGEX
- name: no-mutate
  optional: true
  type: boolean
- name: current-user-with
  optional: true
  type: boolean
name: OWNED_SNIPPET
path: helper-types
type: object

```

