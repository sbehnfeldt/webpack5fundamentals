# Webpack5
Sing-a-long with the video series _Webpack 5 Fundamentals_ by "How To Code"  
ref: https://www.youtube.com/playlist?list=PLB67cosR0_lPUXIK35J8M7EQUbUJQMA0Q

```shell
$> git init .
```

## Lesson 1) Concepts and Overview
ref: https://www.youtube.com/watch?v=sXxVAKTzQ80&list=PLB67cosR0_lPUXIK35J8M7EQUbUJQMA0Q  
ref: https://webpack.js.org/concepts/  
Core concepts:
- Entry
  - File that is the entry point for webpack
  - typically, "index.js"
  - all other js, css etc processed from here
- Output
  - where the bundled assets are written
  - typically "dist" directory
- Loaders
  - how webpack should process a specific file type
  - webpack natively knows how to process only JS and JSON files
- Plugins
  - add additional functionality
  - eg, automatically create an index.html file w/ references to output files
- Mode
  - optimizations based on environment
  - development, production or none
- Browser Compatibility
  - not covered explicitly in this course, as browser compatibility issues will be handled by the Babel transpiler plugin

## Lesson 2) Installation & Setup 
ref: https://www.youtube.com/watch?v=sZYnwFrwXAw&list=PLB67cosR0_lPUXIK35J8M7EQUbUJQMA0Q&index=2  
ref: https://github.com/robertguss/webpack-5-fundamentals-course  
ref: https://webpack.js.org/guides/getting-started/  

Requires NodeJS: https://nodejs.org/en/download  

Confirm NodeJS successfully installed: `$> node -v`  

Initialize package.json file:
```shell
$> npm init -y
$> npm i -D webpack webpack-cli
$> mkdir src
$> touch webpack.config.js
$> touch src/index.js
```
The Webpack guide suggests the above dependencies, `webpack` and `webpack-cli`.
The video series replaces `webpack` with `webpack@next`, but this errors out at this time.

**Using a configuration file**

`webpack.config.js`
```js
const path=require( 'path' );

module.exports = {
    entry: './src/index.js',
    output: {
        filename: 'bundle.js',
        path: path.resolve(__dirname, 'dist' ),
    },
}
```
Bundle the assets directly:
```shell
$> npx webpack --config webpack.config.js
```

Or, add a script to package.json:  
_package.json_  
```json
{
  "scripts": {
    "build": "webpack"
  }
}
```
Then execute webpack via the package.json script:
```shell
$> npm run build
```