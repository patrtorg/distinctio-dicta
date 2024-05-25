# @patrtorg/distinctio-dicta <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Object-related atoms: Object, ToObject, RequireObjectCoercible.

## Example

```js
const assert = require('assert');

const $Object = require('@patrtorg/distinctio-dicta');
const ToObject = require('@patrtorg/distinctio-dicta/ToObject');
const RequireObjectCoercible = require('@patrtorg/distinctio-dicta/RequireObjectCoercible');

assert.equal($Object, Object);
assert.throws(() => ToObject(null), TypeError);
assert.throws(() => ToObject(undefined), TypeError);
assert.throws(() => RequireObjectCoercible(null), TypeError);
assert.throws(() => RequireObjectCoercible(undefined), TypeError);

assert.deepEqual(RequireObjectCoercible(true), true);
assert.deepEqual(ToObject(true), Object(true));

const obj = {};
assert.equal(RequireObjectCoercible(obj), obj);
assert.equal(ToObject(obj), obj);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@patrtorg/distinctio-dicta
[npm-version-svg]: https://versionbadg.es/ljharb/@patrtorg/distinctio-dicta.svg
[deps-svg]: https://david-dm.org/ljharb/@patrtorg/distinctio-dicta.svg
[deps-url]: https://david-dm.org/ljharb/@patrtorg/distinctio-dicta
[dev-deps-svg]: https://david-dm.org/ljharb/@patrtorg/distinctio-dicta/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@patrtorg/distinctio-dicta#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@patrtorg/distinctio-dicta.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@patrtorg/distinctio-dicta.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/es-object.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@patrtorg/distinctio-dicta
[codecov-image]: https://codecov.io/gh/ljharb/@patrtorg/distinctio-dicta/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@patrtorg/distinctio-dicta/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@patrtorg/distinctio-dicta
[actions-url]: https://github.com/patrtorg/distinctio-dicta/actions
