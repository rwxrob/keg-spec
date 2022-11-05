# Aggregation and Attribution

A KEG will frequently contain content composed from other sources. This raises obvious legal considerations that can be informed from the [software industry].

Frequently, software with critical dependencies on other software will "vendor" or create an exact duplicate of the software needed so that there is no chance of that software one day going away. Attribution is sometimes required in such cases legally.

Some web information services (such as StackExchange) have similar needs. When a person posts a suggested answer to a question they are required to duplicate the content of a source rather than simply link to it. This "static" duplication ensures that the post remains unbroken if the "dynamic" source were to go away.

Given these considerations and best practices it is clear KEG content must be considered static for the purposes of consumption and generation. This allows KEG publishing and rendering tools to have everything they need to create the required output without having to dynamically fetch anything from a linked dependency.

::: Note
Note that any given KEG node content generators themselves may regularly be poll sources to provide the otherwise static content within that node. These [dynamic nodes] still result in KEG content that can be considered static at any specific moment in time.
:::

How attribution legal requirements are fulfilled is entirely up to the content creator. Nothing in the KEG specification fulfills these requirements alone. Some will choose to place initial paragraphs stating the source of the content of that specific node. Some may choose to place all of these dependencies in a single `legal` node and refer to that from the main `README.md` file for the entire KEG. Whatever the method, KEG supports it and requires the use of static content --- even from remote sources --- so that any KEG or cached KEG copy is always available.

[software industry]: /software-composition-and-aggregation
[dynamic node]: /dynamic-node
