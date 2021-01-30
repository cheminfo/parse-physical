# physical-parser

[![NPM version][npm-image]][npm-url]
[![build status][ci-image]][ci-url]
[![Test coverage][codecov-image]][codecov-url]
[![npm download][download-image]][download-url]

Try to parse a string containing physical data like bp, mp.

## Installation

`$ npm i physical-parser`

## Usage

```js
import { parseBP, parseDensity, parseNumbersUnit } from 'physical-parser';

let bp = parseBP('100-120 @ 50 mmHg', {
  temperature: {
    defaultUnit: '°C'
  }
  pressure: {
    defaultValue: 760,
    defaultUnit: 'mmHg'
  }
})

// bp: {temperature: {low: 100, high: 120, unit: '°C'}, pressure: {low: 50, unit: 'mmHg'}};

let density = parseDensity('1.5-1.51, t=25', {
  value: {
    defaultUnit: 'g/mL'
  },
  temperature: {
    defaultUnit: '°C'
  }
})

// density: {low: 1.5, high: 1.51, unit: 'g/mL'}


```

## [API Documentation](https://cheminfo.github.io/physical-parser/)

## License

[MIT](./LICENSE)

[npm-image]: https://img.shields.io/npm/v/physical-parser.svg
[npm-url]: https://www.npmjs.com/package/physical-parser
[ci-image]: https://github.com/cheminfo/physical-parser/workflows/Node.js%20CI/badge.svg?branch=master
[ci-url]: https://github.com/cheminfo/physical-parser/actions?query=workflow%3A%22Node.js+CI%22
[codecov-image]: https://img.shields.io/codecov/c/github/cheminfo/physical-parser.svg
[codecov-url]: https://codecov.io/gh/cheminfo/physical-parser
[download-image]: https://img.shields.io/npm/dm/physical-parser.svg
[download-url]: https://www.npmjs.com/package/physical-parser
