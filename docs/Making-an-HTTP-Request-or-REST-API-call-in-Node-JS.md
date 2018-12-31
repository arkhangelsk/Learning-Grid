There are many ways available to send HTTP request or make a REST API call during acceptance testing:

**1. HTTP - The standard library**
* default HTTP module in the standard Node.js library.
* No need to install any external dependency.
* It is NOT very user-friendly compared to other solutions.
* It does not parse the response data manually.
* It does not support HTTPS by default, so you need to require the https module instead if required.

**2. [Request](https://github.com/request/request) - Simplified HTTP client**
* An easy to use library that deals with HTTP requests
* For promise handling, use Bluebird or switch to request-promise library

**3. [Codecept REST API Helper](https://codecept.io/helpers/REST/)**
* This helper use unirest to perform requests.
* Provides easy to understand DSL  

**4. [Unirest](http://unirest.io/nodejs.html)** 
* Lightweight HTTP Request Client library
* Provides a cookie jar to store multiple cookies

**5. [Axios](https://www.npmjs.com/package/axios)**
* This is a promise based HTTP client for the browser and node.js
* Make XMLHttpRequests from the browser
* Make http requests from node.js
* Supports the Promise API
* Intercept request and response
* Transform request and response data
* Cancel requests
* Automatic transforms for JSON data
* Client-side support for protecting against XSRF
* The request contains the following information:

  data: {},status, statusText, headers, config (the config that was provided to axios with request), request.

**Resources:**

[axios cheat sheet](https://kapeli.com/cheat_sheets/Axios.docset/Contents/Resources/Documents/index)

[Getting started with axios tutorial](https://appdividend.com/2018/08/30/getting-started-with-axios-tutorial-example/)

**6. [node-fetch](https://www.npmjs.com/package/node-fetch)**
* A light-weight module that brings window.fetch to node.js
* Stay consistent with window.fetch API. 
* Use native promise, but allow substituting it with other popular promise libraries like Bluebird
* Use native Node streams for body, on both request and response.
* Useful extensions such as timeout, redirect limit, response size limit, explicit errors for troubleshooting.

**7. [request-promise](https://github.com/request/request-promise)**
* Simplified HTTP request client [**'request'**](https://github.com/request/request) with Promise support. Powered by Bluebird.
* request-promise wraps around request so everything that works with request also works with request-promise

**8. [SuperAgent](https://github.com/visionmedia/superagent)**
* Makes AJAX requests from the browser
* Make http requests from node.js
* Provides a function `query()` to add parameters to the request.
* It parses the JSON response automatically.

***

### Cookie Handling:
* [tough-cookie](https://www.npmjs.com/package/tough-cookie)


***

## References:

https://www.twilio.com/blog/2017/08/http-requests-in-node-js.html

https://codeburst.io/how-to-make-an-http-request-in-nodejs-http-mechanism-libraries-f25ec990d307

[Why use Promise Libraries while Node.js has added native support for promises?](https://stackoverflow.com/questions/34960886/are-there-still-reasons-to-use-promise-libraries-like-q-or-bluebird-now-that-we)

Learning Promises:
https://scotch.io/tutorials/javascript-promises-for-dummies
