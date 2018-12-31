## How to pass custom parameters through CLI?

You can pass your parameters through CLI and then use them in your code via an environment variable. For example, you can use the variable declared below as process.env.TARGET_ENV in your code. 

```javascript

//Setting variable through CLI
TARGET_ENV=prod ./node_modules/.bin/codeceptjs run  tests/restServiceTest.js  --config=puppeteer.conf.js --steps

//How to use in code
const apidata = require(`../data/data-${process.env.TARGET_ENV}`);
```