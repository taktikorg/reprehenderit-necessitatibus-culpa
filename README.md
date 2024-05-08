# @taktikorg/reprehenderit-necessitatibus-culpa <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![dependency status][deps-svg]][deps-url]
[![dev dependency status][dev-deps-svg]][dev-deps-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Robustly `.call.bind()` a function.

## Getting started

```sh
npm install --save @taktikorg/reprehenderit-necessitatibus-culpa
```

## Usage/Examples

```js
const assert = require('assert');
const callBind = require('@taktikorg/reprehenderit-necessitatibus-culpa');
const callBound = require('@taktikorg/reprehenderit-necessitatibus-culpa/callBound');

function f(a, b) {
	assert.equal(this, 1);
	assert.equal(a, 2);
	assert.equal(b, 3);
	assert.equal(arguments.length, 2);
}

const fBound = callBind(f);

const slice = callBound('Array.prototype.slice');

delete Function.prototype.call;
delete Function.prototype.bind;

fBound(1, 2, 3);

assert.deepEqual(slice([1, 2, 3, 4], 1, -1), [2, 3]);
```

## Tests

Clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@taktikorg/reprehenderit-necessitatibus-culpa
[npm-version-svg]: https://versionbadg.es/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa.svg
[deps-svg]: https://david-dm.org/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa.svg
[deps-url]: https://david-dm.org/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa
[dev-deps-svg]: https://david-dm.org/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/reprehenderit-necessitatibus-culpa.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/reprehenderit-necessitatibus-culpa.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/reprehenderit-necessitatibus-culpa.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/reprehenderit-necessitatibus-culpa
[codecov-image]: https://codecov.io/gh/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@taktikorg/reprehenderit-necessitatibus-culpa
[actions-url]: https://github.com/taktikorg/reprehenderit-necessitatibus-culpa/actions
