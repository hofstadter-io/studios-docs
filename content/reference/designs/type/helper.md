---
title: "helpers"
date: 2018-04-10T11:58:26-06:00
draft: false
type: "page"

weight: 1000
---

### AUTH_ROLE_REGEX

#### spec

```yaml
ctx_path: dsl.0-0-1.type.docs.helper-types.[0]
name: AUTH_ROLE_REGEX
parent: type
parent_path: dsl.0-0-1.type.docs
path: helper-types
pkg_path: 0-0-1/type/docs/helper-types
pkgPath: type/AUTH_ROLE_REGEX
regex: ^(user|admin)$
type: string

```

### RELATION_TYPE_REGEX

#### spec

```yaml
ctx_path: dsl.0-0-1.type.docs.helper-types.[1]
name: RELATION_TYPE_REGEX
parent: type
parent_path: dsl.0-0-1.type.docs
path: helper-types
pkg_path: 0-0-1/type/docs/helper-types
pkgPath: type/RELATION_TYPE_REGEX
regex: ^(one-to-one|one-to-many|many-to-many|belongs-to-one|belongs-to-many)$
type: string

```

### OWNED_SNIPPET

#### spec

```yaml
ctx_path: dsl.0-0-1.type.docs.helper-types.[2]
fields:
- ctx_path: dsl.0-0-1.type.docs.helper-types.[2].fields.[0]
  name: type
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0-0-1.type.docs.helper-types.[2]
  pkg_path: 0-0-1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/type
  regex: ^(has-one|has-many)$
  type: string
- ctx_path: dsl.0-0-1.type.docs.helper-types.[2].fields.[1]
  name: name
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0-0-1.type.docs.helper-types.[2]
  pkg_path: 0-0-1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/name
  type: NAME_REGEX
- ctx_path: dsl.0-0-1.type.docs.helper-types.[2].fields.[2]
  name: no-mutate
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0-0-1.type.docs.helper-types.[2]
  pkg_path: 0-0-1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/no-mutate
  type: boolean
- ctx_path: dsl.0-0-1.type.docs.helper-types.[2].fields.[3]
  name: current-user-with
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0-0-1.type.docs.helper-types.[2]
  pkg_path: 0-0-1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/current-user-with
  type: boolean
name: OWNED_SNIPPET
parent: type
parent_path: dsl.0-0-1.type.docs
path: helper-types
pkg_path: 0-0-1/type/docs/helper-types
pkgPath: type/OWNED_SNIPPET
type: object

```

