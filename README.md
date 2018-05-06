# read-argv
> Read the _[process.argv](https://nodejs.org/docs/latest/api/process.html#process_process_argv)_ as an object

The [process.argv](https://nodejs.org/docs/latest/api/process.html#process_process_argv) property returns an array containing the command line arguments passed when the Node.js process was launched. The first element will be [process.execPath](https://nodejs.org/docs/latest/api/process.html#process_process_execpath) which will be read by the underscore variable. See **process.argv0** if access to the original value of **argv[0]** is needed. The second element will be the path to the JavaScript file being executed which will also be read by the underscore. The remaining elements will be any additional command line arguments.

## Usage:

```js
const readArgv = require('read-argv');

const argv = readArgv(process.argv);
const files = argv._;
const args = argv.$.slice(3);
```
