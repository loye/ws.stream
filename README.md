ws.stream
============

WebSocket steam based on ws.

## How to use

Install by `$ npm install ws.stream`


###Example:

```js
//echo server
var wss = require('ws.stream');
wss.listen({ port: 1337 }, function (s) {
  s.pipe(s);
});
```


```js
//client for testing echo server
var wss = require('ws.stream');
wss.connect('ws://localhost:1337').on('connect', function (s) {
  process.stdin.pipe(s).pipe(process.stdout);
});
```
