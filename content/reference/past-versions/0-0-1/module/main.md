---
title: "main"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1
---

Fields:

- [name](#name)
- [types](#types)
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

### types

__Spec__

```yaml

items:
  fields:
  - name: name
    type: NAME_BLACKLIST
  - name: type
    type: TYPEPATH_REGEX
  type: object
name: types
type: list

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

