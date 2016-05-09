# Base Snippets

Sublime Text snippets for [Base](https://github.com/node-base/base).

## Getting Started

**Heads up!** Until this is registered with package control, you'll need to [install manually](#manual-installation).

### 1. Installation

#### Package Control

If you already have [Package Control](http://wbond.net/sublime_packages/package_control/) installed in Sublime Text:

* Select "Install Package" from the Command Palette: <kbd>Ctrl+Shift+P</kbd> on Windows and Linux or <kbd>⇧⌘P</kbd> on OS X)
* Search for "**Base Snippets**" and click <kbd>enter</kbd>.

#### Manual Installation

Go to `Preferences -> Browse Packages`, and then either download and unzip this plugin into that directory, or:

``` bash
git clone https://github.com/node-base/sublime-text-base-snippets.git
```

## Snippets

**gen**

Generator.

```js
'use strict';

module.exports = function(app, base) {
  app.task('default', function(cb) {
    console.log('generator', app.name, '> task', this.name);
    cb();
  });
};
```

**gen empty**

```js
'use strict';

module.exports = function(app, base) {
  
};
```

**app**

Exported instance.

```js
'use strict';

var App = require('base');
var app = new App();

app.task('default', function(cb) {
  console.log('appfile.js', '> task', this.name);
  cb();
});

module.exports = app;
```

**sub**

Sub-generator.

```js
module.exports = function(app, base) {
  
};
```

**plugin**

```js
app.task('default', function(cb) {
  
  cb();
});
```

**reg**

```js
app.register('name', function(app, base) {
  
});
```

**task**

```js
app.task('default', function(cb) {
  
  cb();
});
```

**src**

```js
app.src('*.js')
  .pipe(app.renderFile('*'))
```

**dest**

```js
.pipe(app.dest('dest'))
```

**emit**

```js
app.emit('name', 'value');
```

**on**

```js
app.on('name', function(value) {
  
});
```

**through**

```js
through.obj(function(file, enc, next) {
  
  next(null, file);
})
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](LICENSE).
