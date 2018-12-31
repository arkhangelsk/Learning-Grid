### Configuration

keepCookies: (optional, default: false) - keep cookies between tests when restart set to false.

### WebdriverIO & Puppeteer

**clearCookie:** Clears a cookie by name, if none provided clears all cookies.
```
I.clearCookie();
I.clearCookie('myCookie');
```

**dontSeeCookie:** Checks that cookie with the given name does not exist.
```
I.dontSeeCookie('userID');
```

**grabCookie:** Gets a cookie object by name. If none provided gets all cookies. 
```
let cookie = await I.grabCookie('lang');
assert(cookie.value, 'en');
```	

**seeCookie:** Checks that cookie with given name exists.
```
I.seeCookie('userID');
```

**setCookie:** Sets a cookie.
```
I.setCookie({name: 'auth', value: true});
```

***
**References:**
https://codecept.io/helpers/WebDriverIO/
https://codecept.io/helpers/