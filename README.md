# Force-Require.js
Help you to install the module automatically also can require the module from web.

# Install
Install force-require.js from npm.
``` sh
npm install force-requirejs -g
```

Excute program use `frjs`.
```sh
cd /to/folder/path
frjs . run main.js
```


# Take Example
In old case, you usually use this way to require some module:
```js
// npm install someModule first.
// then
// require the name of module from local
const someModule = require('someModule'); 
```

If you use Force-Require.js:
```js
// frjs . run main.js
const someModule = require('someModule');

const someModule2 = require('https://github.com/hpcslag/microdatabase'); //here you can require the module from github.
const someModule3 = require('https://TANETIPADDRESSTEST.com/hpcslag/microdatabase'); //here you can require the module from web.
const someModule3 = require('https://TANETIPADDRESSTEST.com/hpcslag/microdatabase.zip'); //here you can require the .zip module from web.
```

# Usage
#### Auto Install Modules
```sh
frjs [directory] [-g | run] [filePath]
```
 - `directory`: Folder path (`./to/path`)
 - `-g` : Install to global
 - `run` : After install and run
 - `filePath`: If you use the `run` command, Then `filePath` need to fill main `.js` you want to run.
 
 Example:
 ```sh
 frjs ./ run
 ```
 Then `frjs` will make sure all of module is installed and also run the project.
