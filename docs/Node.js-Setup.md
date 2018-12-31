## Check Node Installation & install Path:

**Install Node:**

> $brew install node

**Upgrade Node Version:**

> $brew upgrade node

**Check Node/npm/npx version:**

> $node -v

> $npm -v

> $npx -v

**Check Node/npm/npx installation path:**

> $which node 

> $which npm

> $which npx

## REPL:

**Open Node REPL:**

> $node

**Open multi-line editor in REPL:**

> $.editor

**Check commands available in REPL:**

> $.help

## Check if your version of node supports modern JavaScript:
Start node in REPL mode and type below line of code in node interactive session. If you get an error, means you need to upgrade your node version:

**Modern JS Test:**

> (async (a = 1, ...b) => ({ ...b, a, [a]: `${a}` }))()

**New Promise APIs:**

> util.promisify

> require('fs').promises

Ref: https://gist.github.com/samerbuna/8d9d36576df425181e70e50b3cb35f3a

