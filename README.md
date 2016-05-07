# github-pagination
[![NPM version](https://img.shields.io/npm/v/github-pagination.svg?style=flat)](https://www.npmjs.org/package/github-pagination)

A simple js lib for parse GitHub's pagination info from API's response.

------

## Installation

```bash
$ npm install github-pagination --save
```

or 

```bash
$ bower install github-pagination --save
```

## Example
in node.js / io.js

```js
var octopage = require('./');

var test = '<https://api.github.com/search/code?q=addClass+user%3Amozilla&page=15>; rel="next",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=34>; rel="last",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=1>; rel="first",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=13>; rel="prev"';

console.log(octopage.parser(test));
// { next: '15', last: '34', first: '1', prev: '13' }
```

in browser

link this script and then,

```html
<script src="octopage.js"></script>
<script>
  var test = '<https://api.github.com/search/code?q=addClass+user%3Amozilla&page=15>; rel="next",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=34>; rel="last",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=1>; rel="first",  <https://api.github.com/search/code?q=addClass+user%3Amozilla&page=13>; rel="prev"';

  console.log(octopage.parser(test));
  // { next: '15', last: '34', first: '1', prev: '13' }
</script>
```

## License

MIT © [Leigh Zhu](#)
