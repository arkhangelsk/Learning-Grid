Use babel npm package to transpile your ES6 to ES5

1. Setup your project to use npm by running `npm init` command. This will create a package.json file in the root directory
2. install babel required packages

```
npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/node
```

* babel-cli package includes command line Babel tools
* babel-preset-env package has the code that maps ES6 and above (ES6+), to ES5

3. Create .babelrc file. Inside .babelrc you need to define the preset for your source JavaScript file. To specify that you are transpiling code from an ES6+ source, add the following code into .babelrc:

```
{
  "presets": ["@babel/preset-env"]
}
```

4. Create a npm build script using the babel command in package.json


```
"scripts": {
     "build": "babel src -d build"
``` 

The babel command takes two arguments: the path to your ES6 code and a path where you want your ES5 code to be placed.

Adding the -d flag to the command instructs Babel to write the transpiled code to a directory. In above example, ES6 code is in src directory and babel writes the transpiled code into 'build' directory.

5. Run the npm command

```
npm run build
``` 

Now you'll see your converted JavaScript files in the build directory. 

Reference: 

[Convert ES6 into ES5 using Babel](https://medium.com/@SunnyB/how-to-convert-es6-into-es5-using-babel-1b533d31a169)

