# Custom data

* A **domain owner** MUST be someone with control of an Internet domain.
* A **domain owner** MAY provide custom data in the `keg` **info file**.
* A **custom data** section in **info file** MUST use domain as key.
* A **domain owner** MUST provide a keg at identifying domain as authoritative schema.

Any Internet **domain owner** can provide custom data that may be used by anyone, anywhere --- allowing the creation of data models to be used organically and globally.

Specification of custom data schemas is accomplished as follows:

1. Create an **authoritative keg** at the domain (or subdomain)
1. Add a section to the `keg` **info file** matching the domain name exactly.
1. Add a subsection of the domain matching the exact name of the schema.
1. Add a `schemaType` identifier (such as `json-schema-2020-12`).
1. Add a `schema` subsection.
1. Add the schema rule definitions under the `schema` subsection.

The reserved `schemaType` field allows different models for specifying different schema types over time, but the structured data format will always be KEG **simplified YAML**. This flexibility allows the KEG network to grow and adapt over time.

```yaml
keg.pub.listing:
  schemaType: json-schema-2020-12
  schema:
    ...
```
