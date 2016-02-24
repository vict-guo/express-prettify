# express-prettify

[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]

express middleware to send pretty printed json


## Install

    $ npm install express-prettify


## Examples

```js
"use strict";

var app = require('express')();
var pretty = require('express-prettify');

app.use(pretty({ query: 'pretty' }));

app.get('/', function(req, res) {
  res.json({ hello: 'world', body: 'This is pretty printed json' });
});

app.listen(3000);
```
    $ node app.js &

    $ curl http://localhost:3000?pretty
    {
      "hello": "world",
      "body": "This is pretty printed json"
    }

    $ curl http://localhost:3000
    { "hello": "world", "body": "This is pretty printed json" }


## License

[MIT](http://stoshiya.mit-license.org/2016)

[npm-image]: https://img.shields.io/npm/v/express-prettify.svg?style=flat
[npm-url]: https://npmjs.org/package/express-prettify
[downloads-image]: https://img.shields.io/npm/dm/express-prettify.svg?style=flat
[downloads-url]: https://npmjs.org/package/express-prettify