## module.exports

* 'module' is a variable that represents the module, and 'exports' exposes the module as an object.


```javascript
let Book = {};
Book.JavaScript = "You Don't know JS";
module.exports = Book;
```


* module.exports can expose the current module as an object. You can do this by wrapping any collection of data and functions in an object, and exporting the object using module.exports


```javascript
module.exports = {
    javascript: "You Don't know JS",
    getJavaScript: function(){
        return this.javascript;
    }
};
```

## require

require method imports the module for use in the current program.

```javascript
const book1 = require('./book1'); 
const book2 = require('./book2'); 
```
## export default

When using ES6 syntax, use export default in place of module.exports statement to export JavaScript objects, functions, and primitive data types.


```javascript
let Car = {};

export default Car;
```

## import

In ES6 syntax, module introduces the import keyword for importing objects.


```javascript
import Car from './car';
```

In the above example Car specifies the name of the variable to store the default export in. If you are working with local files, no extension is required with the name of the file.

## Named Exports

In ES6, we can also use named exports that allow exporting data through the use of variables.


```javascript
let colors = '';

function isWhite() {
}; 
function isBlack() {
}; 

export { colors, isWhite, isBlack};
```

Named exports can also be exported by placing the keyword export in the beginning of the variable declaration statement.


```javascript
export let colors = '';

export function isWhite() {
}; 
function isBlack() {
}; 
```

## Named Imports


```javascript
import { isWhite, isBlack } from './colors';

console.log(isWhite);
```

## Export as 

You can also change the name of variables when you export or import them.


```javascript
let colors = '';

function isWhite() {
}; 
function isBlack() {
}; 

export { colors as colorChoices, isWhite, isBlack};
```

## Import as 


```javascript
import {isWhite as White} from './color';
```

You can also import the entire module as an alias using 'as':


```javascript
import * as Colors from './color';

Colors.colors;
Colors.isWhite();
Colors.isBlack();
```

## Combining named exports and default export


```javascript
let colors = '';

function isWhite() {
}; 
function isBlack() {
}; 

export {isWhite as White, isBlack as Black};
export default colors;
```

Similarly We can also exported some of the variables at declaration time and export others with the export default syntax.


```javascript
let colors = '';

export function isWhite() {
}; 
export function isBlack() {
}; 

export default colors;

```