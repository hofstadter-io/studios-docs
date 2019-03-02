---
title: "config"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 7
---

- [gaTracking](#gaTracking)
- [multilang](#multilang)

---

### gaTracking

__Spec__

```yaml

name: gaTracking
regex: ^UA-[[:digit:]]+-[[:digit:]]{2}
type: string

```

### multilang

__Spec__

```yaml

fields:
- name: picker
  optional: true
  type: boolean
- items:
    fields:
    - name: short
      regex: ^[[:alpha:]]+$
      type: string
    - name: code
      regex: ^[[:word:]-]+$
      type: string
    type: object
  name: languages
  type: list
name: multilang
type: object

```

