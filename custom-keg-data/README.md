# Custom KEG Data

Any KEG structured data file that allows maps (aka "objects", "dictionaries") may contain custom data specified by the owner of any domain (including subdomains) on the Internet. These custom data may be used by anyone, anywhere --- allowing the creation of data models used globally --- but only the `KEG.yaml` file at the root URI for that domain is able to specify the scheme for those custom data.

Specification is accomplished by adding the reserved `schema` key to another map with a key matching the root domain. The reserved `schemaType` field allows different models for specifying different schema types over time, but the structured data format will always be KEG simplified YAML. This flexibility allows the KEG network to grow and adapt over time.

```yaml
keg.pub:
  schemaType: json-schema-2020-12
  schema:
    ...
```
