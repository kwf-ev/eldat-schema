# eldat-schema
[.eldat](https://eldatstandard.de/) is the data standard for communication between the partners in the wood supply chain. 

.eldat files are basically [JSON](https://www.json.org/json-de.html) files that have been created according to a given data format.

This data format is defined by a [JSON Schema](https://json-schema.org), the `schema_de.json` file, that allows you to validate your .eldat documents.

## Usage
There are [implementations](https://json-schema.org/implementations.html) for common languages.

These implementations make it easy to validate a .eldat 1.0.3 document against the provided schema.

For working with `.eldat` files you only need the `schema_de.json` file which contains the complete .eldat 1.0.3 data format definition with German titles and descriptions.

### How to validate .eldat 1.0.3 files
1. Read your .eldat file as a `string`
2. Check if this `string` is a valid `JSON` string by [parsing](https://www.json.org/json-de.html) it with your chosen JSON library
3. Validate your `JSON` against the provided `schema_de.json` to ensure that it corresponds to a valid eldat 1.0.3 document

