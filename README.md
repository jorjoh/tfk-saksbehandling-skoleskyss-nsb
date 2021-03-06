[![Build Status](https://travis-ci.org/telemark/tfk-saksbehandling-skoleskyss-nsb.svg?branch=master)](https://travis-ci.org/telemark/tfk-saksbehandling-skoleskyss-nsb)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat)](https://github.com/feross/standard)
# tfk-saksbehandling-skoleskyss-nsb
Node-module for identifying NSB as transporter.

It uses a combination of zipcodes and schoolids.

## Installation
From GitHub

```sh
$ git clone git@github.com:telemark/tfk-saksbehandling-skoleskyss-nsb.git
```

cd into the directory and run the setup script

```sh
$ npm run setup
```

This will install the module dependencies

## Usage
Pass in an options object and get true or false in return.

**postnummer** zipcode, required

**skole** schoolid, required

```javascript

'use strict';

var transportByNSB = require('tfk-saksbehandling-skoleskyss-nsb');
var options = {
  postnummer: 3681,
  skoleid: 3880
};

console.log(transportByNSB(options)); //Returns true

```

The logic is explained in the [docs/rules.md](/docs/rules.md)

The complete list of schoolids is in [lib/data/skoler.json](/lib/data/skoler.json)

## Test

```sh
$ npm test
```