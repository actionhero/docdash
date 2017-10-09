# Docdash
[![npm package](https://img.shields.io/npm/v/docdash-actionhero.svg)](https://www.npmjs.com/package/docdash-actionhero) [![license](https://img.shields.io/npm/l/docdash-actionhero.svg)](LICENSE.md)

A clean, responsive documentation template theme for JSDoc 3.

![docdash-screenshot](https://pbs.twimg.com/media/DLuxGsFU8AAaFNz.png:large)

## Where?
I power [docs.actionherojs.com](https://docs.actionherojs.com)

## Install

```bash
$ npm install docdash-actionhero
```

## Usage
Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/docdash-actionhero
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
  "template": "node_modules/docdash-actionhero"
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
        "template": "assets/template/docdash/",
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

## Options
Docdash supports the following options:

```
{
    "docdash": {
        "static": [false|true],  // Display the static members inside the navbar
        "sort": [false|true]     // Sort the methods in the navbar
    }
}
```

Place them anywhere inside your `jsdoc.json` file.

## Thanks
Thanks to [lodash](https://lodash.com) and [minami](https://github.com/nijikokun/minami).

## License
Licensed under the Apache License, version 2.0. (see [Apache-2.0](LICENSE.md)).
