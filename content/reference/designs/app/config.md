---
title: "config"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 7
---

```yaml
ctx_path: dsl.0-0-1.app.docs.spec.fields.[7]
fields:
- ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[0]
  name: gaTracking
  parent: app.config
  parent_path: dsl.0-0-1.app.docs.spec.fields.[7]
  pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields
  pkgPath: app/config/gaTracking
  regex: ^UA-[[:digit:]]+-[[:digit:]]{2}
  type: string
- ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1]
  fields:
  - ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[0]
    name: picker
    optional: true
    parent: app.config.multilang
    parent_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1]
    pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields/[1]/fields
    pkgPath: app/config/multilang/picker
    type: boolean
  - ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[1]
    items:
      fields:
      - ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[1].items.fields.[0]
        name: short
        parent: app.config.multilang.languages
        parent_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[1]
        pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields/[1]/fields/[1]/items/fields
        pkgPath: app/config/multilang/languages/short
        regex: ^[[:alpha:]]+$
        type: string
      - ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[1].items.fields.[1]
        name: code
        parent: app.config.multilang.languages
        parent_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1].fields.[1]
        pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields/[1]/fields/[1]/items/fields
        pkgPath: app/config/multilang/languages/code
        regex: ^[[:word:]-]+$
        type: string
      type: object
    name: languages
    parent: app.config.multilang
    parent_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[1]
    pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields/[1]/fields
    pkgPath: app/config/multilang/languages
    type: list
  name: multilang
  parent: app.config
  parent_path: dsl.0-0-1.app.docs.spec.fields.[7]
  pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields
  pkgPath: app/config/multilang
  type: object
- ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[2]
  name: oauth
  optional: true
  parent: app.config
  parent_path: dsl.0-0-1.app.docs.spec.fields.[7]
  pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields
  pkgPath: app/config/oauth
  type: ignore
- ctx_path: dsl.0-0-1.app.docs.spec.fields.[7].fields.[3]
  name: mailer
  optional: true
  parent: app.config
  parent_path: dsl.0-0-1.app.docs.spec.fields.[7]
  pkg_path: 0-0-1/app/docs/spec/fields/[7]/fields
  pkgPath: app/config/mailer
  type: ignore
name: config
own-file: true
parent: app
parent_path: dsl.0-0-1.app.docs
pkg_path: 0-0-1/app/docs/spec/fields
pkgPath: app/config
type: object

```

