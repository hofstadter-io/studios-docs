ctx_path: dsl.0.0.1.app.docs
helper-types:
- blacklist:
  - hof
  - hofstadter
  ctx_path: dsl.0.0.1.app.docs.helper-types.[0]
  name: APP_NAME_BLACKLIST
  parent: app
  parent_path: dsl.0.0.1.app.docs
  pkg_path: 0/0/1/app/docs/helper-types
  pkgPath: app/APP_NAME_BLACKLIST
  type: NAME_REGEX
- ctx_path: dsl.0.0.1.app.docs.helper-types.[1]
  name: AUTHOR_REGEX
  parent: app
  parent_path: dsl.0.0.1.app.docs
  pkg_path: 0/0/1/app/docs/helper-types
  pkgPath: app/AUTHOR_REGEX
  regex: ^[[:alpha:]][[:word:] -\<\>\@\.]*$
  type: string
- ctx_path: dsl.0.0.1.app.docs.helper-types.[2]
  name: NPM_IMPORT_REGEX
  parent: app
  parent_path: dsl.0.0.1.app.docs
  pkg_path: 0/0/1/app/docs/helper-types
  pkgPath: app/NPM_IMPORT_REGEX
  regex: ^[[:alpha:]][[:word:]-]*$
  type: string
- ctx_path: dsl.0.0.1.app.docs.helper-types.[3]
  name: NPM_VERSION_REGEX
  parent: app
  parent_path: dsl.0.0.1.app.docs
  pkg_path: 0/0/1/app/docs/helper-types
  pkgPath: app/NPM_VERSION_REGEX
  regex:
  - ^[\~\^]?[[:digit:]]+\.[[:digit:]]+\.[[:digit:]]+$
  - ^[\~\^]?[[:digit:]]+\.[[:digit:]]+$
  - ^[\~\^]?[[:digit:]]+$
  type: string
intro: Docs for app
name: app
parent: ""
parent_path: ""
pkg_path: 0/0/1/app
pkgPath: app
relPath: 0.0.1/app
spec:
  fields:
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[0]
    example: my app
    name: name
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/name
    type: APP_NAME_BLACKLIST
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[1]
    name: title
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/title
    type: TEXT_REGEX
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[2]
    name: version
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/version
    type: SEMVER_REGEX
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[3]
    name: author
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/author
    type: AUTHOR_REGEX
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[4]
    name: license
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/license
    type: TEXT_REGEX
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[5]
    items:
      type: TEXT_REGEX
    name: keywords
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/keywords
    type: list
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[6]
    items:
      type: NAME_REGEX
    name: modules
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/modules
    type: list
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7]
    fields:
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[0]
      name: gaTracking
      parent: app.config
      parent_path: dsl.0.0.1.app.docs.spec.fields.[7]
      pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields
      pkgPath: app/config/gaTracking
      regex: ^UA-[[:digit:]]+-[[:digit:]]{2}
      type: string
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1]
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[0]
        name: picker
        optional: true
        parent: app.config.multilang
        parent_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1]
        pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields/[1]/fields
        pkgPath: app/config/multilang/picker
        type: boolean
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[1]
        items:
          fields:
          - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[1].items.fields.[0]
            name: short
            parent: app.config.multilang.languages
            parent_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[1]
            pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields/[1]/fields/[1]/items/fields
            pkgPath: app/config/multilang/languages/short
            regex: ^[[:alpha:]]+$
            type: string
          - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[1].items.fields.[1]
            name: code
            parent: app.config.multilang.languages
            parent_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1].fields.[1]
            pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields/[1]/fields/[1]/items/fields
            pkgPath: app/config/multilang/languages/code
            regex: ^[[:word:]-]+$
            type: string
          type: object
        name: languages
        parent: app.config.multilang
        parent_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[1]
        pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields/[1]/fields
        pkgPath: app/config/multilang/languages
        type: list
      name: multilang
      parent: app.config
      parent_path: dsl.0.0.1.app.docs.spec.fields.[7]
      pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields
      pkgPath: app/config/multilang
      type: object
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[2]
      name: oauth
      optional: true
      parent: app.config
      parent_path: dsl.0.0.1.app.docs.spec.fields.[7]
      pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields
      pkgPath: app/config/oauth
      type: ignore
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[7].fields.[3]
      name: mailer
      optional: true
      parent: app.config
      parent_path: dsl.0.0.1.app.docs.spec.fields.[7]
      pkg_path: 0/0/1/app/docs/spec/fields/[7]/fields
      pkgPath: app/config/mailer
      type: ignore
    name: config
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/config
    type: object
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[8]
    fields:
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[8].fields.[0]
      name: translations
      optional: true
      parent: app.user
      parent_path: dsl.0.0.1.app.docs.spec.fields.[8]
      pkg_path: 0/0/1/app/docs/spec/fields/[8]/fields
      pkgPath: app/user/translations
      type: I18N_SNIPPET
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[8].fields.[1]
      name: hooks
      optional: true
      parent: app.user
      parent_path: dsl.0.0.1.app.docs.spec.fields.[8]
      pkg_path: 0/0/1/app/docs/spec/fields/[8]/fields
      pkgPath: app/user/hooks
      type: ignore
    name: user
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/user
    type: object
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9]
    fields:
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[0]
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[0].fields.[0]
        name: enabled
        parent: app.auth.password
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[0]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[0]/fields
        pkgPath: app/auth/password/enabled
        type: boolean
      name: password
      parent: app.auth
      parent_path: dsl.0.0.1.app.docs.spec.fields.[9]
      pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields
      pkgPath: app/auth/password
      type: object
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[1]
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[1].fields.[0]
        name: enabled
        parent: app.auth.apikey
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[1]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[1]/fields
        pkgPath: app/auth/apikey/enabled
        type: boolean
      name: apikey
      parent: app.auth
      parent_path: dsl.0.0.1.app.docs.spec.fields.[9]
      pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields
      pkgPath: app/auth/apikey
      type: object
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2]
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2].fields.[0]
        name: google
        optional: true
        parent: app.auth.oauth
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[2]/fields
        pkgPath: app/auth/oauth/google
        type: boolean
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2].fields.[1]
        name: facebook
        optional: true
        parent: app.auth.oauth
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[2]/fields
        pkgPath: app/auth/oauth/facebook
        type: boolean
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2].fields.[2]
        name: linkedin
        optional: true
        parent: app.auth.oauth
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[2]/fields
        pkgPath: app/auth/oauth/linkedin
        type: boolean
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2].fields.[3]
        name: github
        optional: true
        parent: app.auth.oauth
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[2]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[2]/fields
        pkgPath: app/auth/oauth/github
        type: boolean
      name: oauth
      parent: app.auth
      parent_path: dsl.0.0.1.app.docs.spec.fields.[9]
      pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields
      pkgPath: app/auth/oauth
      type: object
    - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[3]
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[3].fields.[0]
        name: disabled
        parent: app.auth.registration
        parent_path: dsl.0.0.1.app.docs.spec.fields.[9].fields.[3]
        pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields/[3]/fields
        pkgPath: app/auth/registration/disabled
        type: boolean
      name: registration
      optional: true
      parent: app.auth
      parent_path: dsl.0.0.1.app.docs.spec.fields.[9]
      pkg_path: 0/0/1/app/docs/spec/fields/[9]/fields
      pkgPath: app/auth/registration
      type: object
    name: auth
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/auth
    type: object
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[10]
    items:
      fields:
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[10].items.fields.[0]
        name: library
        parent: app.imports
        parent_path: dsl.0.0.1.app.docs.spec.fields.[10]
        pkg_path: 0/0/1/app/docs/spec/fields/[10]/items/fields
        pkgPath: app/imports/library
        type: NPM_IMPORT_REGEX
      - ctx_path: dsl.0.0.1.app.docs.spec.fields.[10].items.fields.[1]
        name: version
        parent: app.imports
        parent_path: dsl.0.0.1.app.docs.spec.fields.[10]
        pkg_path: 0/0/1/app/docs/spec/fields/[10]/items/fields
        pkgPath: app/imports/version
        type: NPM_VERSION_REGEX
      type: object
    name: imports
    optional: true
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/imports
    type: list
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[11]
    name: components
    optional: true
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/components
    type: COMPONENT_SNIPPET
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[12]
    name: pages
    optional: true
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/pages
    type: PAGES_SNIPPET
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[13]
    name: secrets
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/secrets
    type: ignore
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[14]
    name: homepage
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/homepage
    type: ignore
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[15]
    name: layout
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/layout
    type: ignore
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[16]
    name: builtin-pages
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/builtin-pages
    type: ignore
  - ctx_path: dsl.0.0.1.app.docs.spec.fields.[17]
    name: hof-223--proxy-endpoints
    optional: true
    parent: app
    parent_path: dsl.0.0.1.app.docs
    pkg_path: 0/0/1/app/docs/spec/fields
    pkgPath: app/hof-223--proxy-endpoints
    type: ignore
  type: object
version: 0.0.1
