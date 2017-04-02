# api documentation for  [fluent-ffmpeg (v2.1.0)](https://github.com/fluent-ffmpeg/node-fluent-ffmpeg#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-fluent-ffmpeg.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fluent-ffmpeg) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fluent-ffmpeg.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fluent-ffmpeg)
#### A fluent API to FFMPEG (http://www.ffmpeg.org)

[![NPM](https://nodei.co/npm/fluent-ffmpeg.png?downloads=true)](https://www.npmjs.com/package/fluent-ffmpeg)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-fluent-ffmpeg_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-fluent-ffmpeg/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Stefan Schaermeli",
        "email": "schaermu@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/fluent-ffmpeg/node-fluent-ffmpeg/issues"
    },
    "contributors": [
        {
            "name": "Felix Fichte",
            "email": "spruce@space-ships.de"
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
            "name": "schaermu",
            "email": "schaermu@gmail.com"
        },
        {
            "name": "spruce",
            "email": "spruce@space-ships.de"
        },
        {
            "name": "bencevans",
            "email": "ben@bensbit.co.uk"
        },
        {
            "name": "njoyard",
            "email": "joyard.nicolas@gmail.com"
        }
    ],
    "name": "fluent-ffmpeg",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
1.  object <span class="apidocSignatureSpan">fluent-ffmpeg.</span>jsdoc_aliases
1.  object <span class="apidocSignatureSpan">fluent-ffmpeg.</span>utils

#### [module fluent-ffmpeg.jsdoc_aliases](#apidoc.module.fluent-ffmpeg.jsdoc_aliases)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.jsdoc_aliases.</span>defineTags (dict)](#apidoc.element.fluent-ffmpeg.jsdoc_aliases.defineTags)
1.  object <span class="apidocSignatureSpan">fluent-ffmpeg.jsdoc_aliases.</span>handlers

#### [module fluent-ffmpeg.utils](#apidoc.module.fluent-ffmpeg.utils)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>args ()](#apidoc.element.fluent-ffmpeg.utils.args)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>copy (source, dest)](#apidoc.element.fluent-ffmpeg.utils.copy)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractCodecData (command, stderrLine, codecsObject)](#apidoc.element.fluent-ffmpeg.utils.extractCodecData)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractError (stderr)](#apidoc.element.fluent-ffmpeg.utils.extractError)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractProgress (command, stderrLine, duration)](#apidoc.element.fluent-ffmpeg.utils.extractProgress)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>linesRing (maxLines)](#apidoc.element.fluent-ffmpeg.utils.linesRing)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>makeFilterStrings (filters)](#apidoc.element.fluent-ffmpeg.utils.makeFilterStrings)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>timemarkToSeconds (timemark)](#apidoc.element.fluent-ffmpeg.utils.timemarkToSeconds)
1.  [function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>which (name, callback)](#apidoc.element.fluent-ffmpeg.utils.which)
1.  object <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>isWindows
1.  object <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>streamRegexp



# <a name="apidoc.module.fluent-ffmpeg"></a>[module fluent-ffmpeg](#apidoc.module.fluent-ffmpeg)

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
...
   * @private
   */
  proto._checkCapabilities = function(callback) {
    var self = this;
    async.waterfall([
      // Get available formats
      function(cb) {
self.availableFormats(cb);
      },

      // Check whether specified formats are available
      function(formats, cb) {
var unavailable;

// Output format(s)
...
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



# <a name="apidoc.module.fluent-ffmpeg.jsdoc_aliases"></a>[module fluent-ffmpeg.jsdoc_aliases](#apidoc.module.fluent-ffmpeg.jsdoc_aliases)

#### <a name="apidoc.element.fluent-ffmpeg.jsdoc_aliases.defineTags"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.jsdoc_aliases.</span>defineTags (dict)](#apidoc.element.fluent-ffmpeg.jsdoc_aliases.defineTags)
- description and source-code
```javascript
defineTags = function (dict) {
	dict.defineTag('aliases', {
		onTagged: function(doclet, tag) {
			doclet.aliases = tag.text.split(',');
		}
	});

	dict.defineTag('category', {
		onTagged: function(doclet, tag) {
			doclet.category = tag.text;
		}
	});
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.fluent-ffmpeg.utils"></a>[module fluent-ffmpeg.utils](#apidoc.module.fluent-ffmpeg.utils)

#### <a name="apidoc.element.fluent-ffmpeg.utils.args"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>args ()](#apidoc.element.fluent-ffmpeg.utils.args)
- description and source-code
```javascript
args = function () {
  var list = [];

  // Append argument(s) to the list
  var argfunc = function() {
    if (arguments.length === 1 && Array.isArray(arguments[0])) {
      list = list.concat(arguments[0]);
    } else {
      list = list.concat([].slice.call(arguments));
    }
  };

  // Clear argument list
  argfunc.clear = function() {
    list = [];
  };

  // Return argument list
  argfunc.get = function() {
    return list;
  };

  // Find argument 'arg' in list, and if found, return an array of the 'count' items that follow it
  argfunc.find = function(arg, count) {
    var index = list.indexOf(arg);
    if (index !== -1) {
      return list.slice(index + 1, index + 1 + (count || 0));
    }
  };

  // Find argument 'arg' in list, and if found, remove it as well as the 'count' items that follow it
  argfunc.remove = function(arg, count) {
    var index = list.indexOf(arg);
    if (index !== -1) {
      list.splice(index, (count || 0) + 1);
    }
  };

  // Clone argument list
  argfunc.clone = function() {
    var cloned = utils.args();
    cloned(list);
    return cloned;
  };

  return argfunc;
}
```
- example usage
```shell
...
    if (index !== -1) {
      list.splice(index, (count || 0) + 1);
    }
  };

  // Clone argument list
  argfunc.clone = function() {
    var cloned = utils.args();
    cloned(list);
    return cloned;
  };

  return argfunc;
},
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.copy"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>copy (source, dest)](#apidoc.element.fluent-ffmpeg.utils.copy)
- description and source-code
```javascript
copy = function (source, dest) {
  Object.keys(source).forEach(function(key) {
    dest[key] = source[key];
  });
}
```
- example usage
```shell
...
          encoders = encoders ? encoders[1].trim().split(' ') : [];

          var decoders = codecData.description.match(ffDecodersRegexp);
          decoders = decoders ? decoders[1].trim().split(' ') : [];

          if (encoders.length || decoders.length) {
var coderData = {};
utils.copy(codecData, coderData);
delete coderData.canEncode;
delete coderData.canDecode;

encoders.forEach(function(name) {
  data[name] = {};
  utils.copy(coderData, data[name]);
  data[name].canEncode = true;
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.extractCodecData"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractCodecData (command, stderrLine, codecsObject)](#apidoc.element.fluent-ffmpeg.utils.extractCodecData)
- description and source-code
```javascript
extractCodecData = function (command, stderrLine, codecsObject) {
  var inputPattern = /Input #[0-9]+, ([^ ]+),/;
  var durPattern = /Duration\: ([^,]+)/;
  var audioPattern = /Audio\: (.*)/;
  var videoPattern = /Video\: (.*)/;

  if (!('inputStack' in codecsObject)) {
    codecsObject.inputStack = [];
    codecsObject.inputIndex = -1;
    codecsObject.inInput = false;
  }

  var inputStack = codecsObject.inputStack;
  var inputIndex = codecsObject.inputIndex;
  var inInput = codecsObject.inInput;

  var format, dur, audio, video;

  if (format = stderrLine.match(inputPattern)) {
    inInput = codecsObject.inInput = true;
    inputIndex = codecsObject.inputIndex = codecsObject.inputIndex + 1;

    inputStack[inputIndex] = { format: format[1], audio: '', video: '', duration: '' };
  } else if (inInput && (dur = stderrLine.match(durPattern))) {
    inputStack[inputIndex].duration = dur[1];
  } else if (inInput && (audio = stderrLine.match(audioPattern))) {
    audio = audio[1].split(', ');
    inputStack[inputIndex].audio = audio[0];
    inputStack[inputIndex].audio_details = audio;
  } else if (inInput && (video = stderrLine.match(videoPattern))) {
    video = video[1].split(', ');
    inputStack[inputIndex].video = video[0];
    inputStack[inputIndex].video_details = video;
  } else if (/Output #\d+/.test(stderrLine)) {
    inInput = codecsObject.inInput = false;
  } else if (/Stream mapping:|Press (\[q\]|ctrl-c) to stop/.test(stderrLine)) {
    command.emit.apply(command, ['codecData'].concat(inputStack));
    return true;
  }

  return false;
}
```
- example usage
```shell
...
// 'codecData' event
if (self.listeners('codecData').length) {
  var codecDataSent = false;
  var codecObject = {};

  stderrRing.callback(function(line) {
    if (!codecDataSent)
      codecDataSent = utils.extractCodecData(self, line, codecObject);
  });
}

// 'progress' event
if (self.listeners('progress').length) {
  var duration = 0;
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.extractError"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractError (stderr)](#apidoc.element.fluent-ffmpeg.utils.extractError)
- description and source-code
```javascript
extractError = function (stderr) {
  // Only return the last stderr lines that don't start with a space or a square bracket
  return stderr.split(nlRegexp).reduce(function(messages, message) {
    if (message.charAt(0) === ' ' || message.charAt(0) === '[') {
      return [];
    } else {
      messages.push(message);
      return messages;
    }
  }, []).join('\n');
}
```
- example usage
```shell
...

        function endCB(err, stdoutRing, stderrRing) {
delete self.ffmpegProc;

if (err) {
  if (err.message.match(/ffmpeg exited with code/)) {
    // Add ffmpeg error message
    err.message += ': ' + utils.extractError(stderrRing.get());
  }

  emitEnd(err, stdoutRing.get(), stderrRing.get());
} else {
  // Find out which outputs need flv metadata
  var flvmeta = self._outputs.filter(function(output) {
    return output.flags.flvmeta;
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.extractProgress"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>extractProgress (command, stderrLine, duration)](#apidoc.element.fluent-ffmpeg.utils.extractProgress)
- description and source-code
```javascript
extractProgress = function (command, stderrLine, duration) {
  var progress = parseProgressLine(stderrLine);

  if (progress) {
    // build progress report object
    var ret = {
      frames: parseInt(progress.frame, 10),
      currentFps: parseInt(progress.fps, 10),
      currentKbps: progress.bitrate ? parseFloat(progress.bitrate.replace('kbits/s', '')) : 0,
      targetSize: parseInt(progress.size, 10),
      timemark: progress.time
    };

    // calculate percent progress using duration
    if (duration && duration > 0) {
      ret.percent = (utils.timemarkToSeconds(ret.timemark) / duration) * 100;
    }

    command.emit('progress', ret);
  }
}
```
- example usage
```shell
...
      var duration = 0;

      if (self._ffprobeData && self._ffprobeData.format && self._ffprobeData.format.duration) {
        duration = Number(self._ffprobeData.format.duration);
      }

      stderrRing.callback(function(line) {
        utils.extractProgress(self, line, duration);
      });
    }
  }
},

function endCB(err, stdoutRing, stderrRing) {
  delete self.ffmpegProc;
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.linesRing"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>linesRing (maxLines)](#apidoc.element.fluent-ffmpeg.utils.linesRing)
- description and source-code
```javascript
linesRing = function (maxLines) {
  var cbs = [];
  var lines = [];
  var current = null;
  var closed = false
  var max = maxLines - 1;

  function emit(line) {
    cbs.forEach(function(cb) { cb(line); });
  }

  return {
    callback: function(cb) {
      lines.forEach(function(l) { cb(l); });
      cbs.push(cb);
    },

    append: function(str) {
      if (closed) return;
      if (str instanceof Buffer) str = '' + str;
      if (!str || str.length === 0) return;

      var newLines = str.split(nlRegexp);

      if (newLines.length === 1) {
        if (current !== null) {
          current = current + newLines.shift();
        } else {
          current = newLines.shift();
        }
      } else {
        if (current !== null) {
          current = current + newLines.shift();
          emit(current);
          lines.push(current);
        }

        current = newLines.pop();

        newLines.forEach(function(l) {
          emit(l);
          lines.push(l);
        });

        if (max > -1 && lines.length > max) {
          lines.splice(0, lines.length - max);
        }
      }
    },

    get: function() {
      if (current !== null) {
        return lines.concat([current]).join('\n');
      } else {
        return lines.join('\n');
      }
    },

    close: function() {
      if (closed) return;

      if (current !== null) {
        emit(current);
        lines.push(current);

        if (max > -1 && lines.length > max) {
          lines.shift();
        }

        current = null;
      }

      closed = true;
    }
  };
}
```
- example usage
```shell
...

// Apply niceness
if (options.niceness && options.niceness !== 0 && !utils.isWindows) {
  args.unshift('-n', options.niceness, command);
  command = 'nice';
}

var stdoutRing = utils.linesRing(maxLines);
var stdoutClosed = false;

var stderrRing = utils.linesRing(maxLines);
var stderrClosed = false;

// Spawn process
var ffmpegProc = spawn(command, args, options);
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.makeFilterStrings"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>makeFilterStrings (filters)](#apidoc.element.fluent-ffmpeg.utils.makeFilterStrings)
- description and source-code
```javascript
makeFilterStrings = function (filters) {
  return filters.map(function(filterSpec) {
    if (typeof filterSpec === 'string') {
      return filterSpec;
    }

    var filterString = '';

    // Filter string format is:
    // [input1][input2]...filter[output1][output2]...
    // The 'filter' part can optionaly have arguments:
    //   filter=arg1:arg2:arg3
    //   filter=arg1=v1:arg2=v2:arg3=v3

    // Add inputs
    if (Array.isArray(filterSpec.inputs)) {
      filterString += filterSpec.inputs.map(function(streamSpec) {
        return streamSpec.replace(streamRegexp, '[$1]');
      }).join('');
    } else if (typeof filterSpec.inputs === 'string') {
      filterString += filterSpec.inputs.replace(streamRegexp, '[$1]');
    }

    // Add filter
    filterString += filterSpec.filter;

    // Add options
    if (filterSpec.options) {
      if (typeof filterSpec.options === 'string' || typeof filterSpec.options === 'number') {
        // Option string
        filterString += '=' + filterSpec.options;
      } else if (Array.isArray(filterSpec.options)) {
        // Option array (unnamed options)
        filterString += '=' + filterSpec.options.map(function(option) {
          if (typeof option === 'string' && option.match(filterEscapeRegexp)) {
            return '\'' + option + '\'';
          } else {
            return option;
          }
        }).join(':');
      } else if (Object.keys(filterSpec.options).length) {
        // Option object (named options)
        filterString += '=' + Object.keys(filterSpec.options).map(function(option) {
          var value = filterSpec.options[option];

          if (typeof value === 'string' && value.match(filterEscapeRegexp)) {
            value = '\'' + value + '\'';
          }

          return option + '=' + value;
        }).join(':');
      }
    }

    // Add outputs
    if (Array.isArray(filterSpec.outputs)) {
      filterString += filterSpec.outputs.map(function(streamSpec) {
        return streamSpec.replace(streamRegexp, '[$1]');
      }).join('');
    } else if (typeof filterSpec.outputs === 'string') {
      filterString += filterSpec.outputs.replace(streamRegexp, '[$1]');
    }

    return filterString;
  });
}
```
- example usage
```shell
...
        fileOutput ? ['-y'] : [],

        // Complex filters
        complexFilters,

        // Outputs, filters and output options
        this._outputs.reduce(function(args, output) {
var sizeFilters = utils.makeFilterStrings(output.sizeFilters.get());
var audioFilters = output.audioFilters.get();
var videoFilters = output.videoFilters.get().concat(sizeFilters);
var outputArg;

if (!output.target) {
  outputArg = [];
} else if (typeof output.target === 'string') {
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.timemarkToSeconds"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>timemarkToSeconds (timemark)](#apidoc.element.fluent-ffmpeg.utils.timemarkToSeconds)
- description and source-code
```javascript
timemarkToSeconds = function (timemark) {
  if (typeof timemark === 'number') {
    return timemark;
  }

  if (timemark.indexOf(':') === -1 && timemark.indexOf('.') >= 0) {
    return Number(timemark);
  }

  var parts = timemark.split(':');

  // add seconds
  var secs = Number(parts.pop());

  if (parts.length) {
    // add minutes
    secs += Number(parts.pop()) * 60;
  }

  if (parts.length) {
    // add hours
    secs += Number(parts.pop()) * 3600;
  }

  return secs;
}
```
- example usage
```shell
...
    next();
  }
},

// Turn all timemarks into numbers and sort them
function normalizeTimemarks(next) {
  config.timemarks = config.timemarks.map(function(mark) {
    return utils.timemarkToSeconds(mark);
  }).sort(function(a, b) { return a - b; });

  next();
},

// Add '_%i' to pattern when requesting multiple screenshots and no variable token is present
function fixPattern(next) {
...
```

#### <a name="apidoc.element.fluent-ffmpeg.utils.which"></a>[function <span class="apidocSignatureSpan">fluent-ffmpeg.utils.</span>which (name, callback)](#apidoc.element.fluent-ffmpeg.utils.which)
- description and source-code
```javascript
which = function (name, callback) {
  if (name in whichCache) {
    return callback(null, whichCache[name]);
  }

  which(name, function(err, result){
    if (err) {
      // Treat errors as not found
      return callback(null, whichCache[name] = '');
    }
    callback(null, whichCache[name] = result);
  });
}
```
- example usage
```shell
...

  // Search in the PATH
  function(ffmpeg, cb) {
    if (ffmpeg.length) {
      return cb(null, ffmpeg);
    }

    utils.which('ffmpeg', function(err, ffmpeg) {
      cb(err, ffmpeg);
    });
  }
], function(err, ffmpeg) {
  if (err) {
    callback(err);
  } else {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
