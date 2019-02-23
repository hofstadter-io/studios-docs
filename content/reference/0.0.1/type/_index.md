---
title: "type"
type: page
---

Docs for type

## Fields

### hooks

#### Type

ignore

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[0]
name: hooks
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/hooks
type: ignore

```

### name

#### Type

NAME_BLACKLIST

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[1]
name: name
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/name
type: NAME_BLACKLIST

```

### owned

#### Type

OWNED_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[2]
name: owned
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/owned
type: OWNED_SNIPPET

```

### auth

#### Type

variant

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[3]
name: auth
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/auth
type: variant
variants:
- fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[0].fields.[0]
    name: default
    parent: type.auth
    parent_path: dsl.0.0.1.type.docs.spec.fields.[3]
    pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[0]/fields
    pkgPath: type/auth/default
    type: boolean
  type: object
- fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[0]
    name: view
    parent: type.auth
    parent_path: dsl.0.0.1.type.docs.spec.fields.[3]
    pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields
    pkgPath: type/auth/view
    type: variant
    variants:
    - items:
        type: AUTH_ROLE_REGEX
      type: list
    - fields:
      - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[0].variants.[1].fields.[0]
        items:
          type: AUTH_ROLE_REGEX
        name: public
        parent: type.auth.view
        parent_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[0]
        pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields/[0]/variants/[1]/fields
        pkgPath: type/auth/view/public
        type: list
      - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[0].variants.[1].fields.[1]
        items:
          type: AUTH_ROLE_REGEX
        name: private
        parent: type.auth.view
        parent_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[0]
        pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields/[0]/variants/[1]/fields
        pkgPath: type/auth/view/private
        type: list
      type: object
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[1]
    items:
      type: AUTH_ROLE_REGEX
    name: create
    parent: type.auth
    parent_path: dsl.0.0.1.type.docs.spec.fields.[3]
    pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields
    pkgPath: type/auth/create
    type: list
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[2]
    items:
      type: AUTH_ROLE_REGEX
    name: update
    parent: type.auth
    parent_path: dsl.0.0.1.type.docs.spec.fields.[3]
    pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields
    pkgPath: type/auth/update
    type: list
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[3].variants.[1].fields.[3]
    items:
      type: AUTH_ROLE_REGEX
    name: delete
    parent: type.auth
    parent_path: dsl.0.0.1.type.docs.spec.fields.[3]
    pkg_path: 0/0/1/type/docs/spec/fields/[3]/variants/[1]/fields
    pkgPath: type/auth/delete
    type: list
  type: object

```

### fields

#### Type

list

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[4]
items:
  type: variant
  variants:
  - fields:
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[0]
      name: name
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/name
      type: NAME_REGEX
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[1]
      name: type
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/type
      regex: ^(string)
      type: string
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[2]
      name: default
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/default
      type: TEXT_REGEX
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[3]
      name: length
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/length
      type: integer
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[4]
      name: unique
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/unique
      type: boolean
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[5]
      name: nullable
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/nullable
      type: boolean
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[0].fields.[6]
      name: notNullable
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[0]/fields
      pkgPath: type/fields/notNullable
      type: boolean
    type: object
  - fields:
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[0]
      name: name
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/name
      type: NAME_REGEX
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[1]
      name: type
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/type
      regex: ^(text|integer|decimal|boolean|date|time|datetime|json|jsonb)
      type: string
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[2]
      name: default
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/default
      type: ignore
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[3]
      name: unique
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/unique
      type: boolean
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[4]
      name: nullable
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/nullable
      type: boolean
    - ctx_path: dsl.0.0.1.type.docs.spec.fields.[4].items.variants.[1].fields.[5]
      name: notNullable
      optional: true
      parent: type.fields
      parent_path: dsl.0.0.1.type.docs.spec.fields.[4]
      pkg_path: 0/0/1/type/docs/spec/fields/[4]/items/variants/[1]/fields
      pkgPath: type/fields/notNullable
      type: boolean
    type: object
name: fields
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/fields
type: list

```

### relations

#### Type

list

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[5]
items:
  fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[5].items.fields.[0]
    name: name
    parent: type.relations
    parent_path: dsl.0.0.1.type.docs.spec.fields.[5]
    pkg_path: 0/0/1/type/docs/spec/fields/[5]/items/fields
    pkgPath: type/relations/name
    type: NAME_BLACKLIST
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[5].items.fields.[1]
    name: type
    parent: type.relations
    parent_path: dsl.0.0.1.type.docs.spec.fields.[5]
    pkg_path: 0/0/1/type/docs/spec/fields/[5]/items/fields
    pkgPath: type/relations/type
    type: TYPEPATH_REGEX
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[5].items.fields.[2]
    name: relation
    parent: type.relations
    parent_path: dsl.0.0.1.type.docs.spec.fields.[5]
    pkg_path: 0/0/1/type/docs/spec/fields/[5]/items/fields
    pkgPath: type/relations/relation
    type: RELATION_TYPE_REGEX
  type: object
name: relations
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/relations
type: list

```

### lookup

#### Type

list

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[6]
items:
  fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[6].items.fields.[0]
    name: name
    parent: type.lookup
    parent_path: dsl.0.0.1.type.docs.spec.fields.[6]
    pkg_path: 0/0/1/type/docs/spec/fields/[6]/items/fields
    pkgPath: type/lookup/name
    type: NAME_REGEX
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[6].items.fields.[1]
    name: field
    parent: type.lookup
    parent_path: dsl.0.0.1.type.docs.spec.fields.[6]
    pkg_path: 0/0/1/type/docs/spec/fields/[6]/items/fields
    pkgPath: type/lookup/field
    type: NAME_REGEX
  type: object
name: lookup
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/lookup
type: list

```

### visibility

#### Type

variant

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[7]
name: visibility
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/visibility
type: variant
variants:
- fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[0].fields.[0]
    name: enabled
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[0]/fields
    pkgPath: type/visibility/enabled
    type: boolean
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[0].fields.[1]
    name: default
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[0]/fields
    pkgPath: type/visibility/default
    type: boolean
  type: object
- fields:
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[1].fields.[0]
    name: enabled
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[1]/fields
    pkgPath: type/visibility/enabled
    type: boolean
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[1].fields.[1]
    name: default
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[1]/fields
    pkgPath: type/visibility/default
    type: boolean
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[1].fields.[2]
    name: public
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[1]/fields
    pkgPath: type/visibility/public
    type: NAME_REGEX
  - ctx_path: dsl.0.0.1.type.docs.spec.fields.[7].variants.[1].fields.[3]
    name: private
    parent: type.visibility
    parent_path: dsl.0.0.1.type.docs.spec.fields.[7]
    pkg_path: 0/0/1/type/docs/spec/fields/[7]/variants/[1]/fields
    pkgPath: type/visibility/private
    type: NAME_REGEX
  type: object

```

### files

#### Type

FILES_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[8]
name: files
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/files
type: FILES_SNIPPET

```

### seeds

#### Type

SEEDS_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[9]
name: seeds
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/seeds
type: SEEDS_SNIPPET

```

### translations

#### Type

I18N_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[10]
name: translations
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/translations
type: I18N_SNIPPET

```

### components

#### Type

COMPONENT_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[11]
name: components
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/components
type: COMPONENT_SNIPPET

```

### pages

#### Type

PAGES_SNIPPET

#### Source

```yaml
ctx_path: dsl.0.0.1.type.docs.spec.fields.[12]
name: pages
optional: true
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/spec/fields
pkgPath: type/pages
type: PAGES_SNIPPET

```

## Helper types

### AUTH_ROLE_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.type.docs.helper-types.[0]
name: AUTH_ROLE_REGEX
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/helper-types
pkgPath: type/AUTH_ROLE_REGEX
regex: ^(user|admin)$
type: string

```

### RELATION_TYPE_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.type.docs.helper-types.[1]
name: RELATION_TYPE_REGEX
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/helper-types
pkgPath: type/RELATION_TYPE_REGEX
regex: ^(one-to-one|one-to-many|many-to-many|belongs-to-one|belongs-to-many)$
type: string

```

### OWNED_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.type.docs.helper-types.[2]
fields:
- ctx_path: dsl.0.0.1.type.docs.helper-types.[2].fields.[0]
  name: type
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0.0.1.type.docs.helper-types.[2]
  pkg_path: 0/0/1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/type
  regex: ^(has-one|has-many)$
  type: string
- ctx_path: dsl.0.0.1.type.docs.helper-types.[2].fields.[1]
  name: name
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0.0.1.type.docs.helper-types.[2]
  pkg_path: 0/0/1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/name
  type: NAME_REGEX
- ctx_path: dsl.0.0.1.type.docs.helper-types.[2].fields.[2]
  name: no-mutate
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0.0.1.type.docs.helper-types.[2]
  pkg_path: 0/0/1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/no-mutate
  type: boolean
- ctx_path: dsl.0.0.1.type.docs.helper-types.[2].fields.[3]
  name: current-user-with
  optional: true
  parent: type.OWNED_SNIPPET
  parent_path: dsl.0.0.1.type.docs.helper-types.[2]
  pkg_path: 0/0/1/type/docs/helper-types/[2]/fields
  pkgPath: type/OWNED_SNIPPET/current-user-with
  type: boolean
name: OWNED_SNIPPET
parent: type
parent_path: dsl.0.0.1.type.docs
pkg_path: 0/0/1/type/docs/helper-types
pkgPath: type/OWNED_SNIPPET
type: object

```

