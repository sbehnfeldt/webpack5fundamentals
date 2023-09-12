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
