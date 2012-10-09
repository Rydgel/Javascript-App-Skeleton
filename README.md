# Javascript App Skeleton for use with [Brunch](http://brunch.io/)

Main languages are JavaScript,
[Stylus for CSS pre-processing](http://learnboost.github.com/stylus/) and
[Handlebars for templating](http://handlebarsjs.com/).  Also included is [Backbone.Mediator](https://github.com/chalbert/Backbone-Mediator) for implementing Pub/Sub patterns.

## Installation

First install Brunch: `sudo npm install -g brunch` and then run `brunch new <app> -s https://github.com/damassi/Javascript-App-Skeleton` & then `npm install` and finally `brunch build`.  To continually watch for changes, use `brunch watch`.
See more info on the [official site](http://brunch.io)

## Unit Testing

The Mocha test-suite is included by default.  Files located in `tests` that end with `_test.coffee` (or .js) are automatically packaged.  

To run tests independent of the browser, execute `brunch test`; to run them in the browser, navigate to `public/test/index.html`.  

## Overview

    config.coffee
    README.md
    /app/
      /assets/
        index.html
        images/
      styles/
      helpers/
      config/
      events/
      utils/
      routers/
      models/
      /views/
        templates/

      Application.js
      initialize.js
    /test/
    /vendor/
      scripts/
        backbone.js
        jquery.js
        console-helper.js
        underscore.js
      styles/
        normalize.css
        helpers.css

* `config.coffee`  contains configuration of your app. You can set plugins /
languages that would be used here.
* `app/assets` contains images / static files. Contents of the directory would
be copied to `build/` without change.
Other `app/` directories could contain files that would be compiled. Languages,
that compile to JS (coffeescript, roy etc.) or js files and located in app are 
automatically wrapped in module closure so they can be loaded by 
`require('module/location')`.
* `app/models` & `app/views` contain base classes your app should inherit from.
* `test/` contains feature & unit tests.
* `vendor/` contains all third-party code. The code wouldn’t be wrapped in
modules, it would be loaded instantly instead.

This all will generate `public/` (by default) directory when `brunch build` or `brunch watch` is executed.

## Other
Versions of software the skeleton uses:

* jQuery 1.7.2
* Backbone 0.9.1
* Underscore 1.3.3
* HTML5Boilerplate 3.0.3

The license is [public domain](http://creativecommons.org/publicdomain/zero/1.0/).
Use it however you want.
