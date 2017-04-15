# api documentation for  [fluent-ffmpeg (v2.1.0)](https://github.com/fluent-ffmpeg/node-fluent-ffmpeg#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-fluent-ffmpeg.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fluent-ffmpeg) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fluent-ffmpeg.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fluent-ffmpeg)
#### A fluent API to FFMPEG (http://www.ffmpeg.org)

[![NPM](https://nodei.co/npm/fluent-ffmpeg.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fluent-ffmpeg)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Stefan Schaermeli"
    },
    "bugs": {
        "url": "http://github.com/fluent-ffmpeg/node-fluent-ffmpeg/issues"
    },
    "contributors": [
        {
            "name": "Felix Fichte"
        }
    ],
    "dependencies": {
        "async": ">=0.2.9",
        "which": "^1.1.1"
    },
    "description": "A fluent API to FFMPEG (http://www.ffmpeg.org)",
    "devDependencies": {
        "jsdoc": "latest",
        "mocha": "latest",
        "should": "latest"
    },
    "directories": {},
    "dist": {
        "shasum": "e6ab85e75ba8e49119a3900cd9df10d39831d392",
        "tarball": "https://registry.npmjs.org/fluent-ffmpeg/-/fluent-ffmpeg-2.1.0.tgz"
    },
    "engines": {
        "node": ">=0.8.0"
    },
    "gitHead": "012d5d288d9233c46b4c08fedb85584475b8bde7",
    "homepage": "https://github.com/fluent-ffmpeg/node-fluent-ffmpeg#readme",
    "keywords": [
        "ffmpeg"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "schaermu"
        },
        {
            "name": "spruce"
        },
        {
            "name": "bencevans"
        },
        {
            "name": "njoyard"
        }
    ],
    "name": "fluent-ffmpeg",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/fluent-ffmpeg/node-fluent-ffmpeg.git"
    },
    "scripts": {
        "test": "make test"
    },
    "version": "2.1.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module fluent-ffmpeg](#apidoc.module.fluent-ffmpeg)
1.  [function <span class="apidocSignatureSpan"></span>fluent-ffmpeg (input, options)](#apidoc.element.fluent-ffmpeg.fluent-ffmpeg)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableCodecs (callback)](#apidoc.element.fluent-ffmpeg.availableCodecs)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableFilters (callback)](#apidoc.element.fluent-ffmpeg.availableFilters)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableFormats (callback)](#apidoc.element.fluent-ffmpeg.availableFormats)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>ffprobe (file)](#apidoc.element.fluent-ffmpeg.ffprobe)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableCodecs (callback)](#apidoc.element.fluent-ffmpeg.getAvailableCodecs)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableFilters (callback)](#apidoc.element.fluent-ffmpeg.getAvailableFilters)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableFormats (callback)](#apidoc.element.fluent-ffmpeg.getAvailableFormats)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFfmpegPath (path)](#apidoc.element.fluent-ffmpeg.setFfmpegPath)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFfprobePath (path)](#apidoc.element.fluent-ffmpeg.setFfprobePath)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFlvtoolPath (path)](#apidoc.element.fluent-ffmpeg.setFlvtoolPath)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>super_ ()](#apidoc.element.fluent-ffmpeg.super_)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>toString ()](#apidoc.element.fluent-ffmpeg.toString)



# <a name="apidoc.module.fluent-ffmpeg"></a>[module fluent-ffmpeg](#apidoc.module.fluent-ffmpeg)

#### <a name="apidoc.element.fluent-ffmpeg.fluent-ffmpeg"></a>[function <span class="apidocSignatureSpan"></span>fluent-ffmpeg (input, options)](#apidoc.element.fluent-ffmpeg.fluent-ffmpeg)
- description and source-code
```javascript
function FfmpegCommand(input, options) {
  // Make 'new' optional
  if (!(this instanceof FfmpegCommand)) {
    return new FfmpegCommand(input, options);
  }

  EventEmitter.call(this);

  if (typeof input === 'object' && !('readable' in input)) {
    // Options object passed directly
    options = input;
  } else {
    // Input passed first
    options = options || {};
    options.source = input;
  }

  // Add input if present
  this._inputs = [];
  if (options.source) {
    this.input(options.source);
  }

  // Add target-less output for backwards compatibility
  this._outputs = [];
  this.output();

  // Create argument lists
  var self = this;
  ['_global', '_complexFilters'].forEach(function(prop) {
    self[prop] = utils.args();
  });

  // Set default option values
  options.stdoutLines = 'stdoutLines' in options ? options.stdoutLines : 100;
  options.presets = options.presets || options.preset || path.join(__dirname, 'presets');
  options.niceness = options.niceness || options.priority || 0;

  // Save options
  this.options = options;

  // Setup logger
  this.logger = options.logger || {
    debug: function() {},
    info: function() {},
    warn: function() {},
    error: function() {}
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fluent-ffmpeg.availableCodecs"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableCodecs (callback)](#apidoc.element.fluent-ffmpeg.availableCodecs)
- description and source-code
```javascript
availableCodecs = function (callback) {
  (new FfmpegCommand()).availableCodecs(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fluent-ffmpeg.availableFilters"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableFilters (callback)](#apidoc.element.fluent-ffmpeg.availableFilters)
- description and source-code
```javascript
availableFilters = function (callback) {
  (new FfmpegCommand()).availableFilters(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fluent-ffmpeg.availableFormats"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>availableFormats (callback)](#apidoc.element.fluent-ffmpeg.availableFormats)
- description and source-code
```javascript
availableFormats = function (callback) {
  (new FfmpegCommand()).availableFormats(callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fluent-ffmpeg.ffprobe"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>ffprobe (file)](#apidoc.element.fluent-ffmpeg.ffprobe)
- description and source-code
```javascript
ffprobe = function (file) {
  var instance = new FfmpegCommand(file);
  instance.ffprobe.apply(instance, Array.prototype.slice.call(arguments, 1));
}
```
- example usage
```shell
...


### Reading video metadata

You can read metadata from any valid ffmpeg input file with the modules 'ffprobe' method.

'''js
ffmpeg.ffprobe('/path/to/file.avi', function(err, metadata) {
    console.dir(metadata);
});
'''

You may also call the ffprobe method on an FfmpegCommand to probe one of its input.  You may pass a 0-based input number as a first
 argument to specify which input to read metadata from, otherwise the method will probe the last added input.

'''js
...
```

#### <a name="apidoc.element.fluent-ffmpeg.getAvailableCodecs"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableCodecs (callback)](#apidoc.element.fluent-ffmpeg.getAvailableCodecs)
- description and source-code
```javascript
getAvailableCodecs = function (callback) {
  (new FfmpegCommand()).availableCodecs(callback);
}
```
- example usage
```shell
...
var Ffmpeg = require('fluent-ffmpeg');

Ffmpeg.getAvailableFormats(function(err, formats) {
console.log('Available formats:');
console.dir(formats);
});

Ffmpeg.getAvailableCodecs(function(err, codecs) {
console.log('Available codecs:');
console.dir(codecs);
});

Ffmpeg.getAvailableEncoders(function(err, encoders) {
console.log('Available encoders:');
console.dir(encoders);
...
```

#### <a name="apidoc.element.fluent-ffmpeg.getAvailableFilters"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableFilters (callback)](#apidoc.element.fluent-ffmpeg.getAvailableFilters)
- description and source-code
```javascript
getAvailableFilters = function (callback) {
  (new FfmpegCommand()).availableFilters(callback);
}
```
- example usage
```shell
...
});

Ffmpeg.getAvailableEncoders(function(err, encoders) {
console.log('Available encoders:');
console.dir(encoders);
});

Ffmpeg.getAvailableFilters(function(err, filters) {
console.log("Available filters:");
console.dir(filters);
});

// Those methods can also be called on commands
new Ffmpeg({ source: '/path/to/file.avi' })
.getAvailableCodecs(...);
...
```

#### <a name="apidoc.element.fluent-ffmpeg.getAvailableFormats"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>getAvailableFormats (callback)](#apidoc.element.fluent-ffmpeg.getAvailableFormats)
- description and source-code
```javascript
getAvailableFormats = function (callback) {
  (new FfmpegCommand()).availableFormats(callback);
}
```
- example usage
```shell
...

fluent-ffmpeg enables you to query your installed ffmpeg version for supported formats, codecs, encoders and filters.

'''js

var Ffmpeg = require('fluent-ffmpeg');

Ffmpeg.getAvailableFormats(function(err, formats) {
console.log('Available formats:');
console.dir(formats);
});

Ffmpeg.getAvailableCodecs(function(err, codecs) {
console.log('Available codecs:');
console.dir(codecs);
...
```

#### <a name="apidoc.element.fluent-ffmpeg.setFfmpegPath"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFfmpegPath (path)](#apidoc.element.fluent-ffmpeg.setFfmpegPath)
- description and source-code
```javascript
setFfmpegPath = function (path) {
  (new FfmpegCommand()).setFfmpegPath(path);
}
```
- example usage
```shell
...

If you intend to encode FLV videos, you must have either flvtool2 or flvmeta installed and in your 'PATH' or fluent-ffmpeg won't
 be able to produce streamable output files.  If you set either the 'FLVTOOL2_PATH' or 'FLVMETA_PATH', fluent-ffmpeg will try to
 use it instead of searching in the 'PATH'.

#### Setting binary paths manually

Alternatively, you may set the ffmpeg, ffprobe and flvtool2/flvmeta binary paths manually by using the following API commands:

* **Ffmpeg.setFfmpegPath(path)** Argument 'path' is a string with the full path to the ffmpeg binary.
* **Ffmpeg.setFfprobePath(path)** Argument 'path' is a string with the full path to the ffprobe binary.
* **Ffmpeg.setFlvtoolPath(path)** Argument 'path' is a string with the full path to the flvtool2 or flvmeta binary.


### Creating an FFmpeg command

The fluent-ffmpeg module returns a constructor that you can use to instanciate FFmpeg commands.
...
```

#### <a name="apidoc.element.fluent-ffmpeg.setFfprobePath"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFfprobePath (path)](#apidoc.element.fluent-ffmpeg.setFfprobePath)
- description and source-code
```javascript
setFfprobePath = function (path) {
  (new FfmpegCommand()).setFfprobePath(path);
}
```
- example usage
```shell
...
If you intend to encode FLV videos, you must have either flvtool2 or flvmeta installed and in your 'PATH' or fluent-ffmpeg won't
 be able to produce streamable output files.  If you set either the 'FLVTOOL2_PATH' or 'FLVMETA_PATH', fluent-ffmpeg will try to
 use it instead of searching in the 'PATH'.

#### Setting binary paths manually

Alternatively, you may set the ffmpeg, ffprobe and flvtool2/flvmeta binary paths manually by using the following API commands:

* **Ffmpeg.setFfmpegPath(path)** Argument 'path' is a string with the full path to the ffmpeg binary.
* **Ffmpeg.setFfprobePath(path)** Argument 'path' is a string with the full path to the ffprobe binary.
* **Ffmpeg.setFlvtoolPath(path)** Argument 'path' is a string with the full path to the flvtool2 or flvmeta binary.


### Creating an FFmpeg command

The fluent-ffmpeg module returns a constructor that you can use to instanciate FFmpeg commands.
...
```

#### <a name="apidoc.element.fluent-ffmpeg.setFlvtoolPath"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>setFlvtoolPath (path)](#apidoc.element.fluent-ffmpeg.setFlvtoolPath)
- description and source-code
```javascript
setFlvtoolPath = function (path) {
  (new FfmpegCommand()).setFlvtoolPath(path);
}
```
- example usage
```shell
...

#### Setting binary paths manually

Alternatively, you may set the ffmpeg, ffprobe and flvtool2/flvmeta binary paths manually by using the following API commands:

* **Ffmpeg.setFfmpegPath(path)** Argument 'path' is a string with the full path to the ffmpeg binary.
* **Ffmpeg.setFfprobePath(path)** Argument 'path' is a string with the full path to the ffprobe binary.
* **Ffmpeg.setFlvtoolPath(path)** Argument 'path' is a string with the full path to the flvtool2 or flvmeta binary.


### Creating an FFmpeg command

The fluent-ffmpeg module returns a constructor that you can use to instanciate FFmpeg commands.

'''js
...
```

#### <a name="apidoc.element.fluent-ffmpeg.super_"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>super_ ()](#apidoc.element.fluent-ffmpeg.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.fluent-ffmpeg.toString"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.</span>toString ()](#apidoc.element.fluent-ffmpeg.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
