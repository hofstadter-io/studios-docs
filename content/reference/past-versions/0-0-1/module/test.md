ctx_path: dsl.0-0-1.module.docs
intro: Docs for module
name: module
parent: ""
parent_path: ""
pkg_path: 0-0-1/module
pkgPath: module
relPath: 0-0-1/module
spec:
  fields:
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[0]
    name: forms
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/forms
    type: ignore
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[1]
    name: name
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/name
    type: NAME_BLACKLIST
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[2]
    items:
      fields:
      - ctx_path: dsl.0-0-1.module.docs.spec.fields.[2].items.fields.[0]
        name: name
        parent: module.types
        parent_path: dsl.0-0-1.module.docs.spec.fields.[2]
        pkg_path: 0-0-1/module/docs/spec/fields/[2]/items/fields
        pkgPath: module/types/name
        type: NAME_BLACKLIST
      - ctx_path: dsl.0-0-1.module.docs.spec.fields.[2].items.fields.[1]
        name: type
        parent: module.types
        parent_path: dsl.0-0-1.module.docs.spec.fields.[2]
        pkg_path: 0-0-1/module/docs/spec/fields/[2]/items/fields
        pkgPath: module/types/type
        type: TYPEPATH_REGEX
      type: object
    name: types
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/types
    type: list
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[3]
    name: files
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/files
    type: FILES_SNIPPET
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[4]
    name: seeds
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/seeds
    type: SEEDS_SNIPPET
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[5]
    name: translations
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/translations
    type: I18N_SNIPPET
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[6]
    name: components
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/components
    type: COMPONENT_SNIPPET
  - ctx_path: dsl.0-0-1.module.docs.spec.fields.[7]
    name: pages
    optional: true
    parent: module
    parent_path: dsl.0-0-1.module.docs
    pkg_path: 0-0-1/module/docs/spec/fields
    pkgPath: module/pages
    type: PAGES_SNIPPET
  parent: module
  path: spec
  type: object
version: 0.0.1

