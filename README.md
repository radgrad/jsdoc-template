# RadGrad JSDoc 3 Template

A Semantic UI documentation template theme for JSDoc 3.

## Install

```bash
$ npm install radgrad-jsdoc-template
```

## Usage

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/radgrad-jsdoc-template
```

## Usage (npm)

In your projects `package.json` file add a new script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc -c jsdoc.json"
}
```

In your `jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/radgrad-jsdoc-template"
}
```

## Sample `jsdoc.json`

See the config file for the [fixtures](fixtures/fixtures.conf.json) or the sample below.

```json
{
    "tags": {
        "allowUnknownTags": false
    },
    "source": {
        "include": "../js",
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "opts": {
        "template": "assets/template/radgrad-jsdoc-template/",
        "encoding": "utf8",
        "destination": "docs/",
        "recurse": true,
        "verbose": true
    },
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": false
    }
}
```

## Thanks

Thanks to [docdash](https://github.com/clenemt/docdash).

## License

Licensed under the Apache License, version 2.0. (see [Apache-2.0](LICENSE)).
