## Accessing environment variables in Node.js

Accessing environment variables in Node.js is supported right out of the box and you can use below command to see what environment variables are available to your node application.

```javascript
console.log(process.env);
```

You can access a specific environment variable using below command:
```
console.log('PATH: ', process.env.PATH);
```

## Using .env file to specify environment variables for your application

**What is a .env file? **

It’s a file used inside your project to specify environment variables. To read variables from .env file, you need Dotenv that is is a zero-dependency module that loads environment variables from a .env file into process.env.

Step 1: Create an .env file and add your required variable.
```
ENVIRONMENT = QA2
```

Step 2: Use the defined variable in your desired file.

**Sample Code:**
```javascript
require('dotenv').config();
console.log('Your environment variable ENVIRONMENT has the value: ', process.env.ENVIRONMENT);
```
Output:
```
Your environment variable ENVIRONMENT has the value:  QA2
```

## Resources:
https://www.twilio.com/blog/2017/08/working-with-environment-variables-in-node-js.html
https://github.com/yatki/read-env
https://github.com/recursivefunk/good-env
https://github.com/tkalfigo/dotenvenc
