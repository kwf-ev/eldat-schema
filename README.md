# eldat-schema
.eldat is the data standard for communication between the partners in the wood supply chain. 

.eldat files are basically [`JSON`](https://www.json.org/json-de.html) files that have been created according to a given pattern.
This pattern is defined by following files:

## usage
There are [implementations](https://json-schema.org/implementations.html) for common languages. These implementations make it easy to validate a .eldat document against the corresponding schema.

### validate .eldat files
1. read .eldat file as `string`
2. check if `string` is valid `JSON` and [parse](https://www.json.org/json-de.html)
3. validate `JSON` against `schema_envelope.json` to ensure version-code exists and is valid
4. read `document.meta.version.code` from `JSON`
5. download or select corresponding .eldat-Schema Version from this repository (branch)
6. validate `JSON` against `schema.json` or `schema_de.json`

## about the files
Schema files follow the [JSON-Schema](https://json-schema.org/) syntax. For working with `.eldat` files you need at least `schema.json` or  `schema_de.json` and `schema_envelope.json`.

### schema.json
The complete schema.

### schema_de.json
The complete schema with German titles and descriptions.

### schema_envelope.json
A schema for validating the envelope of a .eldat document.

### lookup-tables.json
The German translation for the lookup tables (enum) in schema.js. These German translations are also included in `schema_de.json`.
