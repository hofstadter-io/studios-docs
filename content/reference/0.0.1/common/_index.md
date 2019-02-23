---
title: "common"
type: page
---

Docs for common

## Fields

## Helper types

### SEMVER_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[0]
name: SEMVER_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/SEMVER_REGEX
regex: ^[[:digit:]]+\.[[:digit:]]+\.[[:digit:]]+$
type: string

```

### NAME_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[1]
name: NAME_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/NAME_REGEX
regex: ^[[:alpha:]][[:word:]-]*$
type: string

```

### TEXT_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[2]
name: TEXT_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/TEXT_REGEX
regex: ^[[:alpha:]][[:word:] -]*$
type: string

```

### NAME_BLACKLIST

#### spec

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
ctx_path: dsl.0.0.1.common.docs.helper-types.[3]
name: NAME_BLACKLIST
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/NAME_BLACKLIST
type: NAME_REGEX

```

### SEEDFILE_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[4]
lookup-file: true
name: SEEDFILE_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/SEEDFILE_REGEX
regex: ^([[:word:]-]+\/)+[[:word:]-]+\.json$
type: string

```

### SEEDS_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[5]
fields:
- ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[0]
  name: file
  parent: common.SEEDS_SNIPPET
  parent_path: dsl.0.0.1.common.docs.helper-types.[5]
  pkg_path: 0/0/1/common/docs/helper-types/[5]/fields
  pkgPath: common/SEEDS_SNIPPET/file
  type: SEEDFILE_REGEX
- ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1]
  items:
    fields:
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1].items.fields.[0]
      name: name
      parent: common.SEEDS_SNIPPET.types
      parent_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1]
      pkg_path: 0/0/1/common/docs/helper-types/[5]/fields/[1]/items/fields
      pkgPath: common/SEEDS_SNIPPET/types/name
      type: NAME_BLACKLIST
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1].items.fields.[1]
      name: data
      parent: common.SEEDS_SNIPPET.types
      parent_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1]
      pkg_path: 0/0/1/common/docs/helper-types/[5]/fields/[1]/items/fields
      pkgPath: common/SEEDS_SNIPPET/types/data
      type: NAME_REGEX
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1].items.fields.[2]
      name: type
      parent: common.SEEDS_SNIPPET.types
      parent_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1]
      pkg_path: 0/0/1/common/docs/helper-types/[5]/fields/[1]/items/fields
      pkgPath: common/SEEDS_SNIPPET/types/type
      type: TYPEPATH_REGEX
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1].items.fields.[3]
      name: lookup
      optional: true
      parent: common.SEEDS_SNIPPET.types
      parent_path: dsl.0.0.1.common.docs.helper-types.[5].fields.[1]
      pkg_path: 0/0/1/common/docs/helper-types/[5]/fields/[1]/items/fields
      pkgPath: common/SEEDS_SNIPPET/types/lookup
      type: ignore
    type: object
  name: types
  parent: common.SEEDS_SNIPPET
  parent_path: dsl.0.0.1.common.docs.helper-types.[5]
  pkg_path: 0/0/1/common/docs/helper-types/[5]/fields
  pkgPath: common/SEEDS_SNIPPET/types
  type: list
name: SEEDS_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/SEEDS_SNIPPET
type: object

```

### I18NFILE_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[6]
lookup-file: true
name: I18NFILE_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/I18NFILE_REGEX
regex: ^([[:word:]-]+\/)+[[:word:]-]+\.json$
type: string

```

### I18N_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[7]
items:
  fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[7].items.fields.[0]
    name: name
    parent: common.I18N_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[7]
    pkg_path: 0/0/1/common/docs/helper-types/[7]/items/fields
    pkgPath: common/I18N_SNIPPET/name
    type: NAME_REGEX
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[7].items.fields.[1]
    name: file
    parent: common.I18N_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[7]
    pkg_path: 0/0/1/common/docs/helper-types/[7]/items/fields
    pkgPath: common/I18N_SNIPPET/file
    type: I18NFILE_REGEX
  type: object
name: I18N_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/I18N_SNIPPET
type: list

```

### FILEPATH_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[8]
lookup-file: true
name: FILEPATH_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/FILEPATH_REGEX
regex: ^(design|custom|pages|seeds|translations)\/([[:word:]-]+\/)+[[:word:]-]+\.[[:lower:]]{1,4}$
type: string

```

### FILES_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[9]
items:
  fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[9].items.fields.[0]
    name: name
    parent: common.FILES_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[9]
    pkg_path: 0/0/1/common/docs/helper-types/[9]/items/fields
    pkgPath: common/FILES_SNIPPET/name
    type: NAME_BLACKLIST
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[9].items.fields.[1]
    name: src
    parent: common.FILES_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[9]
    pkg_path: 0/0/1/common/docs/helper-types/[9]/items/fields
    pkgPath: common/FILES_SNIPPET/src
    type: FILEPATH_REGEX
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[9].items.fields.[2]
    name: dst
    parent: common.FILES_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[9]
    pkg_path: 0/0/1/common/docs/helper-types/[9]/items/fields
    pkgPath: common/FILES_SNIPPET/dst
    type: FILEPATH_REGEX
  type: object
name: FILES_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/FILES_SNIPPET
type: list

```

### TYPEPATH_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[10]
lookup-design: true
name: TYPEPATH_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/TYPEPATH_REGEX
regex: ^type\.modules\.[[:word:]-]+\.[[:word:]-]+$
type: string

```

### COMPONENT_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[11]
lookup-design: true
name: COMPONENT_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/COMPONENT_REGEX
regex: ^(type|module)\.modules\.([[:word:]-]+\.){1,2}components\.[[:word:]-]+$
type: string

```

### DATA_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[12]
items:
  fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[0]
    name: name
    parent: common.DATA_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[12]
    pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields
    pkgPath: common/DATA_SNIPPET/name
    type: NAME_BLACKLIST
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[1]
    name: type
    parent: common.DATA_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[12]
    pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields
    pkgPath: common/DATA_SNIPPET/type
    type: TYPEPATH_REGEX
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2]
    fields:
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2].fields.[0]
      name: type
      parent: common.DATA_SNIPPET.query
      parent_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2]
      pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields/[2]/fields
      pkgPath: common/DATA_SNIPPET/query/type
      regex: ^(view|list)$
      type: string
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2].fields.[1]
      name: sync
      optional: true
      parent: common.DATA_SNIPPET.query
      parent_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2]
      pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields/[2]/fields
      pkgPath: common/DATA_SNIPPET/query/sync
      type: boolean
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2].fields.[2]
      name: filter
      optional: true
      parent: common.DATA_SNIPPET.query
      parent_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2]
      pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields/[2]/fields
      pkgPath: common/DATA_SNIPPET/query/filter
      type: ignore
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2].fields.[3]
      name: variables
      optional: true
      parent: common.DATA_SNIPPET.query
      parent_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[2]
      pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields/[2]/fields
      pkgPath: common/DATA_SNIPPET/query/variables
      type: ignore
    name: query
    optional: true
    parent: common.DATA_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[12]
    pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields
    pkgPath: common/DATA_SNIPPET/query
    type: object
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[12].items.fields.[3]
    items:
      regex: ^(create|update|delete)$
      type: string
    name: mutations
    optional: true
    parent: common.DATA_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[12]
    pkg_path: 0/0/1/common/docs/helper-types/[12]/items/fields
    pkgPath: common/DATA_SNIPPET/mutations
    type: list
  type: object
name: DATA_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/DATA_SNIPPET
type: list

```

### COMPONENT_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[13]
name: COMPONENT_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/COMPONENT_SNIPPET
type: variant
variants:
- fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[0].fields.[0]
    name: default
    parent: common.COMPONENT_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[13]
    pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[0]/fields
    pkgPath: common/COMPONENT_SNIPPET/default
    type: boolean
  type: object
- items:
    fields:
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[1].items.fields.[0]
      name: name
      parent: common.COMPONENT_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[13]
      pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[1]/items/fields
      pkgPath: common/COMPONENT_SNIPPET/name
      type: NAME_BLACKLIST
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[1].items.fields.[1]
      items:
        type: FILEPATH_REGEX
      name: style
      optional: true
      parent: common.COMPONENT_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[13]
      pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[1]/items/fields
      pkgPath: common/COMPONENT_SNIPPET/style
      type: list
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[1].items.fields.[2]
      items:
        type: FILEPATH_REGEX
      name: content
      optional: true
      parent: common.COMPONENT_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[13]
      pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[1]/items/fields
      pkgPath: common/COMPONENT_SNIPPET/content
      type: list
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[1].items.fields.[3]
      name: current-user
      optional: true
      parent: common.COMPONENT_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[13]
      pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[1]/items/fields
      pkgPath: common/COMPONENT_SNIPPET/current-user
      type: boolean
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[13].variants.[1].items.fields.[4]
      name: data
      optional: true
      parent: common.COMPONENT_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[13]
      pkg_path: 0/0/1/common/docs/helper-types/[13]/variants/[1]/items/fields
      pkgPath: common/COMPONENT_SNIPPET/data
      type: DATA_SNIPPET
    type: object
  type: list

```

### PAGE_ROUTE_REGEX

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[14]
name: PAGE_ROUTE_REGEX
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/PAGE_ROUTE_REGEX
regex:
- ^\/$
- ^(\/[[:alpha:]][[:word:]-]*)+$
- ^(\/[[:alpha:]][[:word:]-]*)+\/\:[[:alpha:]][[:word:]-]*$
type: string

```

### PAGE_COMPONENT_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[15]
items:
  fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[15].items.fields.[0]
    name: name
    parent: common.PAGE_COMPONENT_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[15]
    pkg_path: 0/0/1/common/docs/helper-types/[15]/items/fields
    pkgPath: common/PAGE_COMPONENT_SNIPPET/name
    regex: ^[[:alpha:]][[:word:]-]*$
    type: string
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[15].items.fields.[1]
    name: component
    parent: common.PAGE_COMPONENT_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[15]
    pkg_path: 0/0/1/common/docs/helper-types/[15]/items/fields
    pkgPath: common/PAGE_COMPONENT_SNIPPET/component
    type: COMPONENT_REGEX
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[15].items.fields.[2]
    name: current-user
    optional: true
    parent: common.PAGE_COMPONENT_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[15]
    pkg_path: 0/0/1/common/docs/helper-types/[15]/items/fields
    pkgPath: common/PAGE_COMPONENT_SNIPPET/current-user
    type: boolean
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[15].items.fields.[3]
    name: data
    optional: true
    parent: common.PAGE_COMPONENT_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[15]
    pkg_path: 0/0/1/common/docs/helper-types/[15]/items/fields
    pkgPath: common/PAGE_COMPONENT_SNIPPET/data
    type: DATA_SNIPPET
  type: object
name: PAGE_COMPONENT_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/PAGE_COMPONENT_SNIPPET
type: list

```

### PAGES_SNIPPET

#### spec

```yaml
ctx_path: dsl.0.0.1.common.docs.helper-types.[16]
name: PAGES_SNIPPET
parent: common
parent_path: dsl.0.0.1.common.docs
pkg_path: 0/0/1/common/docs/helper-types
pkgPath: common/PAGES_SNIPPET
type: variant
variants:
- fields:
  - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[0].fields.[0]
    name: default
    parent: common.PAGES_SNIPPET
    parent_path: dsl.0.0.1.common.docs.helper-types.[16]
    pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[0]/fields
    pkgPath: common/PAGES_SNIPPET/default
    type: boolean
  type: object
- items:
    fields:
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[0]
      name: name
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/name
      type: NAME_BLACKLIST
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[1]
      name: route
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/route
      type: PAGE_ROUTE_REGEX
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[2]
      items:
        type: FILEPATH_REGEX
      name: style
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/style
      type: list
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[3]
      items:
        type: FILEPATH_REGEX
      name: content
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/content
      type: list
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[4]
      name: current-user
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/current-user
      type: boolean
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[5]
      name: data
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/data
      type: DATA_SNIPPET
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[6]
      name: components
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/components
      type: PAGE_COMPONENT_SNIPPET
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[7]
      name: translations
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/translations
      type: I18N_SNIPPET
    - ctx_path: dsl.0.0.1.common.docs.helper-types.[16].variants.[1].items.fields.[8]
      name: imports
      optional: true
      parent: common.PAGES_SNIPPET
      parent_path: dsl.0.0.1.common.docs.helper-types.[16]
      pkg_path: 0/0/1/common/docs/helper-types/[16]/variants/[1]/items/fields
      pkgPath: common/PAGES_SNIPPET/imports
      type: ignore
    type: object
  type: list

```

