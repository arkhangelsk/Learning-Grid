## Node Module Wrapper Function

`(function (exports, require, module, __filename, __dirname) {  `
`});`

This is an IIFE (Immediately Invoked Function Expression). Code in a (Node)file is wrapped inside this particular function. When someone requires this file, IIFE runs automatically and provides objects such as module.exports, exports, __dirname, __filename. These objects are not global but local to the module (file). 

Reference: https://nodejs.org/api/modules.html#modules_the_module_wrapper