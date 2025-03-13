# Pico Base
A foundation for creating hugo themes using PicoCSS. It is meant to KISS.

## Features
Based on:
```bash
hugo new theme
```
Then converted to YAML and added PicoCSS sass dependencies via npm.
Modified css.html to transpile main.scss (within sass instead of css folder) and link the compiled css. Following hugoes documentation:

https://gohugo.io/functions/css/sass/#dart-sass

## Installation
Reccomendation: Fork this repository, as this is meant to be a start.

## Configuration
Modify main.scss and all the layout files as you need. Reffer PicoCSS and Hugo documentation.
