# generator-gulp-angular [![Build Status](https://secure.travis-ci.org/Swiip/generator-gulp-angular.svg?branch=master)](http://travis-ci.org/Swiip/generator-gulp-angular)

Offers you a Yeoman generator to initiate a Web application with the following workflow:

<img height="100" align="left" src="https://raw.githubusercontent.com/yeoman/yeoman.io/master/app/assets/img/bullet-yo.gif">

<img height="100" align="left" src="http://bower.io/img/bower-logo.png">

<img height="100" align="left" src="https://s3.amazonaws.com/media-p.slid.es/uploads/hugojosefson/images/86267/angularjs-logo.png">

<img height="100" align="left" src="https://raw.github.com/gulpjs/artwork/master/gulp.png">

<br><br><br><br>

## Why generator-gulp-angular ?

This generator aims to takes the best from others generators like generator-angular, ngTailor and generator-gulp-webapp to offers the best workflow to start an application with AngularJS powered by Gulp!

generator-gulp-angular scaffolds out an Angularjs application with a full featured gulpfile.js wich offers all the tasks for a modern Web development.

## Usage

### Create your project

Install `generator-gulp-angular`:
```
npm install -g generator-gulp-angular
```

Make a new directory, and `cd` into it:
```
mkdir my-new-project && cd $_
```

Run `yo gulp-angular`, optionally passing an app name:
```
yo gulp-angular [app-name]
```

### Use Gulp tasks

* `gulp` or `gulp build` to build an optimized version of your application in `/dist`
* `gulp watch` to launch a server with livereload capacities on your source files
* `gulp serve:dist` to launch a server on your optimized application
* `gulp wiredep` to fill bower dependencies in your `.html` file(s)
* `gulp test` to launch your unit tests with Karma
* `gulp protractor` to launch your e2e tests with Protractor
* `gulp protractor:dist` to launch your e2e tests with Protractor on the dist files

## Directory structure

[Best Practice Recommendations for Angular App Structure](https://docs.google.com/document/d/1XXMvReO8-Awi1EZXAXS4PzDzdNvV6pGcuaF4Q9821Es/pub)

But I think keeping first division by file type: scripts, styles, partials.

## Features included in the gulpfile
* *useref* : allow to configure your files in comments of your HTML file
* *ngMin* : convert simple injection in complete syntax to be minificaction proof
* *uglify* : optimize all your JavaScript
* *csso* : optimize all your CSS
* *rev* : add an hash in the files names to prevent all browsers cache problems
* *watch* : watch your source files to recompile them automatically
* *connect* : launch a dev HTTP server, can also be used on the dist files
* *livereload* : the web server will reload every time the watch task detect a change
* *jshint* : JavaScript code linter
* *imagemin* : all your images will be optimized at build
* *Unit test (karma)* : out of the box unit test configuration with karma
* *e2e test (protratctor)* : out of the box e2e test configuration with protractor
* *ngHtml2js* : all HTML partials will be converted in JS to be bundled in the application
* **TODO** lazy : don't process files wich has not change as much as possible
* **TODO** browsersync : replace livereload by browsersync

## Questions the generator will asks
* *jQuery*: jQuery 1.x, 2.x, Zepto, none
* *Angular modules*: animate, cookies, touch, sanitize
* *Resource handler*: ngResource, Restangular, none.
* *Router*: ngRoute, UI Router, none.
* **TODO** *0.3* UI Framework: Bootstrap, SemanticUI, Foundation, none (Will be impacted by the CSS preprocessor chosen)
* **TODO** *0.3* Boostrap directives : UI Bootstrap, Angular Strap, none (Only if Bootstrap has been chosen)
* **TODO** *0.3* CSS preprocessor: less, sass, none
* **TODO** JS preprocessor: CoffeeScript, TypeScript, ECMAScript6 (Traceur)
* **TODO** HTML preprocessor: Jade ?
* **TODO** Script loader: Require, Browserify, ES6 with Require?, none
* **TODO** Test framework: Jasmine, Mocha, Qunit

## TODO -> 0.3

* UI framework
* CSS preprocessor
* Template for each CSS framework
* Bootstrap directives
* Update Modernizer
* Documentation

## Changelog

### 0.2.1

* Fix main.html missing with routing
* Fix unit tests by ignoring bootstrap js files in wiredep

### 0.2.0

* Convert HTML templates into JS and add them into the optimized bundle
* Let you choose to use jQuery, Zepto or nothing (Angular's jqLite)
* Ask for optional Angular modules: animate cookies, touch and sanitize
* Resource handler: ngResource, Restangular, none.
* Router: ngRoute, UI Router, none.

### 0.1.1

* Adding Travis CI

### 0.1.0

* Add unit test with karma and e2e test with protractor
* Split gulp configuration in multiple files
* Create 'inception' test which generate files and try gulp tasks on it
* Add ability to serve dist files and run e2e test on dist files
* Still no options

### 0.0.1

* Initial commit
* Scaffolds a working directory but with no options and no tests

## License

MIT
