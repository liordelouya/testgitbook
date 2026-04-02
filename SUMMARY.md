# Table of contents

## API Reference

* [Create/Update Third Party API](README.md)
  * ```yaml
    type: builtin:openapi
    props:
      models: false
      downloadLink: false
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: update-vendor
    ```
* [Get Third Parties API](api-reference/get-third-parties-api/README.md)
  * ```yaml
    type: builtin:openapi
    props:
      models: false
      downloadLink: false
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: get-companies
    ```
