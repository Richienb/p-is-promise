# p-is-promise

> Check if something is a promise

Why not [`is-promise`](https://github.com/then/is-promise)? That module [checks for a thenable](https://github.com/then/is-promise/issues/6), not an ES2015 promise. This one is stricter.

You most likely don't need this. Just pass your value to `Promise.resolve()` and let it handle it.

Can be useful if you need to create a fast path for a synchronous operation.


## Install

```
$ npm install p-is-promise
```


## Usage

```js
const pIsPromise = require('p-is-promise');
const Bluebird = require('bluebird');

pIsPromise(Promise.resolve('🦄'));
//=> true

pIsPromise(Bluebird.resolve('🦄'));
//=> true

pIsPromise('🦄');
//=> false
```


## Related

- [More…](https://github.com/sindresorhus/promise-fun)


---

<div align="center">
	<b>
		<a href="https://tidelift.com/subscription/pkg/npm-p-is-promise?utm_source=npm-p-is-promise&utm_medium=referral&utm_campaign=readme">Get professional support for this package with a Tidelift subscription</a>
	</b>
	<br>
	<sub>
		Tidelift helps make open source sustainable for maintainers while giving companies<br>assurances about security, maintenance, and licensing for their dependencies.
	</sub>
</div>
