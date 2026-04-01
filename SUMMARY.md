# Table of contents

## API Reference

* [Create/Update Third Party API](README.md)
  * ```yaml
    props:
      models: true
      downloadLink: false
    type: builtin:openapi
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: update-vendor
    ```
* [Get Third Parties API](api-reference/get-third-parties-api/README.md)
  * ```yaml
    props:
      models: true
      downloadLink: false
    type: builtin:openapi
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: get-companies
    ```
