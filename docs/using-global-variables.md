# Usage globalVariable and usecases

## Overview

It can inject global variables by editting neutralino.config.json

```json
{
   // 
  "globalVariables": {
    "TEST1": "Hello",
    "TEST2": [2, 4, 5],
    "TEST3": {
      "value1": 10,
      "value2": {}
    }
  },
}
```

We can access by call `app.getConfig` API.

```javascript
const config = await Neutralino.app.getConfig();

// print 'Hello"'.
console.log(config.globalVariables.TEST1);
```

Wen we calls it, api return same value.
We can use them as immutable.

# Usecases

## Inject global api key

When we use Sentry to capture errors, it requires DSN and settings.
But these values should not be managed in application code.

It can keep them outside of code.

## Default theme

When we use CSS library, we can use for default values of theme.

# Questions

Should we manage values difference for environments?
