# npmdoc-sinopia

#### api documentation for  [sinopia (v1.4.0)](https://github.com/rlidwka/sinopia)  [![npm package](https://img.shields.io/npm/v/npmdoc-sinopia.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sinopia) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sinopia.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sinopia)

#### Private npm repository server

[![NPM](https://nodei.co/npm/sinopia.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sinopia)

- [https://npmdoc.github.io/node-npmdoc-sinopia/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sinopia/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sinopia/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sinopia/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sinopia/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sinopia/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Alex Kocharin"
    },
    "bin": {
        "sinopia": "./bin/sinopia"
    },
    "bugs": {
        "url": "https://github.com/rlidwka/sinopia/issues"
    },
    "dependencies": {
        "JSONStream": "1.x",
        "async": ">=0.9.0 <1.0.0-0",
        "body-parser": ">=1.9.2 <2.0.0-0",
        "bunyan": ">=0.22.1 <2.0.0-0",
        "commander": ">=2.3.0 <3.0.0-0",
        "compression": ">=1.2.0 <2.0.0-0",
        "cookies": ">=0.5.0 <1.0.0-0",
        "crypt3": ">=0.1.6 <1.0.0-0",
        "es6-shim": "0.21.x",
        "express": ">=5.0.0-0 <6.0.0-0",
        "express-json5": ">=0.1.0 <1.0.0-0",
        "fs-ext": ">=0.4.1 <1.0.0-0",
        "handlebars": "2.x",
        "highlight.js": "8.x",
        "http-errors": ">=1.2.0",
        "jju": "1.x",
        "js-yaml": ">=3.0.1 <4.0.0-0",
        "lunr": ">=0.5.2 <1.0.0-0",
        "minimatch": ">=0.2.14 <2.0.0-0",
        "mkdirp": ">=0.3.5 <1.0.0-0",
        "readable-stream": "~1.1.0",
        "render-readme": ">=0.2.1",
        "request": ">=2.31.0 <3.0.0-0",
        "semver": ">=2.2.1 <5.0.0-0",
        "sinopia-htpasswd": ">= 0.4.3"
    },
    "description": "Private npm repository server",
    "devDependencies": {
        "bluebird": "2 >=2.9",
        "browserify": "7.x",
        "browserify-handlebars": "1.x",
        "eslint": ">= 0.18",
        "grunt": ">=0.4.4 <1.0.0-0",
        "grunt-browserify": ">=2.0.8 <3.0.0-0",
        "grunt-cli": "*",
        "grunt-contrib-less": ">=0.11.0 <1.0.0-0",
        "grunt-contrib-watch": ">=0.6.1 <1.0.0-0",
        "mocha": "2 >=2.2.3",
        "onclick": ">=0.1.0 <1.0.0-0",
        "rimraf": ">=2.2.5 <3.0.0-0",
        "transition-complete": ">=0.0.2 <1.0.0-0",
        "unopinionate": ">=0.0.4 <1.0.0-0"
    },
    "directories": {},
    "dist": {
        "shasum": "36bf5209356facbf6cef18fa32274d116043ed24",
        "tarball": "https://registry.npmjs.org/sinopia/-/sinopia-1.4.0.tgz"
    },
    "engines": {
        "node": ">=0.10"
    },
    "gitHead": "93245c0179524874fea574db1da48d1c68e6d0a2",
    "homepage": "https://github.com/rlidwka/sinopia",
    "keywords": [
        "private",
        "package",
        "repository",
        "registry",
        "modules",
        "proxy",
        "server"
    ],
    "license": {
        "type": "WTFPL",
        "url": "http://www.wtfpl.net/txt/copying/"
    },
    "main": "index.js",
    "maintainers": [
        {
            "name": "rlidwka"
        }
    ],
    "name": "sinopia",
    "optionalDependencies": {
        "crypt3": ">=0.1.6 <1.0.0-0",
        "fs-ext": ">=0.4.1 <1.0.0-0"
    },
    "preferGlobal": true,
    "publishConfig": {
        "registry": "https://registry.npmjs.org/"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/rlidwka/sinopia.git"
    },
    "scripts": {
        "clean-shrinkwrap": "node -e '\n  function clean(j) {\n    if (!j) return\n    for (var k in j) {\n      delete j[k].from\n      delete j[k].resolved\n      if (j[k].dependencies) clean(j[k].dependencies)\n    }\n  }\n  x = JSON.parse(require(\"fs\").readFileSync(\"./npm-shrinkwrap.json\"))\n  clean(x.dependencies)\n  x = JSON.stringify(x, null, \"  \")\n  require(\"fs\").writeFileSync(\"./npm-shrinkwrap.json\", x + \"\\n\")\n'\n",
        "lint": "eslint --reset .",
        "prepublish": "js-yaml package.yaml > package.json",
        "test": "eslint --reset . && mocha ./test/functional ./test/unit",
        "test-only": "mocha ./test/functional ./test/unit",
        "test-travis": "eslint --reset . && mocha -R spec ./test/functional ./test/unit"
    },
    "version": "1.4.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
