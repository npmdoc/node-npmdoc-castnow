# api documentation for  [castnow (v0.4.18)](https://github.com/xat/castnow#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-castnow.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-castnow) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-castnow.svg)](https://travis-ci.org/npmdoc/node-npmdoc-castnow)
#### commandline chromecast player

[![NPM](https://nodei.co/npm/castnow.png?downloads=true)](https://www.npmjs.com/package/castnow)

[![apidoc](https://npmdoc.github.io/node-npmdoc-castnow/build/screenCapture.buildNpmdoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-castnow%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-castnow/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-castnow/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-castnow/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Simon Kusterer"
    },
    "bin": {
        "castnow": "./index.js"
    },
    "bugs": {
        "url": "https://github.com/xat/castnow/issues"
    },
    "dependencies": {
        "array-loop": "^1.0.0",
        "array-shuffle": "^1.0.1",
        "castv2-client": "^1.1.0",
        "chalk": "1.0.0",
        "chromecast-player": "^0.2.3",
        "debounced-seeker": "^1.0.0",
        "debug": "^2.1.0",
        "diveSync": "^0.3.0",
        "got": "^1.2.2",
        "internal-ip": "^1.0.0",
        "keypress": "^0.2.1",
        "mime": "^1.2.11",
        "minimist": "^1.1.0",
        "peerflix": "^0.34.0",
        "playerui": "^1.2.0",
        "query-string": "^1.0.0",
        "range-parser": "^1.0.2",
        "read-torrent": "^1.0.0",
        "router": "^0.6.2",
        "srt2vtt": "^1.3.1",
        "stream-transcoder": "0.0.5",
        "xml2js": "^0.4.4",
        "xspfr": "^0.3.1",
        "xtend": "^4.0.0"
    },
    "description": "commandline chromecast player",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "4ffd81c55f381a5aa10c637607683a196830bdd8",
        "tarball": "https://registry.npmjs.org/castnow/-/castnow-0.4.18.tgz"
    },
    "gitHead": "9a09de90432dc126920a07fa48b31160cdb9b7db",
    "homepage": "https://github.com/xat/castnow#readme",
    "keywords": [
        "chromecast",
        "media",
        "player",
        "video",
        "torrent",
        "peerflix",
        "commandline",
        "subtitles",
        "cast"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "xat",
            "email": "simon@soped.com"
        }
    ],
    "name": "castnow",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/xat/castnow.git"
    },
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "version": "0.4.18"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module castnow](#apidoc.module.castnow)
1.  [function <span class="apidocSignatureSpan">castnow.</span>attach ()](#apidoc.element.castnow.attach)
1.  [function <span class="apidocSignatureSpan">castnow.</span>launch ()](#apidoc.element.castnow.launch)
1.  [function <span class="apidocSignatureSpan">castnow.</span>use ()](#apidoc.element.castnow.use)
1.  number <span class="apidocSignatureSpan">castnow.</span>_eventsCount
1.  object <span class="apidocSignatureSpan">castnow.</span>_events
1.  object <span class="apidocSignatureSpan">castnow.</span>domain
1.  object <span class="apidocSignatureSpan">castnow.</span>mw



# <a name="apidoc.module.castnow"></a>[module castnow](#apidoc.module.castnow)

#### <a name="apidoc.element.castnow.attach"></a>[function <span class="apidocSignatureSpan">castnow.</span>attach ()](#apidoc.element.castnow.attach)
- description and source-code
```javascript
attach = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  var sig = (function () {
    var ret = [];
    for (var i = 0, len = args.length; i < len; i++) {
      ret.push(toType(args[i]));
    }
    return ret;
  })().join('::');

  if (map[sig]) {
    if (map[sig].inject) args.unshift(input);
    return map[sig].fn.apply(ctx || null, args);
  }

  return input && input.apply(ctx || null, args);
}
```
- example usage
```shell
...
var file = ctx.options.playlist.shift();
if (ctx.options.loop) ctx.options.playlist.push(file);
next();
});

if (!opts.playlist) {
debug('attaching...');
player.attach(opts, ctrl);
} else {
debug('launching...');
player.launch(opts, ctrl);
}

process.on('SIGINT', function() {
process.exit();
...
```

#### <a name="apidoc.element.castnow.launch"></a>[function <span class="apidocSignatureSpan">castnow.</span>launch ()](#apidoc.element.castnow.launch)
- description and source-code
```javascript
launch = function () {
  var args = Array.prototype.slice.call(arguments, 0);
  var sig = (function () {
    var ret = [];
    for (var i = 0, len = args.length; i < len; i++) {
      ret.push(toType(args[i]));
    }
    return ret;
  })().join('::');

  if (map[sig]) {
    if (map[sig].inject) args.unshift(input);
    return map[sig].fn.apply(ctx || null, args);
  }

  return input && input.apply(ctx || null, args);
}
```
- example usage
```shell
...
});

if (!opts.playlist) {
  debug('attaching...');
  player.attach(opts, ctrl);
} else {
  debug('launching...');
  player.launch(opts, ctrl);
}

process.on('SIGINT', function() {
  process.exit();
});

process.on('exit', function() {
...
```

#### <a name="apidoc.element.castnow.use"></a>[function <span class="apidocSignatureSpan">castnow.</span>use ()](#apidoc.element.castnow.use)
- description and source-code
```javascript
use = function () { [native code] }
```
- example usage
```shell
...
    inter = setInterval(function() {
      ui.setLabel('state', 'State', capitalize(status) + dots());
      ui.render();
    }, 300);
  };
})();

player.use(function(ctx, next) {
  ctx.on('status', logState);
  next();
});

player.use(stdin);
player.use(directories);
player.use(torrent);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
