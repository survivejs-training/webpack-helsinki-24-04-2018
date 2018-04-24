# Webpack - The Good Parts

* [Slides](https://presentations.survivejs.com/webpack-the-good-parts/#/1)
* [Book](https://survivejs.com/webpack/)

## Schedule

**24.04.2018**

* 09:30-12:00 - Slides
* 12:00-13:00 - Freeform, QA

## Goals

* Using webpack more efficiently
* How to optimize modules, tree-shaking, how to do this
* Webpack from scratch
* How to set up a project properly
* Code splitting, how to write custom plugins

## Examples

```javascript
import foo from 'foo'; // what happens now?

// 1. Look at node_modules
// 2. ???
```

```javascript
const path = require('path');

module.exports = {
  resolve: {
    alias: {
      foo: path.join(__dirname, 'foo.js'),
    },
    extensions: [
      /*...*/
      '.jsx',
      '.js'
    ],
    modules: [
      /*...*/
      path.join(__dirname, 'my_modules'),
      path.join(__dirname, 'node_modules'),
    ],
  }
};
```
