# Pico Base
A foundation for creating hugo themes using PicoCSS. It is meant to KISS.

## Features
Based on:
```bash
hugo new theme
```
Then converted to YAML and added PicoCSS sass dependencies via npm.

https://picocss.com/docs#install-with-npm

Modified css.html to transpile main.scss (within sass instead of css folder) and link the compiled css. Following hugoes documentation:

https://gohugo.io/functions/css/sass/#dart-sass

In order to refer the right module directory:

https://picocss.com/docs/sass#import

configured the proper includePaths within css.html:

https://gohugo.io/functions/css/sass/#options

´´´go-html-template
  {{ $opts := dict
    "enableSourceMap" (not hugo.IsProduction)
    "outputStyle" (cond hugo.IsProduction "compressed" "expanded")
    "targetPath" "css/main.css"
    "transpiler" "dartsass"
    "includePaths" (slice "node_modules/@picocss/pico/scss")
  }}
´´´

## Installation
Reccomendation: Fork this repository, as this is meant to be a start.

## Configuration
Modify main.scss and all the layout files as you need. See PicoCSS and Hugo documentation.
