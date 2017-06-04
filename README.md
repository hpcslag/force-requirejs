# Force-Require.js
Help you to install the module automatically also can require the module from web.

# Install
Install force-require.js from npm.
``` sh
npm install force-requirejs -g
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
const frequire = require('force-require');

frequire.version('~'); //install module with this version or up then this version.

const someModule = frequire('npm://hpcslag@microdatabase').savedev().use('~1.1.3');// --save-dev and return module.


const someModule2 = require('https://github.com/hpcslag/microdatabase').nostorage(); //here you can require the module from github. *nostorage() will cleanup this module every time when you start.
const someModule3 = require('https://TANETIPADDRESSTEST.com/hpcslag/microdatabase').; //here you can require the module from web.
const someModule3 = require('https://TANETIPADDRESSTEST.com/hpcslag/microdatabase.zip'); //here you can require the .zip module from web.

const someModule3 = require('https://www.npmjs.com/package/chalk').cmd(['--save-dev','--xxx']).use('^3.4.5'); //use module from npm
```

If your repo need to use auth, also can do it:
Add file: `.authdata`
```json
{
    "moduleName or input url string":{
        "authType":"basic auth",
        //use
        "auth":"auth", 
        //or
        "username":"xxxx",
        "password":"xxxxxx"
    }
}
```

# API

# Support Repo
 - Github
 - npmjs
 - Personal url
 - zip file
