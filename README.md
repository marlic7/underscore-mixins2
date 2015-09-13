# underscore-mixins2 
Exports underscore with additional methods (see below).

Important!
We don't modify underscore from cache see: [`library-mixin-fake`](https://github.com/marlic7/library-mixin-fake)

## install
```shell
npm install --save underscore-mixins2
```

## usage
```js
var _ = require('underscore-mixins2');
```

## Additional methods

### _.lookup

returns value of `error.responseJSON.error.message` if it exists otherwise `undefined`

```js
_.lookup(error, 'responseJSON.error.message');
```

returns value of `error.responseJSON.error.message` if it exists otherwise `false`

```js
_.lookup(error, 'responseJSON.error.message', false); 
```

returns value of `error.responseJSON.error.message` if it exists and evaluates to `true`
otherwise returns 'not exists'

```js
_.lookup(error, 'responseJSON.error.message', 'not exists', 'not exists')
```

### _.lookupLength

returns value of `error.responseJSON.error.stack.length` if it exists otherwise `0`

```js
_.lookupLength(error, 'responseJSON.error.stack', 0);
```

## _.deepExtend

returns object: 
```js
{ db: { a: 1, b: 22, c: 3 }, ldap: 1 }
```

```js
_.deepExtend({db: {a:1, b:2}}, {ldap: 1, db: {b: 22, c: 3}});
```

