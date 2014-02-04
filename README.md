anchor-schema   [![Build Status](https://travis-ci.org/weo-edu/anchor-schema.png?branch=master)](https://travis-ci.org/weo-edu/anchor-schema)
=============

### Example

```javascript
var anchorSchema = require('anchor-schema');
var schema = {
  username: 'string',
  email: {
    type: 'string',
    email: true
  }
};
var validators = anchorSchema(schema);

function onSubmit(model) {
  var valid = validators(model, function(prop, rule, valid) {
    // Log property and rule specific errors here
  });

  if(valid) {
    // Submit
  } else
    // Show errors
}
```
