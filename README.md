[new-thunk](https://www.npmjs.com/package/new-thunk) - npm
====

  `new-thunk` is Thunk implementation.<br/>
  it supports browser Chrome, Firefox, ie11, ie9, ie8. (tested)<br/>
  also supports node.js.

# INSTALL:

[![NPM](https://nodei.co/npm/new-thunk.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/new-thunk/)
[![NPM](https://nodei.co/npm-dl/new-thunk.png?height=2)](https://nodei.co/npm/new-thunk/)

for node.js

```bash
$ npm install new-thunk --save
```

or

for browsers

[https://lightspeedworks.github.io/new-thunk/new-thunk.js](https://lightspeedworks.github.io/new-thunk/new-thunk.js)

```html
<script src="https://lightspeedworks.github.io/new-thunk/new-thunk.js"></script>
```

# PREPARE:

you can use Thunk.

```js
var Thunk = require('new-thunk');
// you can use Thunk
```


# USAGE:

Thunk Specification
----

### new Thunk(setup)

how to make thunk.

```js
thunk = new Thunk(
  function setup(callback) {
    // async process -> callback(error, value)
    try { callback(null, 'value'); }
    catch (error) { callback(error); }
  }
);
// setup(
//  function callback(error, value) {},
```

example

```js
var thunk = new Thunk(
  function setup(callback) {
    setTimeout(function () {
      if (Math.random() < 0.5) callback(null, 'value');
      else callback(new Error('error'));
    }, 100);
  }
);

thunk(function callback(error, value) {
  if (error) console.error(error);
  else console.info(value);
});
```

### thunk(callback)

how to use thunk.

```js
thunk = thunk(
  function callback(error, value) {});
```

example

```js
thunk = thunk(function callback(error, value) {
  if (error) console.error(error);
  else console.info(value);
});
```

# TO DO LIST

  [To Do List](todo.md)

# LICENSE:

  MIT
