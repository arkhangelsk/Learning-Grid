## npm Commands:

> npm install package-name 

This command will install the package-name & add to the package.json

> npm uninstall package-name

This command will remove or uninstall the package-name from node_modules & package.json

> npm help

This command is to get a list of all available npm commands.

> npm ls

This command will print all top-level installed packages and their dependencies in a tree structure.

> npm show package-name

This command will show all the information about the given package-name 

> npm outdated

This command will show all outdated packages in the current folder.

> npm update

This command will update the outdated packages in current folder

> npm install package-name@latest

This command will install latest version of given package-name

## npm run scripts:

> npm help npm-scripts

This command will provide information on how npm handles the "scripts" field

## Package.JSON

Run the command **npm init** to create the file while answering some questions about your project.

Run the command **npm init -y** to create the file with default values without a need to answer any question.

This file:

* Contains meta-data about your project
* Manages dependencies of your project
* Contains scripts that help in generating builds, running tests and some other stuff

Run the command **npm install** to install dependencies from an existing project using Package.JSON

**Adding dependencies to Package.JSON**

> npm install packagename --save //install as devDependency

Note: As of npm 5.0.0, installed modules are added as a dependency by default, so the --save option is no longer needed. 

> npm install -D packagename //install as dependency

> npm help install //to check help for npm install command

**Installing npm packages locally or globally**

$npm install packagename //installs locally. The command will be available to run from the folder where it is installed.

$npm install -g packagename //installs globally.The command will be available to run from anywhere.

npm packages can be installed locally or globally.

## Package-lock.JSON

* Automatically generated for any operations where npm modifies either the node_modules tree, or package.json.
* As the package-lock specifies a version, location and integrity hash for every module and each of its dependencies, the install it creates will be the same, every single time. 

**References:**

https://medium.com/beginners-guide-to-mobile-web-development/why-package-json-npm-basics-cab3e8cd150

https://medium.com/coinmonks/everything-you-wanted-to-know-about-package-lock-json-b81911aa8ab8

## Semantic Versioning (SemVer)

Major.Minor.Patch (4.5.0)

* Major: Breaking Changes
* Minor: Backward Compatible
* Patch: Bug Fixes 

**Symbols used in SemVer:**

~ means update can install the most recent patch version (e.g. ~4.5.0) - matches any 4.5.x version.

^ means update can install most recent minor version (e.g. ^4.5.0) - matches any 4.x.y version.

## Common Issues:

**Issue:**

Error: Cannot find module '../lib/utils/unsupported.js'

**Solution:**

Uninstall node: $brew uninstall --force node

Install it again: $brew install node

If the above solution doesn't work, check out: https://gist.github.com/DanHerbert/9520689

OR run $brew uninstall --force node

then visit https://nodejs.org/en/ and download the LTS version and install and the error will be gone.

**Issue:**

npm throws error while trying to install any package globally without using sudo

**Solution:**

Check out: 

https://www.competa.com/blog/how-to-run-npm-without-sudo/

https://www.competa.com/blog/use-nvm-for-fun-and-profit-and-to-run-npm-without-sudo/