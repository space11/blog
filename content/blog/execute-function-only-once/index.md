---
title: Execute function in JavaScript only once.
date: "2019-03-05T13:55:00"
author: "Borys"
---

### Add field to function - hey function is an object in JavaScript!

```JavaScript
function willExecuteOnce() {
    if(willExecuteOnce.executed) return;
        // this will execute only once
        foo();
    willExecuteOnce.executed = true;
}
```


### Use third-party library in example lodash
```JavaScript
const initialize = _.once(createApplication);
initialize();
initialize();
// => `createApplication` is invoked once
```