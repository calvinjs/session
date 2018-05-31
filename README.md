# Session

Middleware for Dylan which provides cookie based sessions.

## Install

`npm install @dylanjs/session`

## Usage

``` js
const session = require('@dylanjs/session');
app.use(session({ cookie: 'foo', secret: 'boo' }));
app.get('/foo', (req, res) => {
  req.session.set('hello', 'world');
});
app.get('/boo', (req, res) => {
  req.session.get('hello'); // returns 'world'
});
```

