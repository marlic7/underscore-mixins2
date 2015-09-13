# underscore-mixins2 (underscore with additional methods)

## usage

```
var _ = require('underscore-mixins2');
```

### _.lookup

```
_.lookup(error, 'responseJSON.error.message') // returns error.responseJSON.error.message if it exists otherwise `undefined`

_.lookup(error, 'responseJSON.error.message', false) // returns error.responseJSON.error.message if it exists otherwise false

/**
  returns error.responseJSON.error.message if it exists and evaluates to true
  otherwise returns 'not exists'
 */
_.lookup(error, 'responseJSON.error.message', 'not exists', 'not exists')
```

### _.lookupLength

```
_.lookupLength(error, 'responseJSON.error.stack', 0) // returns error.responseJSON.error.stack.length if it exists otherwise 0
```

## _.deepExtend

```
_.deepExtend({db: {a:1, b:2}}, {ldap: 1, db: {b: 22, c: 3}}); // returns: { db: { a: 1, b: 22, c: 3 }, ldap: 1 }
```

