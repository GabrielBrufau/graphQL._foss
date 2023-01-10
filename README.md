# graphQL._foss
## step 1
- let's start create one preject of node in the dir 0.1
- `npm init -y`
- then we can install express `npm i express`
- in the dir 0.1 we go to create an dir `mkdir src`
- inside this create a file `touch index.js` with the next code
```js
const express = require('express');

const app = express()

app.listen(4000,()=> console.log('server on port 4000'));
```
## step 2
- if you can use babel 
- `npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/node`
- config the .babelrc this file go to in the dir 0.1 the same that say the dir proyect
- `touch ./0.1/.babelrc`
```json
{
  "presets": [
    [
      "@babel/preset-env",
      {
        "targets": {
          "edge": "17",
          "firefox": "60",
          "chrome": "67",
          "safari": "11.1"
        },
        "useBuiltIns": "usage",
        "corejs": "3.6.5"
      }
    ]
  ]
}

```
- now in package.json in the scripts part we must write 
```json
"scripts":{
		"build":"babel src -d dist --source-maps",
		"start": "babel-node src/index.js"
		}
```
- -d in the scripts build means that I get the code source src and package in the dir dist
- now if you use one es6 you can run de code because babel is run 
- run the next comand for dev
- `npm start`
- run the next comand for production mode
- `npm run build`
-
## step 3
