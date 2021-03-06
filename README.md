Utility to clear read-only flag from actual files in both Windows and Linux environments


[![Build Status](https://travis-ci.org/Karankang007/gulp-clear-readonly.svg?branch=master)](https://travis-ci.org/Karankang007/gulp-clear-readonly)

## Installation
Install package with NPM and add it to your development dependencies:

`npm install --save-dev gulp-clear-readonly`

## Usage
```js
var clearReadOnly = require('gulp-clear-readonly');

// Clearing readonly flag from all files are sub folders recursively
gulp.task('clearReadOnlyFolder', function(done){
  return clearReadOnly("./wwwroot", done);
});

// Clearing readonly flag from a file
gulp.task('clearReadOnlyFile', function(done){
  return clearReadOnly("./wwwroot/testFile", done, {
    isFile: true
  });
});

// Enable debug logging, Default: false
gulp.task('clearReadOnlyWithDebug', function(done){
  return clearReadOnly("./wwwroot/testFile", done, {
    debug: true
  });
});

```

## Supports Pass-through callback result

If the specified callback returns a result, the same result will be pass-throughed clearReadOnly function call.
