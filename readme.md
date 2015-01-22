## [![npm][npmjs-img]][npmjs-url] [![mit license][license-img]][license-url] [![build status][travis-img]][travis-url] [![coverage status][coveralls-img]][coveralls-url] [![deps status][daviddm-img]][daviddm-url]

> Simple, fast, flexible and cross-platform async executing commands (with child_process spawn)

## Install
```bash
npm install async-exec-cmd
npm test
```


## API
> For more use-cases see the [tests](./test.js)

### [.asyncExecCmd](./index.js#L35)
> Async execute command via spawn

* `<cmd>` **{String}**  
* `<args>` **{Array|Function}**  
* `[opts]` **{Object|Function}**  
* `[callback]` **{Function}**  
* `returns` **{Stream}** spawned child process  

**Example:**

```js
var exec = require('async-exec-cmd');
var cp = exec('echo', [
  'hello world'
], function __cb(err, res) {
  // as usual
  if (err) {
    return console.error(err);
  }
  var stdout = res[1];
  var code = res[0];
  console.log(stdout, code)
  //=> code is process exit/close code
  //=> stdout === 'hello world'
})
```


## Author
**Charlike Mike Reagent**
+ [gratipay/tunnckoCore][author-gratipay]
+ [twitter/tunnckoCore][author-twitter]
+ [github/tunnckoCore][author-github]
+ [npmjs/tunnckoCore][author-npmjs]
+ [more ...][contrib-more]


## License [![MIT license][license-img]][license-url]
Copyright (c) 2015 [Charlike Mike Reagent][contrib-more], [contributors][contrib-graf].  
Released under the [`MIT`][license-url] license.


[npmjs-url]: http://npm.im/async-exec-cmd
[npmjs-img]: https://img.shields.io/npm/v/async-exec-cmd.svg?style=flat&label=async-exec-cmd

[coveralls-url]: https://coveralls.io/r/tunnckoCore/async-exec-cmd?branch=master
[coveralls-img]: https://img.shields.io/coveralls/tunnckoCore/async-exec-cmd.svg?style=flat

[license-url]: https://github.com/tunnckoCore/async-exec-cmd/blob/master/license.md
[license-img]: https://img.shields.io/badge/license-MIT-blue.svg?style=flat

[travis-url]: https://travis-ci.org/tunnckoCore/async-exec-cmd
[travis-img]: https://img.shields.io/travis/tunnckoCore/async-exec-cmd.svg?style=flat

[daviddm-url]: https://david-dm.org/tunnckoCore/async-exec-cmd
[daviddm-img]: https://img.shields.io/david/tunnckoCore/async-exec-cmd.svg?style=flat

[author-gratipay]: https://gratipay.com/tunnckoCore
[author-twitter]: https://twitter.com/tunnckoCore
[author-github]: https://github.com/tunnckoCore
[author-npmjs]: https://npmjs.org/~tunnckocore

[contrib-more]: http://j.mp/1stW47C
[contrib-graf]: https://github.com/tunnckoCore/async-exec-cmd/graphs/contributors

***

_Powered and automated by [kdf](https://github.com/tunnckoCore), January 22, 2015_