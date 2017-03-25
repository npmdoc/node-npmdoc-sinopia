# api documentation for  [sinopia (v1.4.0)](https://github.com/rlidwka/sinopia)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sinopia.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sinopia)
#### Private npm repository server

[![NPM](https://nodei.co/npm/sinopia.png?downloads=true)](https://www.npmjs.com/package/sinopia)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sinopia/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sinopia_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sinopia/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-sinopia/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Alex Kocharin",
        "email": "alex@kocharin.ru"
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
            "name": "rlidwka",
            "email": "alex@kocharin.ru"
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
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sinopia](#apidoc.module.sinopia)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>GUI (context, options)](#apidoc.element.sinopia.GUI)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>auth (config)](#apidoc.element.sinopia.auth)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>config (config)](#apidoc.element.sinopia.config)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>local_data (path)](#apidoc.element.sinopia.local_data)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>local_storage (config)](#apidoc.element.sinopia.local_storage)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>storage (config)](#apidoc.element.sinopia.storage)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>up_storage (config, mainconfig)](#apidoc.element.sinopia.up_storage)
1.  object <span class="apidocSignatureSpan">sinopia.</span>auth.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>config.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>local_data.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>local_fs
1.  object <span class="apidocSignatureSpan">sinopia.</span>local_storage.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>logger
1.  object <span class="apidocSignatureSpan">sinopia.</span>middleware
1.  object <span class="apidocSignatureSpan">sinopia.</span>plugin_loader
1.  object <span class="apidocSignatureSpan">sinopia.</span>status_cats
1.  object <span class="apidocSignatureSpan">sinopia.</span>storage.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>streams
1.  object <span class="apidocSignatureSpan">sinopia.</span>up_storage.prototype
1.  object <span class="apidocSignatureSpan">sinopia.</span>utils

#### [module sinopia.GUI](#apidoc.module.sinopia.GUI)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>GUI (context, options)](#apidoc.element.sinopia.GUI.GUI)
1.  [function <span class="apidocSignatureSpan">sinopia.GUI.</span>_child (i, data, depths)](#apidoc.element.sinopia.GUI._child)
1.  [function <span class="apidocSignatureSpan">sinopia.GUI.</span>_setup (options)](#apidoc.element.sinopia.GUI._setup)

#### [module sinopia.auth](#apidoc.module.sinopia.auth)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>auth (config)](#apidoc.element.sinopia.auth.auth)

#### [module sinopia.auth.prototype](#apidoc.module.sinopia.auth.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>add_user (user, password, cb)](#apidoc.element.sinopia.auth.prototype.add_user)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>aes_decrypt (buf)](#apidoc.element.sinopia.auth.prototype.aes_decrypt)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>aes_encrypt (buf)](#apidoc.element.sinopia.auth.prototype.aes_encrypt)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>allow_access (package_name, user, callback)](#apidoc.element.sinopia.auth.prototype.allow_access)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>allow_publish (package_name, user, callback)](#apidoc.element.sinopia.auth.prototype.allow_publish)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>authenticate (user, password, cb)](#apidoc.element.sinopia.auth.prototype.authenticate)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>basic_middleware ()](#apidoc.element.sinopia.auth.prototype.basic_middleware)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>bearer_middleware ()](#apidoc.element.sinopia.auth.prototype.bearer_middleware)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>cookie_middleware ()](#apidoc.element.sinopia.auth.prototype.cookie_middleware)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>decode_token (str, expire_time)](#apidoc.element.sinopia.auth.prototype.decode_token)
1.  [function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>issue_token (user)](#apidoc.element.sinopia.auth.prototype.issue_token)

#### [module sinopia.config](#apidoc.module.sinopia.config)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>config (config)](#apidoc.element.sinopia.config.config)
1.  [function <span class="apidocSignatureSpan">sinopia.config.</span>parse_interval (interval)](#apidoc.element.sinopia.config.parse_interval)

#### [module sinopia.config.prototype](#apidoc.module.sinopia.config.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.config.prototype.</span>can_proxy_to (package, uplink)](#apidoc.element.sinopia.config.prototype.can_proxy_to)
1.  [function <span class="apidocSignatureSpan">sinopia.config.prototype.</span>get_package_spec (package)](#apidoc.element.sinopia.config.prototype.get_package_spec)

#### [module sinopia.local_data](#apidoc.module.sinopia.local_data)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>local_data (path)](#apidoc.element.sinopia.local_data.local_data)

#### [module sinopia.local_data.prototype](#apidoc.module.sinopia.local_data.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>add (name)](#apidoc.element.sinopia.local_data.prototype.add)
1.  [function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>get ()](#apidoc.element.sinopia.local_data.prototype.get)
1.  [function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>remove (name)](#apidoc.element.sinopia.local_data.prototype.remove)
1.  [function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>sync ()](#apidoc.element.sinopia.local_data.prototype.sync)

#### [module sinopia.local_fs](#apidoc.module.sinopia.local_fs)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>create (name, contents, callback)](#apidoc.element.sinopia.local_fs.create)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>create_json (name, value, cb)](#apidoc.element.sinopia.local_fs.create_json)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>lock_and_read (name, _callback)](#apidoc.element.sinopia.local_fs.lock_and_read)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>lock_and_read_json (name, cb)](#apidoc.element.sinopia.local_fs.lock_and_read_json)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read (name, callback)](#apidoc.element.sinopia.local_fs.read)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read_json (name, cb)](#apidoc.element.sinopia.local_fs.read_json)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read_stream (name, stream, callback)](#apidoc.element.sinopia.local_fs.read_stream)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>rmdir (path, callback)](#apidoc.element.sinopia.local_fs.rmdir)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>unlink (path, callback)](#apidoc.element.sinopia.local_fs.unlink)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>update (name, contents, callback)](#apidoc.element.sinopia.local_fs.update)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>update_json (name, value, cb)](#apidoc.element.sinopia.local_fs.update_json)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write (dest, data, cb)](#apidoc.element.sinopia.local_fs.write)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write_json (name, value, cb)](#apidoc.element.sinopia.local_fs.write_json)
1.  [function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write_stream (name)](#apidoc.element.sinopia.local_fs.write_stream)

#### [module sinopia.local_storage](#apidoc.module.sinopia.local_storage)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>local_storage (config)](#apidoc.element.sinopia.local_storage.local_storage)

#### [module sinopia.local_storage.prototype](#apidoc.module.sinopia.local_storage.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_each_package (on_package, on_end)](#apidoc.element.sinopia.local_storage.prototype._each_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_internal_error (err, file, message)](#apidoc.element.sinopia.local_storage.prototype._internal_error)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_normalize_package (pkg)](#apidoc.element.sinopia.local_storage.prototype._normalize_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_read_create_package (name, callback)](#apidoc.element.sinopia.local_storage.prototype._read_create_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_write_package (name, json, callback)](#apidoc.element.sinopia.local_storage.prototype._write_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_package (name, info, callback)](#apidoc.element.sinopia.local_storage.prototype.add_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_tarball (name, filename)](#apidoc.element.sinopia.local_storage.prototype.add_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_version (name, version, metadata, tag, callback)](#apidoc.element.sinopia.local_storage.prototype.add_version)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>change_package (name, metadata, revision, callback)](#apidoc.element.sinopia.local_storage.prototype.change_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.local_storage.prototype.get_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>get_tarball (name, filename, callback)](#apidoc.element.sinopia.local_storage.prototype.get_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>merge_tags (name, tags, callback)](#apidoc.element.sinopia.local_storage.prototype.merge_tags)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>remove_package (name, callback)](#apidoc.element.sinopia.local_storage.prototype.remove_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>remove_tarball (name, filename, revision, callback)](#apidoc.element.sinopia.local_storage.prototype.remove_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>replace_tags (name, tags, callback)](#apidoc.element.sinopia.local_storage.prototype.replace_tags)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.local_storage.prototype.search)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>storage (package)](#apidoc.element.sinopia.local_storage.prototype.storage)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>update_package (name, updateFn, _callback)](#apidoc.element.sinopia.local_storage.prototype.update_package)
1.  [function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>update_versions (name, newdata, callback)](#apidoc.element.sinopia.local_storage.prototype.update_versions)

#### [module sinopia.logger](#apidoc.module.sinopia.logger)
1.  [function <span class="apidocSignatureSpan">sinopia.logger.</span>setup (logs)](#apidoc.element.sinopia.logger.setup)
1.  object <span class="apidocSignatureSpan">sinopia.</span>logger

#### [module sinopia.middleware](#apidoc.module.sinopia.middleware)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>allow (auth)](#apidoc.element.sinopia.middleware.allow)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>anti_loop (config)](#apidoc.element.sinopia.middleware.anti_loop)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>expect_json (req, res, next)](#apidoc.element.sinopia.middleware.expect_json)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>final (body, req, res, next)](#apidoc.element.sinopia.middleware.final)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>log (req, res, next)](#apidoc.element.sinopia.middleware.log)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>match (regexp)](#apidoc.element.sinopia.middleware.match)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>media (expect)](#apidoc.element.sinopia.middleware.media)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>validate_name (req, res, next, value, name)](#apidoc.element.sinopia.middleware.validate_name)
1.  [function <span class="apidocSignatureSpan">sinopia.middleware.</span>validate_package (req, res, next, value, name)](#apidoc.element.sinopia.middleware.validate_package)

#### [module sinopia.plugin_loader](#apidoc.module.sinopia.plugin_loader)
1.  [function <span class="apidocSignatureSpan">sinopia.plugin_loader.</span>load_plugins (config, plugin_configs, params, sanity_check)](#apidoc.element.sinopia.plugin_loader.load_plugins)

#### [module sinopia.status_cats](#apidoc.module.sinopia.status_cats)
1.  [function <span class="apidocSignatureSpan">sinopia.status_cats.</span>get_image (status)](#apidoc.element.sinopia.status_cats.get_image)
1.  [function <span class="apidocSignatureSpan">sinopia.status_cats.</span>middleware (req, res, next)](#apidoc.element.sinopia.status_cats.middleware)

#### [module sinopia.storage](#apidoc.module.sinopia.storage)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>storage (config)](#apidoc.element.sinopia.storage.storage)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.</span>_merge_versions (local, up, config)](#apidoc.element.sinopia.storage._merge_versions)

#### [module sinopia.storage.prototype](#apidoc.module.sinopia.storage.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>_sync_package_with_uplinks (name, pkginfo, options, callback)](#apidoc.element.sinopia.storage.prototype._sync_package_with_uplinks)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_package (name, metadata, callback)](#apidoc.element.sinopia.storage.prototype.add_package)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_tarball (name, filename)](#apidoc.element.sinopia.storage.prototype.add_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_version (name, version, metadata, tag, callback)](#apidoc.element.sinopia.storage.prototype.add_version)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>change_package (name, metadata, revision, callback)](#apidoc.element.sinopia.storage.prototype.change_package)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_local (callback)](#apidoc.element.sinopia.storage.prototype.get_local)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.storage.prototype.get_package)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_tarball (name, filename)](#apidoc.element.sinopia.storage.prototype.get_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>merge_tags (name, tag_hash, callback)](#apidoc.element.sinopia.storage.prototype.merge_tags)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>remove_package (name, callback)](#apidoc.element.sinopia.storage.prototype.remove_package)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>remove_tarball (name, filename, revision, callback)](#apidoc.element.sinopia.storage.prototype.remove_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>replace_tags (name, tag_hash, callback)](#apidoc.element.sinopia.storage.prototype.replace_tags)
1.  [function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.storage.prototype.search)

#### [module sinopia.streams](#apidoc.module.sinopia.streams)
1.  [function <span class="apidocSignatureSpan">sinopia.streams.</span>ReadTarballStream (options)](#apidoc.element.sinopia.streams.ReadTarballStream)
1.  [function <span class="apidocSignatureSpan">sinopia.streams.</span>UploadTarballStream (options)](#apidoc.element.sinopia.streams.UploadTarballStream)

#### [module sinopia.up_storage](#apidoc.module.sinopia.up_storage)
1.  [function <span class="apidocSignatureSpan">sinopia.</span>up_storage (config, mainconfig)](#apidoc.element.sinopia.up_storage.up_storage)

#### [module sinopia.up_storage.prototype](#apidoc.module.sinopia.up_storage.prototype)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>_add_proxy_headers (req, headers)](#apidoc.element.sinopia.up_storage.prototype._add_proxy_headers)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>can_fetch_url (url)](#apidoc.element.sinopia.up_storage.prototype.can_fetch_url)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.up_storage.prototype.get_package)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_tarball (name, options, filename)](#apidoc.element.sinopia.up_storage.prototype.get_tarball)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_url (url)](#apidoc.element.sinopia.up_storage.prototype.get_url)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>request (options, cb)](#apidoc.element.sinopia.up_storage.prototype.request)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.up_storage.prototype.search)
1.  [function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>status_check (alive)](#apidoc.element.sinopia.up_storage.prototype.status_check)

#### [module sinopia.utils](#apidoc.module.sinopia.utils)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>filter_tarball_urls (pkg, req, config)](#apidoc.element.sinopia.utils.filter_tarball_urls)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>get_version (object, version)](#apidoc.element.sinopia.utils.get_version)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>is_object (obj)](#apidoc.element.sinopia.utils.is_object)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>parse_address (addr)](#apidoc.element.sinopia.utils.parse_address)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>semver_sort (array)](#apidoc.element.sinopia.utils.semver_sort)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>tag_version (data, version, tag, config)](#apidoc.element.sinopia.utils.tag_version)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_metadata (object, name)](#apidoc.element.sinopia.utils.validate_metadata)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_name (name)](#apidoc.element.sinopia.utils.validate_name)
1.  [function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_package (name)](#apidoc.element.sinopia.utils.validate_package)



# <a name="apidoc.module.sinopia"></a>[module sinopia](#apidoc.module.sinopia)

#### <a name="apidoc.element.sinopia.GUI"></a>[function <span class="apidocSignatureSpan">sinopia.</span>GUI (context, options)](#apidoc.element.sinopia.GUI)
- description and source-code
```javascript
GUI = function (context, options) {
  if (!compiled) {
    compiled = compileInput();
  }
  return compiled.call(this, context, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.auth"></a>[function <span class="apidocSignatureSpan">sinopia.</span>auth (config)](#apidoc.element.sinopia.auth)
- description and source-code
```javascript
function Auth(config) {
  var self = Object.create(Auth.prototype)
  self.config = config
  self.logger = Logger.logger.child({ sub: 'auth' })
  self.secret = config.secret

  var plugin_params = {
    config: config,
    logger: self.logger
  }

  if (config.users_file) {
    if (!config.auth || !config.auth.htpasswd) {
      // b/w compat
      config.auth = config.auth || {}
      config.auth.htpasswd = { file: config.users_file }
    }
  }

  self.plugins = load_plugins(config, config.auth, plugin_params, function (p) {
    return p.authenticate || p.allow_access || p.allow_publish
  })

  self.plugins.unshift({
    sinopia_version: '1.1.0',

    authenticate: function(user, password, cb) {
      if (config.users != null
       && config.users[user] != null
       && (Crypto.createHash('sha1').update(password).digest('hex')
            === config.users[user].password)
      ) {
        return cb(null, [ user ])
      }

      return cb()
    },

    adduser: function(user, password, cb) {
      if (config.users && config.users[user])
        return cb( Error[403]('this user already exists') )

      return cb()
    },
  })

  function allow_action(action) {
    return function(user, package, cb) {
      var ok = package[action].reduce(function(prev, curr) {
        if (user.groups.indexOf(curr) !== -1) return true
        return prev
      }, false)

      if (ok) return cb(null, true)

      if (user.name) {
        cb( Error[403]('user ' + user.name + ' is not allowed to ' + action + ' package ' + package.name) )
      } else {
        cb( Error[403]('unregistered users are not allowed to ' + action + ' package ' + package.name) )
      }
    }
  }

  self.plugins.push({
    authenticate: function(user, password, cb) {
      return cb( Error[403]('bad username/password, access denied') )
    },

    add_user: function(user, password, cb) {
      return cb( Error[409]('registration is disabled') )
    },

    allow_access: allow_action('access'),
    allow_publish: allow_action('publish'),
  })

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.config"></a>[function <span class="apidocSignatureSpan">sinopia.</span>config (config)](#apidoc.element.sinopia.config)
- description and source-code
```javascript
function Config(config) {
  var self = Object.create(Config.prototype)
  for (var i in config) {
    if (self[i] == null) self[i] = config[i]
  }
  if (!self.user_agent) self.user_agent = 'Sinopia/'+pkg.version

  // some weird shell scripts are valid yaml files parsed as string
  assert.equal(typeof(config), 'object', 'CONFIG: it doesn\'t look like a valid config file')

  assert(self.storage, 'CONFIG: storage path not defined')
  self.localList = LocalData(
    Path.join(
      Path.resolve(Path.dirname(self.self_path), self.storage),
      '.sinopia-db.json'
    )
  )
  if (!self.secret) {
    self.secret = self.localList.data.secret

    if (!self.secret) {
      self.secret = Crypto.pseudoRandomBytes(32).toString('hex')
      self.localList.data.secret = self.secret
      self.localList.sync()
    }
  }

  var users = {all:true, anonymous:true, 'undefined':true, owner:true, none:true}

  var check_user_or_uplink = function(arg) {
    assert(arg !== 'all' && arg !== 'owner' && arg !== 'anonymous' && arg !== 'undefined' && arg !== 'none', 'CONFIG: reserved user
/uplink name: ' + arg)
    assert(!arg.match(/\s/), 'CONFIG: invalid user name: ' + arg)
    assert(users[arg] == null, 'CONFIG: duplicate user/uplink name: ' + arg)
    users[arg] = true
  }

  ;[ 'users', 'uplinks', 'packages' ].forEach(function(x) {
    if (self[x] == null) self[x] = {}
    assert(Utils.is_object(self[x]), 'CONFIG: bad "'+x+'" value (object expected)')
  })

  for (var i in self.users) check_user_or_uplink(i)
  for (var i in self.uplinks) check_user_or_uplink(i)

  for (var i in self.users) {
    assert(self.users[i].password, 'CONFIG: no password for user: ' + i)
    assert(
      typeof(self.users[i].password) === 'string' &&
      self.users[i].password.match(/^[a-f0-9]{40}$/)
    , 'CONFIG: wrong password format for user: ' + i + ', sha1 expected')
  }

  for (var i in self.uplinks) {
    assert(self.uplinks[i].url, 'CONFIG: no url for uplink: ' + i)
    assert( typeof(self.uplinks[i].url) === 'string'
          , 'CONFIG: wrong url format for uplink: ' + i)
    self.uplinks[i].url = self.uplinks[i].url.replace(/\/$/, '')
  }

  function normalize_userlist() {
    var result = []

    for (var i=0; i<arguments.length; i++) {
      if (arguments[i] == null) continue

      // if it's a string, split it to array
      if (typeof(arguments[i]) === 'string') {
        result.push(arguments[i].split(/\s+/))
      } else if (Array.isArray(arguments[i])) {
        result.push(arguments[i])
      } else {
        throw Error('CONFIG: bad package acl (array or string expected): ' + JSON.stringify(arguments[i]))
      }
    }
    return flatten(result)
  }

  // add a default rule for all packages to make writing plugins easier
  if (self.packages['**'] == null) {
    self.packages['**'] = {}
  }

  for (var i in self.packages) {
    assert(
      typeof(self.packages[i]) === 'object' &&
      !Array.isArray(self.packages[i])
    , 'CONFIG: bad "'+i+'" package description (object expected)')

    self.packages[i].access = normalize_userlist(
      self.packages[i].allow_access,
      self.packages[i].access
    );
    delete self.packages[i].allow_access

    self.packages[i].publish = normalize_userlist(
      self.packages[i].allow_publish,
      self.packages[i].publish
    );
    delete self.packages[i].allow_publish

    self.packages[i].proxy = normalize_userlist(
      self.packages[i].proxy_access,
      self.packages[i].proxy
    );
    delete self.packages[i].proxy_access
  }

  // loading these from ENV if aren't in config
  ;[ 'http_proxy', 'https_proxy', 'no_proxy' ].forEach((function(v) {
    if (!(v in self)) {
      self[v] = process.env[v] || process.env[v.toUpperCase()]
    }
  }).bind(self))

  // unique identifier of self server (or a cluster), used to avoid loops
  if (!self.server_id) {
    self.server_id = Crypto.pseudoRandomBytes(6).toString('hex')
  }

  if (self.ignore_latest_tag == null) self.ignore_latest_tag = false

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.local_data"></a>[function <span class="apidocSignatureSpan">sinopia.</span>local_data (path)](#apidoc.element.sinopia.local_data)
- description and source-code
```javascript
function LocalData(path) {
  var self = Object.create(LocalData.prototype)
  self.path = path
  try {
    self.data = JSON.parse(fs.readFileSync(self.path, 'utf8'))
  } catch(_) {
    self.data = { list: [] }
  }
  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.local_storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>local_storage (config)](#apidoc.element.sinopia.local_storage)
- description and source-code
```javascript
function Storage(config) {
  var self = Object.create(Storage.prototype)
  self.config = config
  self.logger = Logger.logger.child({ sub: 'fs' })
  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>storage (config)](#apidoc.element.sinopia.storage)
- description and source-code
```javascript
function Storage(config) {
  var self = Object.create(Storage.prototype)
  self.config = config

  // we support a number of uplinks, but only one local storage
  // Proxy and Local classes should have similar API interfaces
  self.uplinks = {}
  for (var p in config.uplinks) {
    self.uplinks[p] = Proxy(config.uplinks[p], config)
    self.uplinks[p].upname = p
  }
  self.local = Local(config)
  self.logger = Logger.logger.child()

  return self
}
```
- example usage
```shell
...
Storage.prototype._internal_error = function(err, file, message) {
this.logger.error( { err: err, file: file }
                 , message + ' @{file}: @{!err.message}' )
return Error[500]()
}

Storage.prototype.add_package = function(name, info, callback) {
var storage = this.storage(name)
if (!storage) return callback( Error[404]('this package cannot be added') )

storage.create_json(info_file, get_boilerplate(name), function(err) {
  if (err && err.code === 'EEXISTS') {
    return callback( Error[409]('this package is already present') )
  }
...
```

#### <a name="apidoc.element.sinopia.up_storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>up_storage (config, mainconfig)](#apidoc.element.sinopia.up_storage)
- description and source-code
```javascript
function Storage(config, mainconfig) {
  var self = Object.create(Storage.prototype)
  self.config = config
  self.failed_requests = 0
  self.userAgent = mainconfig.user_agent
  self.ca = config.ca
  self.logger = Logger.logger.child({sub: 'out'})
  self.server_id = mainconfig.server_id

  self.url = URL.parse(self.config.url)

  _setupProxy.call(self, self.url.hostname, config, mainconfig, self.url.protocol === 'https:')

  self.config.url = self.config.url.replace(/\/$/, '')
  if (Number(self.config.timeout) >= 1000) {
    self.logger.warn([ 'Too big timeout value: ' + self.config.timeout,
                       'We changed time format to nginx-like one',
                       '(see http://wiki.nginx.org/ConfigNotation)',
                       'so please update your config accordingly' ].join('\n'))
  }

  // a bunch of different configurable timers
  self.maxage       = parse_interval(config_get('maxage'      , '2m' ))
  self.timeout      = parse_interval(config_get('timeout'     , '30s'))
  self.max_fails    =         Number(config_get('max_fails'   ,  2   ))
  self.fail_timeout = parse_interval(config_get('fail_timeout', '5m' ))
  return self

  // just a helper ('config[key] || default' doesn't work because of zeroes)
  function config_get(key, def) {
    return config[key] != null ? config[key] : def
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.GUI"></a>[module sinopia.GUI](#apidoc.module.sinopia.GUI)

#### <a name="apidoc.element.sinopia.GUI.GUI"></a>[function <span class="apidocSignatureSpan">sinopia.</span>GUI (context, options)](#apidoc.element.sinopia.GUI.GUI)
- description and source-code
```javascript
GUI = function (context, options) {
  if (!compiled) {
    compiled = compileInput();
  }
  return compiled.call(this, context, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.GUI._child"></a>[function <span class="apidocSignatureSpan">sinopia.GUI.</span>_child (i, data, depths)](#apidoc.element.sinopia.GUI._child)
- description and source-code
```javascript
_child = function (i, data, depths) {
  if (!compiled) {
    compiled = compileInput();
  }
  return compiled._child(i, data, depths);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.GUI._setup"></a>[function <span class="apidocSignatureSpan">sinopia.GUI.</span>_setup (options)](#apidoc.element.sinopia.GUI._setup)
- description and source-code
```javascript
_setup = function (options) {
  if (!compiled) {
    compiled = compileInput();
  }
  return compiled._setup(options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.auth"></a>[module sinopia.auth](#apidoc.module.sinopia.auth)

#### <a name="apidoc.element.sinopia.auth.auth"></a>[function <span class="apidocSignatureSpan">sinopia.</span>auth (config)](#apidoc.element.sinopia.auth.auth)
- description and source-code
```javascript
function Auth(config) {
  var self = Object.create(Auth.prototype)
  self.config = config
  self.logger = Logger.logger.child({ sub: 'auth' })
  self.secret = config.secret

  var plugin_params = {
    config: config,
    logger: self.logger
  }

  if (config.users_file) {
    if (!config.auth || !config.auth.htpasswd) {
      // b/w compat
      config.auth = config.auth || {}
      config.auth.htpasswd = { file: config.users_file }
    }
  }

  self.plugins = load_plugins(config, config.auth, plugin_params, function (p) {
    return p.authenticate || p.allow_access || p.allow_publish
  })

  self.plugins.unshift({
    sinopia_version: '1.1.0',

    authenticate: function(user, password, cb) {
      if (config.users != null
       && config.users[user] != null
       && (Crypto.createHash('sha1').update(password).digest('hex')
            === config.users[user].password)
      ) {
        return cb(null, [ user ])
      }

      return cb()
    },

    adduser: function(user, password, cb) {
      if (config.users && config.users[user])
        return cb( Error[403]('this user already exists') )

      return cb()
    },
  })

  function allow_action(action) {
    return function(user, package, cb) {
      var ok = package[action].reduce(function(prev, curr) {
        if (user.groups.indexOf(curr) !== -1) return true
        return prev
      }, false)

      if (ok) return cb(null, true)

      if (user.name) {
        cb( Error[403]('user ' + user.name + ' is not allowed to ' + action + ' package ' + package.name) )
      } else {
        cb( Error[403]('unregistered users are not allowed to ' + action + ' package ' + package.name) )
      }
    }
  }

  self.plugins.push({
    authenticate: function(user, password, cb) {
      return cb( Error[403]('bad username/password, access denied') )
    },

    add_user: function(user, password, cb) {
      return cb( Error[409]('registration is disabled') )
    },

    allow_access: allow_action('access'),
    allow_publish: allow_action('publish'),
  })

  return self
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.auth.prototype"></a>[module sinopia.auth.prototype](#apidoc.module.sinopia.auth.prototype)

#### <a name="apidoc.element.sinopia.auth.prototype.add_user"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>add_user (user, password, cb)](#apidoc.element.sinopia.auth.prototype.add_user)
- description and source-code
```javascript
add_user = function (user, password, cb) {
  var self = this
  var plugins = this.plugins.slice(0)

  ;(function next() {
    var p = plugins.shift()
    var n = 'adduser'
    if (typeof(p[n]) !== 'function') {
      n = 'add_user'
    }
    if (typeof(p[n]) !== 'function') {
      next()
    } else {
      p[n](user, password, function(err, ok) {
        if (err) return cb(err)
        if (ok) return self.authenticate(user, password, cb)
        next()
      })
    }
  })()
}
```
- example usage
```shell
...
if (typeof(req.body.name) !== 'string' || typeof(req.body.password) !== 'string') {
  if (typeof(req.body.password_sha)) {
    return next( Error[422]('your npm version is outdated\nPlease update to npm@1.4.5 or greater.\nSee https://github.com/rlidwka
/sinopia/issues/93 for details.') )
  } else {
    return next( Error[422]('user/password is not found in request (npm issue?)') )
  }
}
auth.add_user(req.body.name, req.body.password, function(err, user) {
  if (err) {
    if (err.status >= 400 && err.status < 500) {
      // With npm registering is the same as logging in,
      // and npm accepts only an 409 error.
      // So, changing status code here.
      return next( Error[409](err.message) )
    }
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.aes_decrypt"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>aes_decrypt (buf)](#apidoc.element.sinopia.auth.prototype.aes_decrypt)
- description and source-code
```javascript
aes_decrypt = function (buf) {
  try {
    var c = Crypto.createDecipher('aes192', this.secret)
    var b1 = c.update(buf)
    var b2 = c.final()
  } catch(_) {
    return Buffer(0)
  }
  return Buffer.concat([ b1, b2 ])
}
```
- example usage
```shell
...
if (parts.length !== 2)
  return next( Error[400]('bad authorization header') )

var scheme = parts[0]
if (scheme === 'Basic') {
  var credentials = Buffer(parts[1], 'base64').toString()
} else if (scheme === 'Bearer') {
  var credentials = self.aes_decrypt(Buffer(parts[1], 'base64')).toString('utf8')
  if (!credentials) return next()
} else {
  return next()
}

var index = credentials.indexOf(':')
if (index < 0) return next()
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.aes_encrypt"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>aes_encrypt (buf)](#apidoc.element.sinopia.auth.prototype.aes_encrypt)
- description and source-code
```javascript
aes_encrypt = function (buf) {
  var c = Crypto.createCipher('aes192', this.secret)
  var b1 = c.update(buf)
  var b2 = c.final()
  return Buffer.concat([ b1, b2 ])
}
```
- example usage
```shell
...
  next({
    ok: 'you are authenticated as "' + req.remote_user.name + '"',
  })
})

app.put('/-/user/:org_couchdb_user/:_rev?/:revision?', function(req, res, next) {
  var token = (req.body.name && req.body.password)
            ? auth.aes_encrypt(req.body.name + ':' + req.body.password).toString('base64')
            : undefined
  if (req.remote_user.name != null) {
    res.status(201)
    return next({
      ok: "you are authenticated as '" + req.remote_user.name + "'",
      //token: auth.issue_token(req.remote_user),
      token: token,
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.allow_access"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>allow_access (package_name, user, callback)](#apidoc.element.sinopia.auth.prototype.allow_access)
- description and source-code
```javascript
allow_access = function (package_name, user, callback) {
  var plugins = this.plugins.slice(0)
  var package = Object.assign({ name: package_name },
                              this.config.get_package_spec(package_name))

  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.allow_access) !== 'function') {
      return next()
    }

    p.allow_access(user, package, function(err, ok) {
      if (err) return callback(err)
      if (ok) return callback(null, ok)
      next() // cb(null, false) causes next plugin to roll
    })
  })()
}
```
- example usage
```shell
...
  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.allow_access) !== 'function') {
      return next()
    }

    p.allow_access(user, package, function(err, ok) {
      if (err) return callback(err)
      if (ok) return callback(null, ok)
      next() // cb(null, false) causes next plugin to roll
    })
  })()
}
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.allow_publish"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>allow_publish (package_name, user, callback)](#apidoc.element.sinopia.auth.prototype.allow_publish)
- description and source-code
```javascript
allow_publish = function (package_name, user, callback) {
  var plugins = this.plugins.slice(0)
  var package = Object.assign({ name: package_name },
                              this.config.get_package_spec(package_name))

  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.allow_publish) !== 'function') {
      return next()
    }

    p.allow_publish(user, package, function(err, ok) {
      if (err) return callback(err)
      if (ok) return callback(null, ok)
      next() // cb(null, false) causes next plugin to roll
    })
  })()
}
```
- example usage
```shell
...
  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.allow_publish) !== 'function') {
      return next()
    }

    p.allow_publish(user, package, function(err, ok) {
      if (err) return callback(err)
      if (ok) return callback(null, ok)
      next() // cb(null, false) causes next plugin to roll
    })
  })()
}
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>authenticate (user, password, cb)](#apidoc.element.sinopia.auth.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (user, password, cb) {
  var plugins = this.plugins.slice(0)

  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.authenticate) !== 'function') {
      return next()
    }

    p.authenticate(user, password, function(err, groups) {
      if (err) return cb(err)
      if (groups != null && groups != false)
        return cb(err, AuthenticatedUser(user, groups))
      next()
    })
  })()
}
```
- example usage
```shell
...
  ;(function next() {
    var p = plugins.shift()

    if (typeof(p.authenticate) !== 'function') {
      return next()
    }

    p.authenticate(user, password, function(err, groups) {
      if (err) return cb(err)
      if (groups != null && groups != false)
        return cb(err, AuthenticatedUser(user, groups))
      next()
    })
  })()
}
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.basic_middleware"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>basic_middleware ()](#apidoc.element.sinopia.auth.prototype.basic_middleware)
- description and source-code
```javascript
basic_middleware = function () {
  var self = this
  return function(req, res, _next) {
    req.pause()
    function next(err) {
      req.resume()
      // uncomment this to reject users with bad auth headers
      //return _next.apply(null, arguments)

      // swallow error, user remains unauthorized
      // set remoteUserError to indicate that user was attempting authentication
      if (err) req.remote_user.error = err.message
      return _next()
    }

    if (req.remote_user != null && req.remote_user.name !== undefined)
      return next()
    req.remote_user = AnonymousUser()

    var authorization = req.headers.authorization
    if (authorization == null) return next()

    var parts = authorization.split(' ')

    if (parts.length !== 2)
      return next( Error[400]('bad authorization header') )

    var scheme = parts[0]
    if (scheme === 'Basic') {
      var credentials = Buffer(parts[1], 'base64').toString()
    } else if (scheme === 'Bearer') {
      var credentials = self.aes_decrypt(Buffer(parts[1], 'base64')).toString('utf8')
      if (!credentials) return next()
    } else {
      return next()
    }

    var index = credentials.indexOf(':')
    if (index < 0) return next()

    var user = credentials.slice(0, index)
    var pass = credentials.slice(index + 1)

    self.authenticate(user, pass, function(err, user) {
      if (!err) {
        req.remote_user = user
        next()
      } else {
        req.remote_user = AnonymousUser()
        next(err)
      }
    })
  }
}
```
- example usage
```shell
...
app.param('revision', validate_name)

// these can't be safely put into express url for some reason
app.param('_rev',             match(/^-rev$/))
app.param('org_couchdb_user', match(/^org\.couchdb\.user:/))
app.param('anything',         match(/.*/))

app.use(auth.basic_middleware())
//app.use(auth.bearer_middleware())
app.use(expressJson5({ strict: false, limit: config.max_body_size || '10mb' }))
app.use(Middleware.anti_loop(config))

// for "npm whoami"
app.get('/whoami', function(req, res, next) {
  if (req.headers.referer === 'whoami') {
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.bearer_middleware"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>bearer_middleware ()](#apidoc.element.sinopia.auth.prototype.bearer_middleware)
- description and source-code
```javascript
bearer_middleware = function () {
  var self = this
  return function(req, res, _next) {
    req.pause()
    function next(_err) {
      req.resume()
      return _next.apply(null, arguments)
    }

    if (req.remote_user != null && req.remote_user.name !== undefined)
      return next()
    req.remote_user = AnonymousUser()

    var authorization = req.headers.authorization
    if (authorization == null) return next()

    var parts = authorization.split(' ')

    if (parts.length !== 2)
      return next( Error[400]('bad authorization header') )

    var scheme = parts[0]
    var token = parts[1]

    if (scheme !== 'Bearer')
      return next()

    try {
      var user = self.decode_token(token)
    } catch(err) {
      return next(err)
    }

    req.remote_user = AuthenticatedUser(user.u, user.g)
    req.remote_user.token = token
    next()
  }
}
```
- example usage
```shell
...

// these can't be safely put into express url for some reason
app.param('_rev',             match(/^-rev$/))
app.param('org_couchdb_user', match(/^org\.couchdb\.user:/))
app.param('anything',         match(/.*/))

app.use(auth.basic_middleware())
//app.use(auth.bearer_middleware())
app.use(expressJson5({ strict: false, limit: config.max_body_size || '10mb' }))
app.use(Middleware.anti_loop(config))

// for "npm whoami"
app.get('/whoami', function(req, res, next) {
  if (req.headers.referer === 'whoami') {
    next({ username: req.remote_user.name })
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.cookie_middleware"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>cookie_middleware ()](#apidoc.element.sinopia.auth.prototype.cookie_middleware)
- description and source-code
```javascript
cookie_middleware = function () {
  var self = this
  return function(req, res, _next) {
    req.pause()
    function next(_err) {
      req.resume()
      return _next()
    }

    if (req.remote_user != null && req.remote_user.name !== undefined)
      return next()

    req.remote_user = AnonymousUser()

    var token = req.cookies.get('token')
    if (token == null) return next()

<span class="apidocCodeCommentSpan">    /*try {
      var user = self.decode_token(token, 60*60)
    } catch(err) {
      return next()
    }

    req.remote_user = AuthenticatedUser(user.u, user.g)
    req.remote_user.token = token
    next()*/
</span>    var credentials = self.aes_decrypt(Buffer(token, 'base64')).toString('utf8')
    if (!credentials) return next()

    var index = credentials.indexOf(':')
    if (index < 0) return next()

    var user = credentials.slice(0, index)
    var pass = credentials.slice(index + 1)

    self.authenticate(user, pass, function(err, user) {
      if (!err) {
        req.remote_user = user
        next()
      } else {
        req.remote_user = AnonymousUser()
        next(err)
      }
    })
  }
}
```
- example usage
```shell
...
app.param('package',  validate_pkg)
app.param('filename', validate_name)
app.param('version',  validate_name)
app.param('anything', match(/.*/))

app.use(Cookies.express())
app.use(bodyParser.urlencoded({ extended: false }))
app.use(auth.cookie_middleware())
app.use(function(req, res, next) {
  // disable loading in frames (clickjacking, etc.)
  res.header('X-Frame-Options', 'deny')
  next()
})

Search.configureStorage(storage)
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.decode_token"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>decode_token (str, expire_time)](#apidoc.element.sinopia.auth.prototype.decode_token)
- description and source-code
```javascript
decode_token = function (str, expire_time) {
  var buf = Buffer(str, 'base64')
  if (buf.length <= 32) throw Error[401]('invalid token')

  var data      = buf.slice(0, buf.length - 32)
  var their_mac = buf.slice(buf.length - 32)
  var good_mac  = Crypto.createHmac('sha256', this.secret).update(data).digest()

  their_mac = Crypto.createHash('sha512').update(their_mac).digest('hex')
  good_mac  = Crypto.createHash('sha512').update(good_mac).digest('hex')
  if (their_mac !== good_mac) throw Error[401]('bad signature')

  // make token expire in 24 hours
  // TODO: make configurable?
  expire_time = expire_time || 24*60*60

  data = jju.parse(data.toString('utf8'))
  if (Math.abs(data.t - ~~(Date.now()/1000)) > expire_time)
    throw Error[401]('token expired')

  return data
}
```
- example usage
```shell
...
var scheme = parts[0]
var token = parts[1]

if (scheme !== 'Bearer')
  return next()

try {
  var user = self.decode_token(token)
} catch(err) {
  return next(err)
}

req.remote_user = AuthenticatedUser(user.u, user.g)
req.remote_user.token = token
next()
...
```

#### <a name="apidoc.element.sinopia.auth.prototype.issue_token"></a>[function <span class="apidocSignatureSpan">sinopia.auth.prototype.</span>issue_token (user)](#apidoc.element.sinopia.auth.prototype.issue_token)
- description and source-code
```javascript
issue_token = function (user) {
  var data = jju.stringify({
    u: user.name,
    g: user.real_groups && user.real_groups.length ? user.real_groups : undefined,
    t: ~~(Date.now()/1000),
  }, { indent: false })

  data = Buffer(data, 'utf8')
  var mac = Crypto.createHmac('sha256', this.secret).update(data).digest()
  return Buffer.concat([ data, mac ]).toString('base64')
}
```
- example usage
```shell
...
var token = (req.body.name && req.body.password)
          ? auth.aes_encrypt(req.body.name + ':' + req.body.password).toString('base64')
          : undefined
if (req.remote_user.name != null) {
  res.status(201)
  return next({
    ok: "you are authenticated as '" + req.remote_user.name + "'",
    //token: auth.issue_token(req.remote_user),
    token: token,
  })
} else {
  if (typeof(req.body.name) !== 'string' || typeof(req.body.password) !== 'string') {
    if (typeof(req.body.password_sha)) {
      return next( Error[422]('your npm version is outdated\nPlease update to npm@1.4.5 or greater.\nSee https://github.com/rlidwka
/sinopia/issues/93 for details.') )
    } else {
...
```



# <a name="apidoc.module.sinopia.config"></a>[module sinopia.config](#apidoc.module.sinopia.config)

#### <a name="apidoc.element.sinopia.config.config"></a>[function <span class="apidocSignatureSpan">sinopia.</span>config (config)](#apidoc.element.sinopia.config.config)
- description and source-code
```javascript
function Config(config) {
  var self = Object.create(Config.prototype)
  for (var i in config) {
    if (self[i] == null) self[i] = config[i]
  }
  if (!self.user_agent) self.user_agent = 'Sinopia/'+pkg.version

  // some weird shell scripts are valid yaml files parsed as string
  assert.equal(typeof(config), 'object', 'CONFIG: it doesn\'t look like a valid config file')

  assert(self.storage, 'CONFIG: storage path not defined')
  self.localList = LocalData(
    Path.join(
      Path.resolve(Path.dirname(self.self_path), self.storage),
      '.sinopia-db.json'
    )
  )
  if (!self.secret) {
    self.secret = self.localList.data.secret

    if (!self.secret) {
      self.secret = Crypto.pseudoRandomBytes(32).toString('hex')
      self.localList.data.secret = self.secret
      self.localList.sync()
    }
  }

  var users = {all:true, anonymous:true, 'undefined':true, owner:true, none:true}

  var check_user_or_uplink = function(arg) {
    assert(arg !== 'all' && arg !== 'owner' && arg !== 'anonymous' && arg !== 'undefined' && arg !== 'none', 'CONFIG: reserved user
/uplink name: ' + arg)
    assert(!arg.match(/\s/), 'CONFIG: invalid user name: ' + arg)
    assert(users[arg] == null, 'CONFIG: duplicate user/uplink name: ' + arg)
    users[arg] = true
  }

  ;[ 'users', 'uplinks', 'packages' ].forEach(function(x) {
    if (self[x] == null) self[x] = {}
    assert(Utils.is_object(self[x]), 'CONFIG: bad "'+x+'" value (object expected)')
  })

  for (var i in self.users) check_user_or_uplink(i)
  for (var i in self.uplinks) check_user_or_uplink(i)

  for (var i in self.users) {
    assert(self.users[i].password, 'CONFIG: no password for user: ' + i)
    assert(
      typeof(self.users[i].password) === 'string' &&
      self.users[i].password.match(/^[a-f0-9]{40}$/)
    , 'CONFIG: wrong password format for user: ' + i + ', sha1 expected')
  }

  for (var i in self.uplinks) {
    assert(self.uplinks[i].url, 'CONFIG: no url for uplink: ' + i)
    assert( typeof(self.uplinks[i].url) === 'string'
          , 'CONFIG: wrong url format for uplink: ' + i)
    self.uplinks[i].url = self.uplinks[i].url.replace(/\/$/, '')
  }

  function normalize_userlist() {
    var result = []

    for (var i=0; i<arguments.length; i++) {
      if (arguments[i] == null) continue

      // if it's a string, split it to array
      if (typeof(arguments[i]) === 'string') {
        result.push(arguments[i].split(/\s+/))
      } else if (Array.isArray(arguments[i])) {
        result.push(arguments[i])
      } else {
        throw Error('CONFIG: bad package acl (array or string expected): ' + JSON.stringify(arguments[i]))
      }
    }
    return flatten(result)
  }

  // add a default rule for all packages to make writing plugins easier
  if (self.packages['**'] == null) {
    self.packages['**'] = {}
  }

  for (var i in self.packages) {
    assert(
      typeof(self.packages[i]) === 'object' &&
      !Array.isArray(self.packages[i])
    , 'CONFIG: bad "'+i+'" package description (object expected)')

    self.packages[i].access = normalize_userlist(
      self.packages[i].allow_access,
      self.packages[i].access
    );
    delete self.packages[i].allow_access

    self.packages[i].publish = normalize_userlist(
      self.packages[i].allow_publish,
      self.packages[i].publish
    );
    delete self.packages[i].allow_publish

    self.packages[i].proxy = normalize_userlist(
      self.packages[i].proxy_access,
      self.packages[i].proxy
    );
    delete self.packages[i].proxy_access
  }

  // loading these from ENV if aren't in config
  ;[ 'http_proxy', 'https_proxy', 'no_proxy' ].forEach((function(v) {
    if (!(v in self)) {
      self[v] = process.env[v] || process.env[v.toUpperCase()]
    }
  }).bind(self))

  // unique identifier of self server (or a cluster), used to avoid loops
  if (!self.server_id) {
    self.server_id = Crypto.pseudoRandomBytes(6).toString('hex')
  }

  if (self.ignore_latest_tag == null) self.ignore_latest_tag = false

  return self
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.config.parse_interval"></a>[function <span class="apidocSignatureSpan">sinopia.config.</span>parse_interval (interval)](#apidoc.element.sinopia.config.parse_interval)
- description and source-code
```javascript
parse_interval = function (interval) {
  if (typeof(interval) === 'number') return interval * 1000

  var result = 0
  var last_suffix = Infinity
  interval.split(/\s+/).forEach(function(x) {
    if (!x) return
    var m = x.match(/^((0|[1-9][0-9]*)(\.[0-9]+)?)(ms|s|m|h|d|w|M|y|)$/)
    if (!m
    ||  parse_interval_table[m[4]] >= last_suffix
    ||  (m[4] === '' && last_suffix !== Infinity)) {
      throw Error('invalid interval: ' + interval)
    }
    last_suffix = parse_interval_table[m[4]]
    result += Number(m[1]) * parse_interval_table[m[4]]
  })
  return result
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.config.prototype"></a>[module sinopia.config.prototype](#apidoc.module.sinopia.config.prototype)

#### <a name="apidoc.element.sinopia.config.prototype.can_proxy_to"></a>[function <span class="apidocSignatureSpan">sinopia.config.prototype.</span>can_proxy_to (package, uplink)](#apidoc.element.sinopia.config.prototype.can_proxy_to)
- description and source-code
```javascript
can_proxy_to = function (package, uplink) {
  return (this.get_package_spec(package).proxy || []).reduce(function(prev, curr) {
    if (uplink === curr) return true
    return prev
  }, false)
}
```
- example usage
```shell
...
  }
} else {
  var exists = true
}

var uplinks = []
for (var i in self.uplinks) {
  if (self.config.can_proxy_to(name, i)) {
    uplinks.push(self.uplinks[i])
  }
}

async.map(uplinks, function(up, cb) {
  var _options = Object.assign({}, options)
  if (Utils.is_object(pkginfo._uplinks[up.upname])) {
...
```

#### <a name="apidoc.element.sinopia.config.prototype.get_package_spec"></a>[function <span class="apidocSignatureSpan">sinopia.config.prototype.</span>get_package_spec (package)](#apidoc.element.sinopia.config.prototype.get_package_spec)
- description and source-code
```javascript
get_package_spec = function (package) {
  for (var i in this.packages) {
    if (minimatch.makeRe(i).exec(package)) {
      return this.packages[i]
    }
  }
  return {}
}
```
- example usage
```shell
...
}
  })()
}

Auth.prototype.allow_access = function(package_name, user, callback) {
  var plugins = this.plugins.slice(0)
  var package = Object.assign({ name: package_name },
                          this.config.get_package_spec(package_name))

  ;(function next() {
var p = plugins.shift()

if (typeof(p.allow_access) !== 'function') {
  return next()
}
...
```



# <a name="apidoc.module.sinopia.local_data"></a>[module sinopia.local_data](#apidoc.module.sinopia.local_data)

#### <a name="apidoc.element.sinopia.local_data.local_data"></a>[function <span class="apidocSignatureSpan">sinopia.</span>local_data (path)](#apidoc.element.sinopia.local_data.local_data)
- description and source-code
```javascript
function LocalData(path) {
  var self = Object.create(LocalData.prototype)
  self.path = path
  try {
    self.data = JSON.parse(fs.readFileSync(self.path, 'utf8'))
  } catch(_) {
    self.data = { list: [] }
  }
  return self
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.local_data.prototype"></a>[module sinopia.local_data.prototype](#apidoc.module.sinopia.local_data.prototype)

#### <a name="apidoc.element.sinopia.local_data.prototype.add"></a>[function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>add (name)](#apidoc.element.sinopia.local_data.prototype.add)
- description and source-code
```javascript
add = function (name) {
  if (this.data.list.indexOf(name) === -1) {
    this.data.list.push(name)
    this.sync()
  }
}
```
- example usage
```shell
...
storage.create_json(info_file, get_boilerplate(name), function(err) {
  if (err && err.code === 'EEXISTS') {
    return callback( Error[409]('this package is already present') )
  }

  var latest = info['dist-tags'].latest
  if (latest && info.versions[latest]) {
    Search.add(info.versions[latest])
  }
  callback()
})
}

Storage.prototype.remove_package = function(name, callback) {
var self = this
...
```

#### <a name="apidoc.element.sinopia.local_data.prototype.get"></a>[function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>get ()](#apidoc.element.sinopia.local_data.prototype.get)
- description and source-code
```javascript
get = function () {
  return this.data.list
}
```
- example usage
```shell
...
}

if (req.remote_user != null && req.remote_user.name !== undefined)
  return next()

req.remote_user = AnonymousUser()

var token = req.cookies.get('token')
if (token == null) return next()

/*try {
  var user = self.decode_token(token, 60*60)
} catch(err) {
  return next()
}
...
```

#### <a name="apidoc.element.sinopia.local_data.prototype.remove"></a>[function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>remove (name)](#apidoc.element.sinopia.local_data.prototype.remove)
- description and source-code
```javascript
remove = function (name) {
  var i = this.data.list.indexOf(name)
  if (i !== -1) {
    this.data.list.splice(i, 1)
  }

  this.sync()
}
```
- example usage
```shell
...
      storage.rmdir('.', function(err) {
        callback(err)
      })
    })
  })
})

Search.remove(name)
this.config.localList.remove(name)
}

Storage.prototype._read_create_package = function(name, callback) {
var self = this
var storage = self.storage(name)
if (!storage) {
...
```

#### <a name="apidoc.element.sinopia.local_data.prototype.sync"></a>[function <span class="apidocSignatureSpan">sinopia.local_data.prototype.</span>sync ()](#apidoc.element.sinopia.local_data.prototype.sync)
- description and source-code
```javascript
sync = function () {
  // Uses sync to prevent ugly race condition
  try {
    require('mkdirp').sync(Path.dirname(this.path))
  } catch(err) {}
  fs.writeFileSync(this.path, JSON.stringify(this.data))
}
```
- example usage
```shell
...
}

create_config_file(paths[0])
return paths[0].path
}

function create_config_file(config_path) {
require('mkdirp').sync(Path.dirname(config_path.path))
logger.logger.info({ file: config_path.path }, 'Creating default config file in @{file}')

var created_config = fs.readFileSync(require.resolve('../conf/default.yaml'), 'utf8')

if (config_path.type === 'xdg') {
  var data_dir = process.env.XDG_DATA_HOME
              || Path.join(process.env.HOME, '.local', 'share')
...
```



# <a name="apidoc.module.sinopia.local_fs"></a>[module sinopia.local_fs](#apidoc.module.sinopia.local_fs)

#### <a name="apidoc.element.sinopia.local_fs.create"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>create (name, contents, callback)](#apidoc.element.sinopia.local_fs.create)
- description and source-code
```javascript
function create(name, contents, callback) {
  fs.exists(name, function(exists) {
    if (exists) return callback( FSError('EEXISTS') )
    write(name, contents, callback)
  })
}
```
- example usage
```shell
...
var Error        = require('http-errors')
var Logger       = require('./logger')
var load_plugins = require('./plugin-loader').load_plugins

module.exports = Auth

function Auth(config) {
var self = Object.create(Auth.prototype)
self.config = config
self.logger = Logger.logger.child({ sub: 'auth' })
self.secret = config.secret

var plugin_params = {
  config: config,
  logger: self.logger
...
```

#### <a name="apidoc.element.sinopia.local_fs.create_json"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>create_json (name, value, cb)](#apidoc.element.sinopia.local_fs.create_json)
- description and source-code
```javascript
create_json = function (name, value, cb) {
  create(name, JSON.stringify(value, null, '\t'), cb)
}
```
- example usage
```shell
...
  return Error[500]()
}

Storage.prototype.add_package = function(name, info, callback) {
  var storage = this.storage(name)
  if (!storage) return callback( Error[404]('this package cannot be added') )

  storage.create_json(info_file, get_boilerplate(name), function(err) {
if (err && err.code === 'EEXISTS') {
  return callback( Error[409]('this package is already present') )
}

var latest = info['dist-tags'].latest
if (latest && info.versions[latest]) {
  Search.add(info.versions[latest])
...
```

#### <a name="apidoc.element.sinopia.local_fs.lock_and_read"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>lock_and_read (name, _callback)](#apidoc.element.sinopia.local_fs.lock_and_read)
- description and source-code
```javascript
function lock_and_read(name, _callback) {
  open_flock(name, 'r', 'exnb', 4, 10, function(err, fd) {
    function callback(err) {
      if (err && fd) {
        fs.close(fd, function(err2) {
          _callback(err)
        })
      } else {
        _callback.apply(null, arguments)
      }
    }

    if (err) return callback(err, fd)

    fs.fstat(fd, function(err, st) {
      if (err) return callback(err, fd)

      var buffer = Buffer(st.size)
      if (st.size === 0) return onRead(null, 0, buffer)
      fs.read(fd, buffer, 0, st.size, null, onRead)

      function onRead(err, bytesRead, buffer) {
        if (err) return callback(err, fd)
        if (bytesRead != st.size) return callback(Error('st.size != bytesRead'), fd)

        callback(null, fd, buffer)
      }
    })
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.local_fs.lock_and_read_json"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>lock_and_read_json (name, cb)](#apidoc.element.sinopia.local_fs.lock_and_read_json)
- description and source-code
```javascript
lock_and_read_json = function (name, cb) {
  lock_and_read(name, function(err, fd, res) {
    if (err) return cb(err, fd)

    var args = []
    try {
      args = [ null, fd, JSON.parse(res.toString('utf8')) ]
    } catch(err) {
      args = [ err, fd ]
    }
    cb.apply(null, args)
  })
}
```
- example usage
```shell
...
// 5. move package.json.tmp package.json
// 6. callback(err?)
//
Storage.prototype.update_package = function(name, updateFn, _callback) {
var self = this
var storage = self.storage(name)
if (!storage) return _callback( Error[404]('no such package available') )
storage.lock_and_read_json(info_file, function(err, fd, json) {
  function callback() {
    var _args = arguments
    if (fd) {
      fs.close(fd, function(err) {
        if (err) return _callback(err)
        _callback.apply(null, _args)
      })
...
```

#### <a name="apidoc.element.sinopia.local_fs.read"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read (name, callback)](#apidoc.element.sinopia.local_fs.read)
- description and source-code
```javascript
function read(name, callback) {
  fs.readFile(name, callback)
}
```
- example usage
```shell
...
    if (err) return callback(err, fd)

    fs.fstat(fd, function(err, st) {
if (err) return callback(err, fd)

var buffer = Buffer(st.size)
if (st.size === 0) return onRead(null, 0, buffer)
fs.read(fd, buffer, 0, st.size, null, onRead)

function onRead(err, bytesRead, buffer) {
  if (err) return callback(err, fd)
  if (bytesRead != st.size) return callback(Error('st.size != bytesRead'), fd)

  callback(null, fd, buffer)
}
...
```

#### <a name="apidoc.element.sinopia.local_fs.read_json"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read_json (name, cb)](#apidoc.element.sinopia.local_fs.read_json)
- description and source-code
```javascript
read_json = function (name, cb) {
  read(name, function(err, res) {
    if (err) return cb(err)

    var args = []
    try {
      args = [ null, JSON.parse(res.toString('utf8')) ]
    } catch(err) {
      args = [ err ]
    }
    cb.apply(null, args)
  })
}
```
- example usage
```shell
...
var self = this
self.logger.info( { name: name }
                , 'unpublishing @{name} (all)')

var storage = self.storage(name)
if (!storage) return callback( Error[404]('no such package available') )

storage.read_json(info_file, function(err, data) {
  if (err) {
    if (err.code === 'ENOENT') {
      return callback( Error[404]('no such package available') )
    } else {
      return callback(err)
    }
  }
...
```

#### <a name="apidoc.element.sinopia.local_fs.read_stream"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>read_stream (name, stream, callback)](#apidoc.element.sinopia.local_fs.read_stream)
- description and source-code
```javascript
function read_stream(name, stream, callback) {
  var rstream = fs.createReadStream(name)
  rstream.on('error', function(err) {
    stream.emit('error', err)
  })
  rstream.on('open', function(fd) {
    fs.fstat(fd, function(err, stats) {
      if (err) return stream.emit('error', err)
      stream.emit('content-length', stats.size)
      stream.emit('open')
      rstream.pipe(stream)
    })
  })

  var stream = MyStreams.ReadTarballStream()
  stream.abort = function() {
    rstream.close()
  }
  return stream
}
```
- example usage
```shell
...
if (!storage) {
  process.nextTick(function() {
    stream.emit('error', Error[404]('no such file available'))
  })
  return stream
}

var rstream = storage.read_stream(filename)
rstream.on('error', function(err) {
  if (err && err.code === 'ENOENT') {
    stream.emit('error', Error(404, 'no such file available'))
  } else {
    stream.emit('error', err)
  }
})
...
```

#### <a name="apidoc.element.sinopia.local_fs.rmdir"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>rmdir (path, callback)](#apidoc.element.sinopia.local_fs.rmdir)
- description and source-code
```javascript
rmdir = function (path, callback) {
  callback = maybeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.rmdir(pathModule._makeLong(path), req);
}
```
- example usage
```shell
...
      storage.unlink(file, function() {
        unlinkNext(cb)
      })
    }

    unlinkNext(function() {
      // try to unlink the directory, but ignore errors because it can fail
      storage.rmdir('.', function(err) {
        callback(err)
      })
    })
  })
})

Search.remove(name)
...
```

#### <a name="apidoc.element.sinopia.local_fs.unlink"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>unlink (path, callback)](#apidoc.element.sinopia.local_fs.unlink)
- description and source-code
```javascript
unlink = function (path, callback) {
  callback = makeCallback(callback);
  if (!nullCheck(path, callback)) return;
  var req = new FSReqWrap();
  req.oncomplete = callback;
  binding.unlink(pathModule._makeLong(path), req);
}
```
- example usage
```shell
...

function tempFile(str) {
return str + '.tmp' + String(Math.random()).substr(2)
}

function renameTmp(src, dst, _cb) {
function cb(err) {
  if (err) fs.unlink(src)
  _cb(err)
}

if (process.platform !== 'win32') {
  return fs.rename(src, dst, cb)
}
...
```

#### <a name="apidoc.element.sinopia.local_fs.update"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>update (name, contents, callback)](#apidoc.element.sinopia.local_fs.update)
- description and source-code
```javascript
function update(name, contents, callback) {
  fs.exists(name, function(exists) {
    if (!exists) return callback( FSError('ENOENT') )
    write(name, contents, callback)
  })
}
```
- example usage
```shell
...

  self.plugins.unshift({
sinopia_version: '1.1.0',

authenticate: function(user, password, cb) {
  if (config.users != null
   && config.users[user] != null
   && (Crypto.createHash('sha1').update(password).digest('hex')
        === config.users[user].password)
  ) {
    return cb(null, [ user ])
  }

  return cb()
},
...
```

#### <a name="apidoc.element.sinopia.local_fs.update_json"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>update_json (name, value, cb)](#apidoc.element.sinopia.local_fs.update_json)
- description and source-code
```javascript
update_json = function (name, value, cb) {
  update(name, JSON.stringify(value, null, '\t'), cb)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.local_fs.write"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write (dest, data, cb)](#apidoc.element.sinopia.local_fs.write)
- description and source-code
```javascript
function write(dest, data, cb) {
  var safe_write = function(cb) {
    var tmpname = tempFile(dest)
    fs.writeFile(tmpname, data, function(err) {
      if (err) return cb(err)
      renameTmp(tmpname, dest, cb)
    })
  }

  safe_write(function(err) {
    if (err && err.code === 'ENOENT') {
      mkdirp(Path.dirname(dest), function(err) {
        if (err) return cb(err)
        safe_write(cb)
      })
    } else {
      cb(err)
    }
  })
}
```
- example usage
```shell
...
  // searching packages
  app.get('/-/all/:anything?', function(req, res, next) {
    var received_end      = false
    var response_finished = false
    var processing_pkgs   = 0

    res.status(200)
    res.write('{"_updated":' + Date.now());

    var stream = storage.search(req.param.startkey || 0, { req: req })

    stream.on('data', function each(pkg) {
processing_pkgs++

auth.allow_access(pkg.name, req.remote_user, function(err, allowed) {
...
```

#### <a name="apidoc.element.sinopia.local_fs.write_json"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write_json (name, value, cb)](#apidoc.element.sinopia.local_fs.write_json)
- description and source-code
```javascript
write_json = function (name, value, cb) {
  write(name, JSON.stringify(value, null, '\t'), cb)
}
```
- example usage
```shell
...
// calculate revision a la couchdb
if (typeof(json._rev) !== 'string') json._rev = '0-0000000000000000'
var rev = json._rev.split('-')
json._rev = ((+rev[0] || 0) + 1) + '-' + Crypto.pseudoRandomBytes(8).toString('hex')

var storage = this.storage(name)
if (!storage) return callback()
storage.write_json(info_file, json, callback)
}

Storage.prototype.storage = function(package) {
var path = this.config.get_package_spec(package).storage
if (path == null) path = this.config.storage
if (path == null || path === false) {
  this.logger.debug( { name: package }
...
```

#### <a name="apidoc.element.sinopia.local_fs.write_stream"></a>[function <span class="apidocSignatureSpan">sinopia.local_fs.</span>write_stream (name)](#apidoc.element.sinopia.local_fs.write_stream)
- description and source-code
```javascript
function write_stream(name) {
  var stream = MyStreams.UploadTarballStream()

  var _ended = 0
  stream.on('end', function() {
    _ended = 1
  })

  fs.exists(name, function(exists) {
    if (exists) return stream.emit('error', FSError('EEXISTS'))

    var tmpname = name + '.tmp-'+String(Math.random()).replace(/^0\./, '')
    var file = fs.createWriteStream(tmpname)
    var opened = false
    stream.pipe(file)

    stream.done = function() {
      function onend() {
        file.on('close', function() {
          renameTmp(tmpname, name, function(err) {
            if (err) {
              stream.emit('error', err)
            } else {
              stream.emit('success')
            }
          })
        })
        file.destroySoon()
      }
      if (_ended) {
        onend()
      } else {
        stream.on('end', onend)
      }
    }
    stream.abort = function() {
      if (opened) {
        opened = false
        file.on('close', function() {
          fs.unlink(tmpname, function(){})
        })
      }
      file.destroySoon()
    }
    file.on('open', function() {
      opened = true
      // re-emitting open because it's handled in storage.js
      stream.emit('open')
    })
    file.on('error', function(err) {
      stream.emit('error', err)
    })
  })
  return stream
}
```
- example usage
```shell
...
if (!storage) {
  process.nextTick(function() {
    stream.emit('error', Error[404]("can't upload this package"))
  })
  return stream
}

var wstream = storage.write_stream(filename)

wstream.on('error', function(err) {
  if (err.code === 'EEXISTS') {
    stream.emit('error', Error[409]('this tarball is already present'))
  } else if (err.code === 'ENOENT') {
    // check if package exists to throw an appropriate message
    self.get_package(name, function(_err, res) {
...
```



# <a name="apidoc.module.sinopia.local_storage"></a>[module sinopia.local_storage](#apidoc.module.sinopia.local_storage)

#### <a name="apidoc.element.sinopia.local_storage.local_storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>local_storage (config)](#apidoc.element.sinopia.local_storage.local_storage)
- description and source-code
```javascript
function Storage(config) {
  var self = Object.create(Storage.prototype)
  self.config = config
  self.logger = Logger.logger.child({ sub: 'fs' })
  return self
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.local_storage.prototype"></a>[module sinopia.local_storage.prototype](#apidoc.module.sinopia.local_storage.prototype)

#### <a name="apidoc.element.sinopia.local_storage.prototype._each_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_each_package (on_package, on_end)](#apidoc.element.sinopia.local_storage.prototype._each_package)
- description and source-code
```javascript
_each_package = function (on_package, on_end) {
  var self = this
  var storages = {}

  storages[self.config.storage] = true

  if (self.config.packages) {
    Object.keys(self.packages || {}).map(function (pkg) {
      if (self.config.packages[pkg].storage) {
        storages[self.config.packages[pkg].storage] = true
      }
    })
  }

  var base = Path.dirname(self.config.self_path);

  async.eachSeries(Object.keys(storages), function (storage, cb) {
    fs.readdir(Path.resolve(base, storage), function (err, files) {
      if (err) return cb(err)

      async.eachSeries(files, function (file, cb) {
        if (file.match(/^@/)) {
          // scoped
          fs.readdir(Path.resolve(base, storage, file), function (err, files) {
            if (err) return cb(err)

            async.eachSeries(files, function (file2, cb) {
              if (Utils.validate_name(file2)) {
                on_package({
                  name: file + '/' + file2,
                  path: Path.resolve(base, storage, file, file2),
                }, cb)
              } else {
                cb()
              }
            }, cb)
          })
        } else if (Utils.validate_name(file)) {
          on_package({
            name: file,
            path: Path.resolve(base, storage, file)
          }, cb)
        } else {
          cb()
        }
      }, cb)
    })
  }, on_end)
}
```
- example usage
```shell
...
}

Storage.prototype.search = function(startkey, options) {
  var self = this

  var stream = new Stream.PassThrough({ objectMode: true })

  self._each_package(function on_package(item, cb) {
    fs.stat(item.path, function(err, stats) {
if (err) return cb(err)

if (stats.mtime > startkey) {
  self.get_package(item.name, options, function(err, data) {
    if (err) return cb(err)
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype._internal_error"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_internal_error (err, file, message)](#apidoc.element.sinopia.local_storage.prototype._internal_error)
- description and source-code
```javascript
_internal_error = function (err, file, message) {
  this.logger.error( { err: err, file: file }
                   , message + ' @{file}: @{!err.message}' )
  return Error[500]()
}
```
- example usage
```shell
...
  storage.read_json(info_file, function(err, data) {
    // TODO: race condition
    if (err) {
      if (err.code === 'ENOENT') {
        // if package doesn't exist, we create it here
        data = get_boilerplate(name)
      } else {
        return callback(self._internal_error(err, info_file, 'error reading'))
      }
    }
    self._normalize_package(data)
    callback(null, data)
  })
}
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype._normalize_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_normalize_package (pkg)](#apidoc.element.sinopia.local_storage.prototype._normalize_package)
- description and source-code
```javascript
_normalize_package = function (pkg) {
  ;['versions', 'dist-tags', '_distfiles', '_attachments', '_uplinks'].forEach(function(key) {
    if (!Utils.is_object(pkg[key])) pkg[key] = {}
  })
  if (typeof(pkg._rev) !== 'string') pkg._rev = '0-0000000000000000'
}
```
- example usage
```shell
...
    if (err) {
if (err.code === 'ENOENT') {
  return callback( Error[404]('no such package available') )
} else {
  return callback(err)
}
    }
    self._normalize_package(data)

    storage.unlink(info_file, function(err) {
if (err) return callback(err)

var files = Object.keys(data._attachments)

function unlinkNext(cb) {
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype._read_create_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_read_create_package (name, callback)](#apidoc.element.sinopia.local_storage.prototype._read_create_package)
- description and source-code
```javascript
_read_create_package = function (name, callback) {
  var self = this
  var storage = self.storage(name)
  if (!storage) {
    var data = get_boilerplate(name)
    self._normalize_package(data)
    return callback(null, data)
  }
  storage.read_json(info_file, function(err, data) {
    // TODO: race condition
    if (err) {
      if (err.code === 'ENOENT') {
        // if package doesn't exist, we create it here
        data = get_boilerplate(name)
      } else {
        return callback(self._internal_error(err, info_file, 'error reading'))
      }
    }
    self._normalize_package(data)
    callback(null, data)
  })
}
```
- example usage
```shell
...
  })
}

// synchronize remote package info with the local one
// TODO: readfile called twice
Storage.prototype.update_versions = function(name, newdata, callback) {
  var self = this
  self._read_create_package(name, function(err, data) {
if (err) return callback(err)

var change = false
for (var ver in newdata.versions) {
  if (data.versions[ver] == null) {
    var verdata = newdata.versions[ver]
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype._write_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>_write_package (name, json, callback)](#apidoc.element.sinopia.local_storage.prototype._write_package)
- description and source-code
```javascript
_write_package = function (name, json, callback) {

  // calculate revision a la couchdb
  if (typeof(json._rev) !== 'string') json._rev = '0-0000000000000000'
  var rev = json._rev.split('-')
  json._rev = ((+rev[0] || 0) + 1) + '-' + Crypto.pseudoRandomBytes(8).toString('hex')

  var storage = this.storage(name)
  if (!storage) return callback()
  storage.write_json(info_file, json, callback)
}
```
- example usage
```shell
...
    if (newdata.readme !== data.readme) {
      data.readme = newdata.readme
      change = true
    }

    if (change) {
      self.logger.debug('updating package info')
      self._write_package(name, data, function(err) {
        callback(err, data)
      })
    } else {
      callback(null, data)
    }
  })
}
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.add_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_package (name, info, callback)](#apidoc.element.sinopia.local_storage.prototype.add_package)
- description and source-code
```javascript
add_package = function (name, info, callback) {
  var storage = this.storage(name)
  if (!storage) return callback( Error[404]('this package cannot be added') )

  storage.create_json(info_file, get_boilerplate(name), function(err) {
    if (err && err.code === 'EEXISTS') {
      return callback( Error[409]('this package is already present') )
    }

    var latest = info['dist-tags'].latest
    if (latest && info.versions[latest]) {
      Search.add(info.versions[latest])
    }
    callback()
  })
}
```
- example usage
```shell
...
}

if (req.params._rev) {
  storage.change_package(name, metadata, req.params.revision, function(err) {
    after_change(err, 'package changed')
  })
} else {
  storage.add_package(name, metadata, function(err) {
    after_change(err, 'created new package')
  })
}

function after_change(err, ok_message) {
  // old npm behaviour
  if (metadata._attachments == null) {
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.add_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_tarball (name, filename)](#apidoc.element.sinopia.local_storage.prototype.add_tarball)
- description and source-code
```javascript
add_tarball = function (name, filename) {
  assert(Utils.validate_name(filename))

  var stream = MyStreams.UploadTarballStream()
  var _transform = stream._transform
  var length = 0
  var shasum = Crypto.createHash('sha1')

  stream.abort = stream.done = function(){}

  stream._transform = function(data) {
    shasum.update(data)
    length += data.length
    _transform.apply(stream, arguments)
  }

  var self = this
  if (name === info_file || name === '__proto__') {
    process.nextTick(function() {
      stream.emit('error', Error[403]("can't use this filename"))
    })
    return stream
  }

  var storage = self.storage(name)
  if (!storage) {
    process.nextTick(function() {
      stream.emit('error', Error[404]("can't upload this package"))
    })
    return stream
  }

  var wstream = storage.write_stream(filename)

  wstream.on('error', function(err) {
    if (err.code === 'EEXISTS') {
      stream.emit('error', Error[409]('this tarball is already present'))
    } else if (err.code === 'ENOENT') {
      // check if package exists to throw an appropriate message
      self.get_package(name, function(_err, res) {
        if (_err) {
          stream.emit('error', _err)
        } else {
          stream.emit('error', err)
        }
      })
    } else {
      stream.emit('error', err)
    }
  })

  wstream.on('open', function() {
    // re-emitting open because it's handled in storage.js
    stream.emit('open')
  })
  wstream.on('success', function() {
    self.update_package(name, function updater(data, cb) {
      data._attachments[filename] = {
        shasum: shasum.digest('hex'),
      }
      cb()
    }, function(err) {
      if (err) {
        stream.emit('error', err)
      } else {
        stream.emit('success')
      }
    })
  })
  stream.abort = function() {
    wstream.abort()
  }
  stream.done = function() {
    if (!length) {
      stream.emit('error', Error[422]('refusing to accept zero-length file'))
      wstream.abort()
    } else {
      wstream.done()
    }
  }
  stream.pipe(wstream)

  return stream
}
```
- example usage
```shell
...
        return next({ ok: ok_message })
      })
    })
  })
}

function create_tarball(filename, data, cb) {
  var stream = storage.add_tarball(name, filename)
  stream.on('error', function(err) {
    cb(err)
  })
  stream.on('success', function() {
    cb()
  })
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.add_version"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>add_version (name, version, metadata, tag, callback)](#apidoc.element.sinopia.local_storage.prototype.add_version)
- description and source-code
```javascript
add_version = function (name, version, metadata, tag, callback) {
  var self = this
  self.update_package(name, function updater(data, cb) {
    // keep only one readme per package
    data.readme = metadata.readme
    delete metadata.readme

    if (data.versions[version] != null) {
      return cb( Error[409]('this version already present') )
    }

    // if uploaded tarball has a different shasum, it's very likely that we have some kind of error
    if (Utils.is_object(metadata.dist) && typeof(metadata.dist.tarball) === 'string') {
      var tarball = metadata.dist.tarball.replace(/.*\//, '')
      if (Utils.is_object(data._attachments[tarball])) {
        if (data._attachments[tarball].shasum != null && metadata.dist.shasum != null) {
          if (data._attachments[tarball].shasum != metadata.dist.shasum) {
            return cb( Error[400]('shasum error, '
                                + data._attachments[tarball].shasum
                                + ' != ' + metadata.dist.shasum) )
          }
        }

        data._attachments[tarball].version = version
      }
    }

    data.versions[version] = metadata
    Utils.tag_version(data, version, tag, self.config)
    self.config.localList.add(name)
    cb()
  }, callback)
}
```
- example usage
```shell
...

    // this is dumb and memory-consuming, but what choices do we have?
    stream.end(Buffer(data.data, 'base64'))
    stream.done()
  }

  function create_version(version, data, cb) {
    storage.add_version(name, version, data, null, cb)
  }

  function add_tags(tags, cb) {
    storage.merge_tags(name, tags, cb)
  }
})
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.change_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>change_package (name, metadata, revision, callback)](#apidoc.element.sinopia.local_storage.prototype.change_package)
- description and source-code
```javascript
change_package = function (name, metadata, revision, callback) {
  var self = this

  if (!Utils.is_object(metadata.versions) || !Utils.is_object(metadata['dist-tags'])) {
    return callback( Error[422]('bad data') )
  }

  self.update_package(name, function updater(data, cb) {
    for (var ver in data.versions) {
      if (metadata.versions[ver] == null) {
        self.logger.info( { name: name, version: ver }
                        , 'unpublishing @{name}@@{version}')
        delete data.versions[ver]

        for (var file in data._attachments) {
          if (data._attachments[file].version === ver) {
            delete data._attachments[file].version
          }
        }
      }
    }
    data['dist-tags'] = metadata['dist-tags']
    cb()
  }, function(err) {
    if (err) return callback(err)
    callback()
  })
}
```
- example usage
```shell
...
try {
  var metadata = Utils.validate_metadata(req.body, name)
} catch(err) {
  return next( Error[422]('bad incoming package data') )
}

if (req.params._rev) {
  storage.change_package(name, metadata, req.params.revision, function(err) {
    after_change(err, 'package changed')
  })
} else {
  storage.add_package(name, metadata, function(err) {
    after_change(err, 'created new package')
  })
}
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.get_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.local_storage.prototype.get_package)
- description and source-code
```javascript
get_package = function (name, options, callback) {
  if (typeof(options) === 'function') callback = options, options = {}

  var self = this
  var storage = self.storage(name)
  if (!storage) return callback( Error[404]('no such package available') )

  storage.read_json(info_file, function(err, result) {
    if (err) {
      if (err.code === 'ENOENT') {
        return callback( Error[404]('no such package available') )
      } else {
        return callback(self._internal_error(err, info_file, 'error reading'))
      }
    }
    self._normalize_package(result)
    callback(err, result)
  })
}
```
- example usage
```shell
...
  })
  app.get('/-/whoami', function(req, res, next) {
    next({ username: req.remote_user.name })
  })

  // TODO: anonymous user?
  app.get('/:package/:version?', can('access'), function(req, res, next) {
    storage.get_package(req.params.package, { req: req }, function(err, info) {
if (err) return next(err)
info = Utils.filter_tarball_urls(info, req, config)

var version = req.params.version
if (!version) return next(info)

var t = Utils.get_version(info, version)
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.get_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>get_tarball (name, filename, callback)](#apidoc.element.sinopia.local_storage.prototype.get_tarball)
- description and source-code
```javascript
get_tarball = function (name, filename, callback) {
  assert(Utils.validate_name(filename))
  var self = this

  var stream = MyStreams.ReadTarballStream()
  stream.abort = function() {
    if (rstream) rstream.abort()
  }

  var storage = self.storage(name)
  if (!storage) {
    process.nextTick(function() {
      stream.emit('error', Error[404]('no such file available'))
    })
    return stream
  }

  var rstream = storage.read_stream(filename)
  rstream.on('error', function(err) {
    if (err && err.code === 'ENOENT') {
      stream.emit('error', Error(404, 'no such file available'))
    } else {
      stream.emit('error', err)
    }
  })
  rstream.on('content-length', function(v) {
    stream.emit('content-length', v)
  })
  rstream.on('open', function() {
    // re-emitting open because it's handled in storage.js
    stream.emit('open')
    rstream.pipe(stream)
  })
  return stream
}
```
- example usage
```shell
...
    }

    return next( Error[404]('version not found: ' + req.params.version) )
  })
})

app.get('/:package/-/:filename', can('access'), function(req, res, next) {
  var stream = storage.get_tarball(req.params.package, req.params.filename)
  stream.on('content-length', function(v) {
    res.header('Content-Length', v)
  })
  stream.on('error', function(err) {
    return res.report_error(err)
  })
  res.header('Content-Type', 'application/octet-stream')
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.merge_tags"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>merge_tags (name, tags, callback)](#apidoc.element.sinopia.local_storage.prototype.merge_tags)
- description and source-code
```javascript
merge_tags = function (name, tags, callback) {
  var self = this

  self.update_package(name, function updater(data, cb) {
    for (var t in tags) {
      if (tags[t] === null) {
        delete data['dist-tags'][t]
        continue
      }

      if (data.versions[tags[t]] == null) {
        return cb( Error[404]("this version doesn't exist") )
      }

      Utils.tag_version(data, tags[t], t, self.config)
    }
    cb()
  }, callback)
}
```
- example usage
```shell
...
})

function tag_package_version(req, res, next) {
  if (typeof(req.body) !== 'string') return next('route')

  var tags = {}
  tags[req.params.tag] = req.body
  storage.merge_tags(req.params.package, tags, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'package tagged' })
  })
}

// tagging a package
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.remove_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>remove_package (name, callback)](#apidoc.element.sinopia.local_storage.prototype.remove_package)
- description and source-code
```javascript
remove_package = function (name, callback) {
  var self = this
  self.logger.info( { name: name }
                  , 'unpublishing @{name} (all)')

  var storage = self.storage(name)
  if (!storage) return callback( Error[404]('no such package available') )

  storage.read_json(info_file, function(err, data) {
    if (err) {
      if (err.code === 'ENOENT') {
        return callback( Error[404]('no such package available') )
      } else {
        return callback(err)
      }
    }
    self._normalize_package(data)

    storage.unlink(info_file, function(err) {
      if (err) return callback(err)

      var files = Object.keys(data._attachments)

      function unlinkNext(cb) {
        if (files.length === 0) return cb()

        var file = files.shift()
        storage.unlink(file, function() {
          unlinkNext(cb)
        })
      }

      unlinkNext(function() {
        // try to unlink the directory, but ignore errors because it can fail
        storage.rmdir('.', function(err) {
          callback(err)
        })
      })
    })
  })

  Search.remove(name)
  this.config.localList.remove(name)
}
```
- example usage
```shell
...
  function add_tags(tags, cb) {
    storage.merge_tags(name, tags, cb)
  }
})

// unpublishing an entire package
app.delete('/:package/-rev/*', can('publish'), function(req, res, next) {
  storage.remove_package(req.params.package, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'package removed' })
  })
})

// removing a tarball
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.remove_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>remove_tarball (name, filename, revision, callback)](#apidoc.element.sinopia.local_storage.prototype.remove_tarball)
- description and source-code
```javascript
remove_tarball = function (name, filename, revision, callback) {
  assert(Utils.validate_name(filename))
  var self = this

  self.update_package(name, function updater(data, cb) {
    if (data._attachments[filename]) {
      delete data._attachments[filename]
      cb()
    } else {
      cb(Error[404]('no such file available'))
    }
  }, function(err) {
    if (err) return callback(err)
    var storage = self.storage(name)
    if (storage) storage.unlink(filename, callback)
  })
}
```
- example usage
```shell
...
    res.status(201)
    return next({ ok: 'package removed' })
  })
})

// removing a tarball
app.delete('/:package/-/:filename/-rev/:revision', can('publish'), function(req, res, next) {
  storage.remove_tarball(req.params.package, req.params.filename, req.params.revision, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'tarball removed' })
  })
})

// uploading package tarball
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.replace_tags"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>replace_tags (name, tags, callback)](#apidoc.element.sinopia.local_storage.prototype.replace_tags)
- description and source-code
```javascript
replace_tags = function (name, tags, callback) {
  var self = this

  self.update_package(name, function updater(data, cb) {
    data['dist-tags'] = {}

    for (var t in tags) {
      if (tags[t] === null) {
        delete data['dist-tags'][t]
        continue
      }

      if (data.versions[tags[t]] == null) {
        return cb( Error[404]("this version doesn't exist") )
      }

      Utils.tag_version(data, tags[t], t, self.config)
    }
    cb()
  }, callback)
}
```
- example usage
```shell
...
  })
})

app.put('/-/package/:package/dist-tags',
    can('publish'), media('application/json'), expect_json,
    function(req, res, next) {

  storage.replace_tags(req.params.package, req.body, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'tags updated' })
  })
})

app.delete('/-/package/:package/dist-tags',
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.search"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.local_storage.prototype.search)
- description and source-code
```javascript
search = function (startkey, options) {
  var self = this

  var stream = new Stream.PassThrough({ objectMode: true })

  self._each_package(function on_package(item, cb) {
    fs.stat(item.path, function(err, stats) {
      if (err) return cb(err)

      if (stats.mtime > startkey) {
        self.get_package(item.name, options, function(err, data) {
          if (err) return cb(err)

          var versions = Utils.semver_sort(Object.keys(data.versions))
          var latest = versions[versions.length - 1]

          if (data.versions[latest]) {
            stream.push({
              name           : data.versions[latest].name,
              description    : data.versions[latest].description,
              'dist-tags'    : { latest: latest },
              maintainers    : data.versions[latest].maintainers ||
                                 [ data.versions[latest]._npmUser ].filter(Boolean),
              author         : data.versions[latest].author,
              repository     : data.versions[latest].repository,
              readmeFilename : data.versions[latest].readmeFilename || '',
              homepage       : data.versions[latest].homepage,
              keywords       : data.versions[latest].keywords,
              bugs           : data.versions[latest].bugs,
              license        : data.versions[latest].license,
              time           : { modified: item.time ? new Date(item.time).toISOString() : undefined },
              versions       : {},
            })
          }

          cb()
        })
      } else {
        cb()
      }
    })
  }, function on_end(err) {
    if (err) return stream.emit('error', err)
    stream.end()
  })

  return stream
}
```
- example usage
```shell
...
    var received_end      = false
    var response_finished = false
    var processing_pkgs   = 0

    res.status(200)
    res.write('{"_updated":' + Date.now());

    var stream = storage.search(req.param.startkey || 0, { req: req })

    stream.on('data', function each(pkg) {
processing_pkgs++

auth.allow_access(pkg.name, req.remote_user, function(err, allowed) {
  processing_pkgs--
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.storage"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>storage (package)](#apidoc.element.sinopia.local_storage.prototype.storage)
- description and source-code
```javascript
storage = function (package) {
  var path = this.config.get_package_spec(package).storage
  if (path == null) path = this.config.storage
  if (path == null || path === false) {
    this.logger.debug( { name: package }
                     , 'this package has no storage defined: @{name}' )
    return null
  }
  return Path_Wrapper(
    Path.join(
      Path.resolve(Path.dirname(this.config.self_path), path),
      package
    )
  )
}
```
- example usage
```shell
...
Storage.prototype._internal_error = function(err, file, message) {
this.logger.error( { err: err, file: file }
                 , message + ' @{file}: @{!err.message}' )
return Error[500]()
}

Storage.prototype.add_package = function(name, info, callback) {
var storage = this.storage(name)
if (!storage) return callback( Error[404]('this package cannot be added') )

storage.create_json(info_file, get_boilerplate(name), function(err) {
  if (err && err.code === 'EEXISTS') {
    return callback( Error[409]('this package is already present') )
  }
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.update_package"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>update_package (name, updateFn, _callback)](#apidoc.element.sinopia.local_storage.prototype.update_package)
- description and source-code
```javascript
update_package = function (name, updateFn, _callback) {
  var self = this
  var storage = self.storage(name)
  if (!storage) return _callback( Error[404]('no such package available') )
  storage.lock_and_read_json(info_file, function(err, fd, json) {
    function callback() {
      var _args = arguments
      if (fd) {
        fs.close(fd, function(err) {
          if (err) return _callback(err)
          _callback.apply(null, _args)
        })
      } else {
        _callback.apply(null, _args)
      }
    }

    if (err) {
      if (err.code === 'EAGAIN') {
        return callback( Error[503]('resource temporarily unavailable') )
      } else if (err.code === 'ENOENT') {
        return callback( Error[404]('no such package available') )
      } else {
        return callback(err)
      }
    }

    self._normalize_package(json)
    updateFn(json, function(err) {
      if (err) return callback(err)

      self._write_package(name, json, callback)
    })
  })
}
```
- example usage
```shell
...
  callback(null, data)
}
  })
}

Storage.prototype.add_version = function(name, version, metadata, tag, callback) {
  var self = this
  self.update_package(name, function updater(data, cb) {
// keep only one readme per package
data.readme = metadata.readme
delete metadata.readme

if (data.versions[version] != null) {
  return cb( Error[409]('this version already present') )
}
...
```

#### <a name="apidoc.element.sinopia.local_storage.prototype.update_versions"></a>[function <span class="apidocSignatureSpan">sinopia.local_storage.prototype.</span>update_versions (name, newdata, callback)](#apidoc.element.sinopia.local_storage.prototype.update_versions)
- description and source-code
```javascript
update_versions = function (name, newdata, callback) {
  var self = this
  self._read_create_package(name, function(err, data) {
    if (err) return callback(err)

    var change = false
    for (var ver in newdata.versions) {
      if (data.versions[ver] == null) {
        var verdata = newdata.versions[ver]

        // we don't keep readmes for package versions,
        // only one readme per package
        delete verdata.readme

        change = true
        data.versions[ver] = verdata

        if (verdata.dist && verdata.dist.tarball) {
          var filename = URL.parse(verdata.dist.tarball).pathname.replace(/^.*\//, '')
          // we do NOT overwrite any existing records
          if (data._distfiles[filename] == null) {
            var hash = data._distfiles[filename] = {
              url: verdata.dist.tarball,
              sha: verdata.dist.shasum,
            }

            if (verdata._sinopia_uplink) {
              // if we got this information from a known registry,
              // use the same protocol for the tarball
              //
              // see https://github.com/rlidwka/sinopia/issues/166
              var tarball_url = URL.parse(hash.url)
              var uplink_url  = URL.parse(self.config.uplinks[verdata._sinopia_uplink].url)
              if (uplink_url.host === tarball_url.host) {
                tarball_url.protocol = uplink_url.protocol
                hash.registry = verdata._sinopia_uplink
                hash.url = URL.format(tarball_url)
              }
            }
          }
        }
      }
    }
    for (var tag in newdata['dist-tags']) {
      if (!Array.isArray(data['dist-tags'][tag]) || data['dist-tags'][tag].length != newdata['dist-tags'][tag].length) {
        // backward compat
        var need_change = true
      } else {
        for (var i=0; i<data['dist-tags'][tag].length; i++) {
          if (data['dist-tags'][tag][i] != newdata['dist-tags'][tag][i]) {
            var need_change = true
            break
          }
        }
      }

      if (need_change) {
        change = true
        data['dist-tags'][tag] = newdata['dist-tags'][tag]
      }
    }
    for (var up in newdata._uplinks) {
      var need_change = !Utils.is_object(data._uplinks[up])
                     || newdata._uplinks[up].etag !== data._uplinks[up].etag
                     || newdata._uplinks[up].fetched !== data._uplinks[up].fetched

      if (need_change) {
        change = true
        data._uplinks[up] = newdata._uplinks[up]
      }
    }
    if (newdata.readme !== data.readme) {
      data.readme = newdata.readme
      change = true
    }

    if (change) {
      self.logger.debug('updating package info')
      self._write_package(name, data, function(err) {
        callback(err, data)
      })
    } else {
      callback(null, data)
    }
  })
}
```
- example usage
```shell
...

    if (!exists) {
      return callback( Error[404]('no such package available')
                     , null
                     , uplink_errors )
    }

    self.local.update_versions(name, pkginfo, function(err, pkginfo) {
      if (err) return callback(err)
      return callback(null, pkginfo, uplink_errors)
    })
  })
}

// function gets a local info and an info from uplinks and tries to merge it
...
```



# <a name="apidoc.module.sinopia.logger"></a>[module sinopia.logger](#apidoc.module.sinopia.logger)

#### <a name="apidoc.element.sinopia.logger.setup"></a>[function <span class="apidocSignatureSpan">sinopia.logger.</span>setup (logs)](#apidoc.element.sinopia.logger.setup)
- description and source-code
```javascript
setup = function (logs) {
  var streams = []
  if (logs == null) logs = [{ type: 'stdout', format: 'pretty', level: 'http' }]

  logs.forEach(function(target) {
    var stream = new Stream()
    stream.writable = true

    if (target.type === 'stdout' || target.type === 'stderr') {
      // destination stream
      var dest = target.type === 'stdout' ? process.stdout : process.stderr

      if (target.format === 'pretty') {
        // making fake stream for prettypritting
        stream.write = function(obj) {
          dest.write(print(obj.level, obj.msg, obj, dest.isTTY) + '\n')
        }
      } else {
        stream.write = function(obj) {
          dest.write(JSON.stringify(obj, Logger.safeCycles()) + '\n')
        }
      }
    } else if (target.type === 'file') {
      var dest = require('fs').createWriteStream(target.path, {flags: 'a', encoding: 'utf8'})
      dest.on('error', function (err) {
        Logger.emit('error', err)
      })
      stream.write = function(obj) {
        if (target.format === 'pretty') {
          dest.write(print(obj.level, obj.msg, obj, false) + '\n')
        } else {
          dest.write(JSON.stringify(obj, Logger.safeCycles()) + '\n')
        }
      }
    } else {
      throw Error('wrong target type for a log')
    }

    if (target.level === 'http') target.level = 35
    streams.push({
      type: 'raw',
      level: target.level || 35,
      stream: stream,
    })
  })

  var logger = new Logger({
    name: 'sinopia',
    streams: streams,
    serializers: {
      err: Logger.stdSerializers.err,
      req: Logger.stdSerializers.req,
      res: Logger.stdSerializers.res,
    },
  })

  module.exports.logger = logger
}
```
- example usage
```shell
...
try {
  // for debugging memory leaks
  // totally optional
  require('heapdump')
} catch(err) {}

var logger = require('./logger')
logger.setup() // default setup

var commander = require('commander')
var constants = require('constants')
var fs        = require('fs')
var http      = require('http')
var https     = require('https')
var YAML      = require('js-yaml')
...
```



# <a name="apidoc.module.sinopia.middleware"></a>[module sinopia.middleware](#apidoc.module.sinopia.middleware)

#### <a name="apidoc.element.sinopia.middleware.allow"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>allow (auth)](#apidoc.element.sinopia.middleware.allow)
- description and source-code
```javascript
allow = function (auth) {
  return function(action) {
    return function(req, res, next) {
      req.pause();
      auth['allow_'+action](req.params.package, req.remote_user, function(error, is_allowed) {
        req.resume();
        if (error) {
          next(error)
        } else if (is_allowed) {
          next()
        } else {
          // last plugin (that's our built-in one) returns either
          // cb(err) or cb(null, true), so this should never happen
          throw Error('bug in the auth plugin system')
        }
      })
    }
  }
}
```
- example usage
```shell
...
var match         = Middleware.match
var media         = Middleware.media
var validate_name = Middleware.validate_name
var validate_pkg  = Middleware.validate_package

module.exports = function(config, auth, storage) {
var app = express.Router()
var can = Middleware.allow(auth)

// validate all of these params as a package name
// this might be too harsh, so ask if it causes trouble
app.param('package',  validate_pkg)
app.param('filename', validate_name)
app.param('tag',      validate_name)
app.param('version',  validate_name)
...
```

#### <a name="apidoc.element.sinopia.middleware.anti_loop"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>anti_loop (config)](#apidoc.element.sinopia.middleware.anti_loop)
- description and source-code
```javascript
anti_loop = function (config) {
  return function(req, res, next) {
    if (req.headers.via != null) {
      var arr = req.headers.via.split(',')

      for (var i=0; i<arr.length; i++) {
        var m = arr[i].match(/\s*(\S+)\s+(\S+)/)
        if (m && m[2] === config.server_id) {
          return next( Error[508]('loop detected') )
        }
      }
    }
    next()
  }
}
```
- example usage
```shell
...
app.param('_rev',             match(/^-rev$/))
app.param('org_couchdb_user', match(/^org\.couchdb\.user:/))
app.param('anything',         match(/.*/))

app.use(auth.basic_middleware())
//app.use(auth.bearer_middleware())
app.use(expressJson5({ strict: false, limit: config.max_body_size || '10mb' }))
app.use(Middleware.anti_loop(config))

// for "npm whoami"
app.get('/whoami', function(req, res, next) {
  if (req.headers.referer === 'whoami') {
    next({ username: req.remote_user.name })
  } else {
    next('route')
...
```

#### <a name="apidoc.element.sinopia.middleware.expect_json"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>expect_json (req, res, next)](#apidoc.element.sinopia.middleware.expect_json)
- description and source-code
```javascript
function expect_json(req, res, next) {
  if (!utils.is_object(req.body)) {
    return next( Error[400]("can't parse incoming json") )
  }
  next()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.middleware.final"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>final (body, req, res, next)](#apidoc.element.sinopia.middleware.final)
- description and source-code
```javascript
final = function (body, req, res, next) {
  if (res.statusCode === 401 && !res.getHeader('WWW-Authenticate')) {
    // they say it's required for 401, so...
    res.header('WWW-Authenticate', 'Basic, Bearer')
  }

  try {
    if (typeof(body) === 'string' || typeof(body) === 'object') {
      if (!res.getHeader('Content-type')) {
        res.header('Content-type', 'application/json')
      }

      if (typeof(body) === 'object' && body != null) {
        if (typeof(body.error) === 'string') {
          res._sinopia_error = body.error
        }
        body = JSON.stringify(body, undefined, '  ') + '\n'
      }

      // don't send etags with errors
      if (!res.statusCode || (res.statusCode >= 200 && res.statusCode < 300)) {
        res.header('ETag', '"' + md5sum(body) + '"')
      }
    } else {
      // send(null), send(204), etc.
    }
  } catch(err) {
    // if sinopia sends headers first, and then calls res.send()
    // as an error handler, we can't report error properly,
    // and should just close socket
    if (err.message.match(/set headers after they are sent/)) {
      if (res.socket != null) res.socket.destroy()
      return
    } else {
      throw err
    }
  }

  res.send(body)
}
```
- example usage
```shell
...

return data
}

Auth.prototype.aes_encrypt = function(buf) {
var c = Crypto.createCipher('aes192', this.secret)
var b1 = c.update(buf)
var b2 = c.final()
return Buffer.concat([ b1, b2 ])
}

Auth.prototype.aes_decrypt = function(buf) {
try {
  var c = Crypto.createDecipher('aes192', this.secret)
  var b1 = c.update(buf)
...
```

#### <a name="apidoc.element.sinopia.middleware.log"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>log (req, res, next)](#apidoc.element.sinopia.middleware.log)
- description and source-code
```javascript
log = function (req, res, next) {
  // logger
  req.log = Logger.logger.child({ sub: 'in' })

  var _auth = req.headers.authorization
  if (_auth != null) req.headers.authorization = '<Classified>'
  var _cookie = req.headers.cookie
  if (_cookie != null) req.headers.cookie = '<Classified>'

  req.url = req.originalUrl
  req.log.info( { req: req, ip: req.ip }
              , '@{ip} requested \'@{req.method} @{req.url}\'' )
  req.originalUrl = req.url

  if (_auth != null) req.headers.authorization = _auth
  if (_cookie != null) req.headers.cookie = _cookie

  var bytesin = 0
  req.on('data', function(chunk) {
    bytesin += chunk.length
  })

  var bytesout = 0
  var _write = res.write
  res.write = function(buf) {
    bytesout += buf.length
    _write.apply(res, arguments)
  }

  function log() {
    var message = "@{status}, user: @{user}, req: '@{request.method} @{request.url}'"
    if (res._sinopia_error) {
      message += ', error: @{!error}'
    } else {
      message += ', bytes: @{bytes.in}/@{bytes.out}'
    }

    req.url = req.originalUrl
    req.log.warn({
      request : { method: req.method, url: req.url },
      level   : 35, // http
      user    : req.remote_user && req.remote_user.name,
      status  : res.statusCode,
      error   : res._sinopia_error,
      bytes   : {
        in  : bytesin,
        out : bytesout,
      }
    }, message)
    req.originalUrl = req.url
  }

  req.on('close', function() {
    log(true)
  })

  var _end = res.end
  res.end = function(buf) {
    if (buf) bytesout += buf.length
    _end.apply(res, arguments)
    log()
  }
  next()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.middleware.match"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>match (regexp)](#apidoc.element.sinopia.middleware.match)
- description and source-code
```javascript
function match(regexp) {
  return function(req, res, next, value, name) {
    if (regexp.exec(value)) {
      next()
    } else {
      next('route')
    }
  }
}
```
- example usage
```shell
...
  }
}

var users = {all:true, anonymous:true, 'undefined':true, owner:true, none:true}

var check_user_or_uplink = function(arg) {
  assert(arg !== 'all' && arg !== 'owner' && arg !== 'anonymous' && arg !== 'undefined' && arg !== 'none', 'CONFIG: reserved user
/uplink name: ' + arg)
  assert(!arg.match(/\s/), 'CONFIG: invalid user name: ' + arg)
  assert(users[arg] == null, 'CONFIG: duplicate user/uplink name: ' + arg)
  users[arg] = true
}

;[ 'users', 'uplinks', 'packages' ].forEach(function(x) {
  if (self[x] == null) self[x] = {}
  assert(Utils.is_object(self[x]), 'CONFIG: bad "'+x+'" value (object expected)')
...
```

#### <a name="apidoc.element.sinopia.middleware.media"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>media (expect)](#apidoc.element.sinopia.middleware.media)
- description and source-code
```javascript
function media(expect) {
  return function(req, res, next) {
    if (req.headers['content-type'] !== expect) {
      next( Error[415]('wrong content-type, expect: ' + expect
                     + ', got: '+req.headers['content-type']) )
    } else {
      next()
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sinopia.middleware.validate_name"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>validate_name (req, res, next, value, name)](#apidoc.element.sinopia.middleware.validate_name)
- description and source-code
```javascript
function validate_name(req, res, next, value, name) {
  if (value.charAt(0) === '-') {
    // special case in couchdb usually
    next('route')
  } else if (utils.validate_name(value)) {
    next()
  } else {
    next( Error[403]('invalid ' + name) )
  }
}
```
- example usage
```shell
...
}, function(err) {
  if (err) return callback(err)
  callback()
})
}

Storage.prototype.remove_tarball = function(name, filename, revision, callback) {
assert(Utils.validate_name(filename))
var self = this

self.update_package(name, function updater(data, cb) {
  if (data._attachments[filename]) {
    delete data._attachments[filename]
    cb()
  } else {
...
```

#### <a name="apidoc.element.sinopia.middleware.validate_package"></a>[function <span class="apidocSignatureSpan">sinopia.middleware.</span>validate_package (req, res, next, value, name)](#apidoc.element.sinopia.middleware.validate_package)
- description and source-code
```javascript
function validate_package(req, res, next, value, name) {
  if (value.charAt(0) === '-') {
    // special case in couchdb usually
    next('route')
  } else if (utils.validate_package(value)) {
    next()
  } else {
    next( Error[403]('invalid ' + name) )
  }
}
```
- example usage
```shell
...
  }
}

module.exports.validate_package = function validate_package(req, res, next, value, name) {
  if (value.charAt(0) === '-') {
    // special case in couchdb usually
    next('route')
  } else if (utils.validate_package(value)) {
    next()
  } else {
    next( Error[403]('invalid ' + name) )
  }
}

module.exports.media = function media(expect) {
...
```



# <a name="apidoc.module.sinopia.plugin_loader"></a>[module sinopia.plugin_loader](#apidoc.module.sinopia.plugin_loader)

#### <a name="apidoc.element.sinopia.plugin_loader.load_plugins"></a>[function <span class="apidocSignatureSpan">sinopia.plugin_loader.</span>load_plugins (config, plugin_configs, params, sanity_check)](#apidoc.element.sinopia.plugin_loader.load_plugins)
- description and source-code
```javascript
function load_plugins(config, plugin_configs, params, sanity_check) {
  var plugins = Object.keys(plugin_configs || {}).map(function(p) {
    var plugin

    // npm package
    if (plugin == null && p.match(/^[^\.\/]/)) {
      plugin = try_load('sinopia-' + p)
    }

    if (plugin == null) {
      plugin = try_load(p)
    }

    // relative to config path
    if (plugin == null && p.match(/^\.\.?($|\/)/)) {
      plugin = try_load(Path.resolve(Path.dirname(config.self_path), p))
    }

    if (plugin == null) {
      throw Error('"' + p + '" plugin not found\n'
        + 'try "npm install sinopia-' + p + '"')
    }

    if (typeof(plugin) !== 'function')
      throw Error('"' + p + '" doesn\'t look like a valid plugin')

    plugin = plugin(plugin_configs[p], params)

    if (plugin == null || !sanity_check(plugin))
      throw Error('"' + p + '" doesn\'t look like a valid plugin')

    return plugin
  })

  return plugins
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.status_cats"></a>[module sinopia.status_cats](#apidoc.module.sinopia.status_cats)

#### <a name="apidoc.element.sinopia.status_cats.get_image"></a>[function <span class="apidocSignatureSpan">sinopia.status_cats.</span>get_image (status)](#apidoc.element.sinopia.status_cats.get_image)
- description and source-code
```javascript
get_image = function (status) {
  if (status in images) {
    return 'http://flic.kr/p/' + images[status]
    //return 'https://secure.flickr.com/photos/girliemac/'+images[status]+'/in/set-72157628409467125/lightbox/'
  }
}
```
- example usage
```shell
...
  }
}

module.exports.middleware = function(req, res, next) {
  var _writeHead = res.writeHead
  res.writeHead = function(status) {
    if (status in images) {
      res.setHeader('X-Status-Cat', module.exports.get_image(status))
    }
    _writeHead.apply(res, arguments)
  }

  next()
}
...
```

#### <a name="apidoc.element.sinopia.status_cats.middleware"></a>[function <span class="apidocSignatureSpan">sinopia.status_cats.</span>middleware (req, res, next)](#apidoc.element.sinopia.status_cats.middleware)
- description and source-code
```javascript
middleware = function (req, res, next) {
  var _writeHead = res.writeHead
  res.writeHead = function(status) {
    if (status in images) {
      res.setHeader('X-Status-Cat', module.exports.get_image(status))
    }
    _writeHead.apply(res, arguments)
  }

  next()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.storage"></a>[module sinopia.storage](#apidoc.module.sinopia.storage)

#### <a name="apidoc.element.sinopia.storage.storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>storage (config)](#apidoc.element.sinopia.storage.storage)
- description and source-code
```javascript
function Storage(config) {
  var self = Object.create(Storage.prototype)
  self.config = config

  // we support a number of uplinks, but only one local storage
  // Proxy and Local classes should have similar API interfaces
  self.uplinks = {}
  for (var p in config.uplinks) {
    self.uplinks[p] = Proxy(config.uplinks[p], config)
    self.uplinks[p].upname = p
  }
  self.local = Local(config)
  self.logger = Logger.logger.child()

  return self
}
```
- example usage
```shell
...
Storage.prototype._internal_error = function(err, file, message) {
this.logger.error( { err: err, file: file }
                 , message + ' @{file}: @{!err.message}' )
return Error[500]()
}

Storage.prototype.add_package = function(name, info, callback) {
var storage = this.storage(name)
if (!storage) return callback( Error[404]('this package cannot be added') )

storage.create_json(info_file, get_boilerplate(name), function(err) {
  if (err && err.code === 'EEXISTS') {
    return callback( Error[409]('this package is already present') )
  }
...
```

#### <a name="apidoc.element.sinopia.storage._merge_versions"></a>[function <span class="apidocSignatureSpan">sinopia.storage.</span>_merge_versions (local, up, config)](#apidoc.element.sinopia.storage._merge_versions)
- description and source-code
```javascript
_merge_versions = function (local, up, config) {
  // copy new versions to a cache
  // NOTE: if a certain version was updated, we can't refresh it reliably
  for (var i in up.versions) {
    if (local.versions[i] == null) {
      local.versions[i] = up.versions[i]
    }
  }

  // refresh dist-tags
  for (var i in up['dist-tags']) {
    var added = Utils.tag_version(local, up['dist-tags'][i], i, config || {})
    if (i === 'latest' && added) {
      // if remote has more fresh package, we should borrow its readme
      local.readme = up.readme
    }
  }
}
```
- example usage
```shell
...
    enumerable   : false,
    configurable : false,
    writable     : true,
  })
}

try {
  Storage._merge_versions(pkginfo, up_res, self.config)
} catch(err) {
  self.logger.error({
    sub: 'out',
    err: err,
  }, 'package.json parsing error @{!err.message}\n@{err.stack}')
  return cb(null, [ err ])
}
...
```



# <a name="apidoc.module.sinopia.storage.prototype"></a>[module sinopia.storage.prototype](#apidoc.module.sinopia.storage.prototype)

#### <a name="apidoc.element.sinopia.storage.prototype._sync_package_with_uplinks"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>_sync_package_with_uplinks (name, pkginfo, options, callback)](#apidoc.element.sinopia.storage.prototype._sync_package_with_uplinks)
- description and source-code
```javascript
_sync_package_with_uplinks = function (name, pkginfo, options, callback) {
  var self = this

  if (!pkginfo) {
    var exists = false

    pkginfo = {
      name        : name,
      versions    : {},
      'dist-tags' : {},
      _uplinks    : {},
    }
  } else {
    var exists = true
  }

  var uplinks = []
  for (var i in self.uplinks) {
    if (self.config.can_proxy_to(name, i)) {
      uplinks.push(self.uplinks[i])
    }
  }

  async.map(uplinks, function(up, cb) {
    var _options = Object.assign({}, options)
    if (Utils.is_object(pkginfo._uplinks[up.upname])) {
      var fetched = pkginfo._uplinks[up.upname].fetched
      if (fetched && fetched > (Date.now() - up.maxage)) {
        return cb()
      }

      _options.etag = pkginfo._uplinks[up.upname].etag
    }

    up.get_package(name, _options, function(err, up_res, etag) {
      if (err && err.status === 304)
        pkginfo._uplinks[up.upname].fetched = Date.now()

      if (err || !up_res) return cb(null, [err || Error('no data')])

      try {
        Utils.validate_metadata(up_res, name)
      } catch(err) {
        self.logger.error({
          sub: 'out',
          err: err,
        }, 'package.json validating error @{!err.message}\n@{err.stack}')
        return cb(null, [ err ])
      }

      pkginfo._uplinks[up.upname] = {
        etag: etag,
        fetched: Date.now()
      }

      for (var i in up_res.versions) {
        // this won't be serialized to json,
        // kinda like an ES6 Symbol
        Object.defineProperty(up_res.versions[i], '_sinopia_uplink', {
          value        : up.upname,
          enumerable   : false,
          configurable : false,
          writable     : true,
        })
      }

      try {
        Storage._merge_versions(pkginfo, up_res, self.config)
      } catch(err) {
        self.logger.error({
          sub: 'out',
          err: err,
        }, 'package.json parsing error @{!err.message}\n@{err.stack}')
        return cb(null, [ err ])
      }

      // if we got to this point, assume that the correct package exists
      // on the uplink
      exists = true
      cb()
    })
  }, function(err, uplink_errors) {
    assert(!err && Array.isArray(uplink_errors))

    if (!exists) {
      return callback( Error[404]('no such package available')
                     , null
                     , uplink_errors )
    }

    self.local.update_versions(name, pkginfo, function(err, pkginfo) {
      if (err) return callback(err)
      return callback(null, pkginfo, uplink_errors)
    })
  })
}
```
- example usage
```shell
...
if (results) return cb( Error[409]('this package is already present') )

cb()
    })
  }

  function check_package_remote(cb) {
    self._sync_package_with_uplinks(name, null, {}, function(err, results, err_results) {
// something weird
if (err && err.status !== 404) return cb(err)

// checking package
if (results) return cb( Error[409]('this package is already present') )

for (var i=0; i<err_results.length; i++) {
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.add_package"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_package (name, metadata, callback)](#apidoc.element.sinopia.storage.prototype.add_package)
- description and source-code
```javascript
add_package = function (name, metadata, callback) {
  var self = this

  // NOTE:
  // - when we checking package for existance, we ask ALL uplinks
  // - when we publishing package, we only publish it to some of them
  // so all requests are necessary

  check_package_local(function(err) {
    if (err) return callback(err)

    check_package_remote(function(err) {
      if (err) return callback(err)

      publish_package(function(err) {
        if (err) return callback(err)
        callback()
      })
    })
  })

  function check_package_local(cb) {
    self.local.get_package(name, {}, function(err, results) {
      if (err && err.status !== 404) return cb(err)

      if (results) return cb( Error[409]('this package is already present') )

      cb()
    })
  }

  function check_package_remote(cb) {
    self._sync_package_with_uplinks(name, null, {}, function(err, results, err_results) {
      // something weird
      if (err && err.status !== 404) return cb(err)

      // checking package
      if (results) return cb( Error[409]('this package is already present') )

      for (var i=0; i<err_results.length; i++) {
        // checking error
        // if uplink fails with a status other than 404, we report failure
        if (err_results[i][0] != null) {
          if (err_results[i][0].status !== 404) {
            return cb( Error[503]('one of the uplinks is down, refuse to publish') )
          }
        }
      }

      return cb()
    })
  }

  function publish_package(cb) {
    self.local.add_package(name, metadata, callback)
  }
}
```
- example usage
```shell
...
}

if (req.params._rev) {
  storage.change_package(name, metadata, req.params.revision, function(err) {
    after_change(err, 'package changed')
  })
} else {
  storage.add_package(name, metadata, function(err) {
    after_change(err, 'created new package')
  })
}

function after_change(err, ok_message) {
  // old npm behaviour
  if (metadata._attachments == null) {
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.add_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_tarball (name, filename)](#apidoc.element.sinopia.storage.prototype.add_tarball)
- description and source-code
```javascript
add_tarball = function (name, filename) {
  return this.local.add_tarball(name, filename)
}
```
- example usage
```shell
...
        return next({ ok: ok_message })
      })
    })
  })
}

function create_tarball(filename, data, cb) {
  var stream = storage.add_tarball(name, filename)
  stream.on('error', function(err) {
    cb(err)
  })
  stream.on('success', function() {
    cb()
  })
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.add_version"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>add_version (name, version, metadata, tag, callback)](#apidoc.element.sinopia.storage.prototype.add_version)
- description and source-code
```javascript
add_version = function (name, version, metadata, tag, callback) {
  return this.local.add_version(name, version, metadata, tag, callback)
}
```
- example usage
```shell
...

    // this is dumb and memory-consuming, but what choices do we have?
    stream.end(Buffer(data.data, 'base64'))
    stream.done()
  }

  function create_version(version, data, cb) {
    storage.add_version(name, version, data, null, cb)
  }

  function add_tags(tags, cb) {
    storage.merge_tags(name, tags, cb)
  }
})
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.change_package"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>change_package (name, metadata, revision, callback)](#apidoc.element.sinopia.storage.prototype.change_package)
- description and source-code
```javascript
change_package = function (name, metadata, revision, callback) {
  return this.local.change_package(name, metadata, revision, callback)
}
```
- example usage
```shell
...
try {
  var metadata = Utils.validate_metadata(req.body, name)
} catch(err) {
  return next( Error[422]('bad incoming package data') )
}

if (req.params._rev) {
  storage.change_package(name, metadata, req.params.revision, function(err) {
    after_change(err, 'package changed')
  })
} else {
  storage.add_package(name, metadata, function(err) {
    after_change(err, 'created new package')
  })
}
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.get_local"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_local (callback)](#apidoc.element.sinopia.storage.prototype.get_local)
- description and source-code
```javascript
get_local = function (callback) {
  var self = this
  var locals = this.config.localList.get()
  var packages = []

  var getPackage = function(i) {
    self.local.get_package(locals[i], function(err, info) {
      if (!err) {
        var latest = Array.isArray(info['dist-tags'].latest)
                   ? Utils.semver_sort(info['dist-tags'].latest).pop()
                   : info['dist-tags'].latest
        if (info.versions[latest]) {
          packages.push(info.versions[latest])
        } else {
          self.logger.warn( { package: locals[i] }
                          , 'package @{package} does not have a "latest" tag?' )
        }
      }

      if (i >= locals.length - 1) {
        callback(null, packages)
      } else {
        getPackage(i + 1)
      }
    })
  }

  if (locals.length) {
    getPackage(0)
  } else {
    callback(null, [])
  }
}
```
- example usage
```shell
...
  }
  app.get('/', function(req, res, next) {
var base = config.url_prefix
         ? config.url_prefix.replace(/\/$/, '')
         : req.protocol + '://' + req.get('host')
res.setHeader('Content-Type', 'text/html')

storage.get_local(function(err, packages) {
  if (err) throw err // that function shouldn't produce any
  async.filterSeries(packages, function(package, cb) {
    auth.allow_access(package.name, req.remote_user, function(err, allowed) {
      setImmediate(function () {
        cb(!err && allowed)
      })
    })
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.get_package"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.storage.prototype.get_package)
- description and source-code
```javascript
get_package = function (name, options, callback) {
  if (typeof(options) === 'function') callback = options, options = {}

  var self = this

  self.local.get_package(name, options, function(err, data) {
    if (err && (!err.status || err.status >= 500)) {
      // report internal errors right away
      return callback(err)
    }

    self._sync_package_with_uplinks(name, data, options, function(err, result, uplink_errors) {
      if (err) return callback(err)
      var whitelist = [ '_rev', 'name', 'versions', 'dist-tags', 'readme' ]
      for (var i in result) {
        if (whitelist.indexOf(i) === -1) delete result[i]
      }

      if (self.config.ignore_latest_tag || !result['dist-tags'].latest) {
        result['dist-tags'].latest = Utils.semver_sort(Object.keys(result.versions))
      }

      for (var i in result['dist-tags']) {
        if (Array.isArray(result['dist-tags'][i])) {
          result['dist-tags'][i] = result['dist-tags'][i][result['dist-tags'][i].length-1]
          if (result['dist-tags'][i] == null) delete result['dist-tags'][i]
        }
      }

      // npm can throw if this field doesn't exist
      result._attachments = {}

      callback(null, result, uplink_errors)
    })
  })
}
```
- example usage
```shell
...
  })
  app.get('/-/whoami', function(req, res, next) {
    next({ username: req.remote_user.name })
  })

  // TODO: anonymous user?
  app.get('/:package/:version?', can('access'), function(req, res, next) {
    storage.get_package(req.params.package, { req: req }, function(err, info) {
if (err) return next(err)
info = Utils.filter_tarball_urls(info, req, config)

var version = req.params.version
if (!version) return next(info)

var t = Utils.get_version(info, version)
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.get_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>get_tarball (name, filename)](#apidoc.element.sinopia.storage.prototype.get_tarball)
- description and source-code
```javascript
get_tarball = function (name, filename) {
  var stream = MyStreams.ReadTarballStream()
  stream.abort = function() {}

  var self = this

  // if someone requesting tarball, it means that we should already have some
  // information about it, so fetching package info is unnecessary

  // trying local first
  var rstream = self.local.get_tarball(name, filename)
  var is_open = false
  rstream.on('error', function(err) {
    if (is_open || err.status !== 404) {
      return stream.emit('error', err)
    }

    // local reported 404
    var err404 = err
    rstream.abort()
    rstream = null // gc

    self.local.get_package(name, function(err, info) {
      if (!err && info._distfiles && info._distfiles[filename] != null) {
        // information about this file exists locally
        serve_file(info._distfiles[filename])

      } else {
        // we know nothing about this file, trying to get information elsewhere

        self._sync_package_with_uplinks(name, info, {}, function(err, info) {
          if (err) return stream.emit('error', err)

          if (!info._distfiles || info._distfiles[filename] == null) {
            return stream.emit('error', err404)
          }

          serve_file(info._distfiles[filename])
        })
      }
    })
  })
  rstream.on('content-length', function(v) {
    stream.emit('content-length', v)
  })
  rstream.on('open', function() {
    is_open = true
    rstream.pipe(stream)
  })
  return stream

  function serve_file(file) {
    var uplink = null
    for (var p in self.uplinks) {
      if (self.uplinks[p].can_fetch_url(file.url)) {
        uplink = self.uplinks[p]
      }
    }
    if (uplink == null) {
      uplink = Proxy({
        url: file.url,
        _autogenerated: true,
      }, self.config)
    }

    var savestream = self.local.add_tarball(name, filename)
    var on_open = function() {
      on_open = function(){} // prevent it from being called twice
      var rstream2 = uplink.get_url(file.url)
      rstream2.on('error', function(err) {
        if (savestream) savestream.abort()
        savestream = null
        stream.emit('error', err)
      })
      rstream2.on('end', function() {
        if (savestream) savestream.done()
      })

      rstream2.on('content-length', function(v) {
        stream.emit('content-length', v)
        if (savestream) savestream.emit('content-length', v)
      })
      rstream2.pipe(stream)
      if (savestream) rstream2.pipe(savestream)
    }

    savestream.on('open', function() {
      on_open()
    })
    savestream.on('error', function(err) {
      self.logger.warn( { err: err }
                      , 'error saving file: @{err.message}\n@{err.stack}' )
      if (savestream) savestream.abort()
      savestream = null
      on_open()
    })
  }
}
```
- example usage
```shell
...
    }

    return next( Error[404]('version not found: ' + req.params.version) )
  })
})

app.get('/:package/-/:filename', can('access'), function(req, res, next) {
  var stream = storage.get_tarball(req.params.package, req.params.filename)
  stream.on('content-length', function(v) {
    res.header('Content-Length', v)
  })
  stream.on('error', function(err) {
    return res.report_error(err)
  })
  res.header('Content-Type', 'application/octet-stream')
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.merge_tags"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>merge_tags (name, tag_hash, callback)](#apidoc.element.sinopia.storage.prototype.merge_tags)
- description and source-code
```javascript
merge_tags = function (name, tag_hash, callback) {
  return this.local.merge_tags(name, tag_hash, callback)
}
```
- example usage
```shell
...
})

function tag_package_version(req, res, next) {
  if (typeof(req.body) !== 'string') return next('route')

  var tags = {}
  tags[req.params.tag] = req.body
  storage.merge_tags(req.params.package, tags, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'package tagged' })
  })
}

// tagging a package
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.remove_package"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>remove_package (name, callback)](#apidoc.element.sinopia.storage.prototype.remove_package)
- description and source-code
```javascript
remove_package = function (name, callback) {
  return this.local.remove_package(name, callback)
}
```
- example usage
```shell
...
  function add_tags(tags, cb) {
    storage.merge_tags(name, tags, cb)
  }
})

// unpublishing an entire package
app.delete('/:package/-rev/*', can('publish'), function(req, res, next) {
  storage.remove_package(req.params.package, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'package removed' })
  })
})

// removing a tarball
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.remove_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>remove_tarball (name, filename, revision, callback)](#apidoc.element.sinopia.storage.prototype.remove_tarball)
- description and source-code
```javascript
remove_tarball = function (name, filename, revision, callback) {
  return this.local.remove_tarball(name, filename, revision, callback)
}
```
- example usage
```shell
...
    res.status(201)
    return next({ ok: 'package removed' })
  })
})

// removing a tarball
app.delete('/:package/-/:filename/-rev/:revision', can('publish'), function(req, res, next) {
  storage.remove_tarball(req.params.package, req.params.filename, req.params.revision, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'tarball removed' })
  })
})

// uploading package tarball
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.replace_tags"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>replace_tags (name, tag_hash, callback)](#apidoc.element.sinopia.storage.prototype.replace_tags)
- description and source-code
```javascript
replace_tags = function (name, tag_hash, callback) {
  return this.local.replace_tags(name, tag_hash, callback)
}
```
- example usage
```shell
...
  })
})

app.put('/-/package/:package/dist-tags',
    can('publish'), media('application/json'), expect_json,
    function(req, res, next) {

  storage.replace_tags(req.params.package, req.body, function(err) {
    if (err) return next(err)
    res.status(201)
    return next({ ok: 'tags updated' })
  })
})

app.delete('/-/package/:package/dist-tags',
...
```

#### <a name="apidoc.element.sinopia.storage.prototype.search"></a>[function <span class="apidocSignatureSpan">sinopia.storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.storage.prototype.search)
- description and source-code
```javascript
search = function (startkey, options) {
  var self = this

  var stream = new Stream.PassThrough({ objectMode: true })

  async.eachSeries(Object.keys(self.uplinks), function(up_name, cb) {
    // shortcut: if 'local=1' is supplied, don't call uplinks
    if (options.req.query.local !== undefined) return cb()

    var lstream = self.uplinks[up_name].search(startkey, options)
    lstream.pipe(stream, { end: false })
    lstream.on('error', function (err) {
      self.logger.error({ err: err }, 'uplink error: @{err.message}')
      cb(), cb = function () {}
    })
    lstream.on('end', function () {
      cb(), cb = function () {}
    })

    stream.abort = function () {
      if (lstream.abort) lstream.abort()
      cb(), cb = function () {}
    }
  }, function () {
    var lstream = self.local.search(startkey, options)
    stream.abort = function () { lstream.abort() }
    lstream.pipe(stream, { end: true })
    lstream.on('error', function (err) {
      self.logger.error({ err: err }, 'search error: @{err.message}')
      stream.end()
    })
  })

  return stream
}
```
- example usage
```shell
...
    var received_end      = false
    var response_finished = false
    var processing_pkgs   = 0

    res.status(200)
    res.write('{"_updated":' + Date.now());

    var stream = storage.search(req.param.startkey || 0, { req: req })

    stream.on('data', function each(pkg) {
processing_pkgs++

auth.allow_access(pkg.name, req.remote_user, function(err, allowed) {
  processing_pkgs--
...
```



# <a name="apidoc.module.sinopia.streams"></a>[module sinopia.streams](#apidoc.module.sinopia.streams)

#### <a name="apidoc.element.sinopia.streams.ReadTarballStream"></a>[function <span class="apidocSignatureSpan">sinopia.streams.</span>ReadTarballStream (options)](#apidoc.element.sinopia.streams.ReadTarballStream)
- description and source-code
```javascript
function ReadTarball(options) {
  var self = new Stream.PassThrough(options)
  Object.setPrototypeOf(self, ReadTarball.prototype)

  // called when data is not needed anymore
  add_abstract_method(self, 'abort')

  return self
}
```
- example usage
```shell
...
      if (err) return stream.emit('error', err)
      stream.emit('content-length', stats.size)
      stream.emit('open')
      rstream.pipe(stream)
    })
  })

  var stream = MyStreams.ReadTarballStream()
  stream.abort = function() {
    rstream.close()
  }
  return stream
}

function create(name, contents, callback) {
...
```

#### <a name="apidoc.element.sinopia.streams.UploadTarballStream"></a>[function <span class="apidocSignatureSpan">sinopia.streams.</span>UploadTarballStream (options)](#apidoc.element.sinopia.streams.UploadTarballStream)
- description and source-code
```javascript
function UploadTarball(options) {
  var self = new Stream.PassThrough(options)
  Object.setPrototypeOf(self, UploadTarball.prototype)

  // called when user closes connection before upload finishes
  add_abstract_method(self, 'abort')

  // called when upload finishes successfully
  add_abstract_method(self, 'done')

  return self
}
```
- example usage
```shell
...
  } else {
    cb(err)
  }
})
}

function write_stream(name) {
var stream = MyStreams.UploadTarballStream()

var _ended = 0
stream.on('end', function() {
  _ended = 1
})

fs.exists(name, function(exists) {
...
```



# <a name="apidoc.module.sinopia.up_storage"></a>[module sinopia.up_storage](#apidoc.module.sinopia.up_storage)

#### <a name="apidoc.element.sinopia.up_storage.up_storage"></a>[function <span class="apidocSignatureSpan">sinopia.</span>up_storage (config, mainconfig)](#apidoc.element.sinopia.up_storage.up_storage)
- description and source-code
```javascript
function Storage(config, mainconfig) {
  var self = Object.create(Storage.prototype)
  self.config = config
  self.failed_requests = 0
  self.userAgent = mainconfig.user_agent
  self.ca = config.ca
  self.logger = Logger.logger.child({sub: 'out'})
  self.server_id = mainconfig.server_id

  self.url = URL.parse(self.config.url)

  _setupProxy.call(self, self.url.hostname, config, mainconfig, self.url.protocol === 'https:')

  self.config.url = self.config.url.replace(/\/$/, '')
  if (Number(self.config.timeout) >= 1000) {
    self.logger.warn([ 'Too big timeout value: ' + self.config.timeout,
                       'We changed time format to nginx-like one',
                       '(see http://wiki.nginx.org/ConfigNotation)',
                       'so please update your config accordingly' ].join('\n'))
  }

  // a bunch of different configurable timers
  self.maxage       = parse_interval(config_get('maxage'      , '2m' ))
  self.timeout      = parse_interval(config_get('timeout'     , '30s'))
  self.max_fails    =         Number(config_get('max_fails'   ,  2   ))
  self.fail_timeout = parse_interval(config_get('fail_timeout', '5m' ))
  return self

  // just a helper ('config[key] || default' doesn't work because of zeroes)
  function config_get(key, def) {
    return config[key] != null ? config[key] : def
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sinopia.up_storage.prototype"></a>[module sinopia.up_storage.prototype](#apidoc.module.sinopia.up_storage.prototype)

#### <a name="apidoc.element.sinopia.up_storage.prototype._add_proxy_headers"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>_add_proxy_headers (req, headers)](#apidoc.element.sinopia.up_storage.prototype._add_proxy_headers)
- description and source-code
```javascript
_add_proxy_headers = function (req, headers) {
  if (req) {
    // Only submit X-Forwarded-For field if we don't have a proxy selected
    // in the config file.
    //
    // Otherwise misconfigured proxy could return 407:
    // https://github.com/rlidwka/sinopia/issues/254
    //
    if (!this.proxy) {
      headers['X-Forwarded-For'] = (
        req && req.headers['x-forwarded-for']
        ? req.headers['x-forwarded-for'] + ', '
        : ''
      ) + req.connection.remoteAddress
    }
  }

  // always attach Via header to avoid loops, even if we're not proxying
  headers['Via'] =
    req && req.headers['via']
    ? req.headers['via'] + ', '
    : ''

  headers['Via'] += '1.1 ' + this.server_id + ' (Sinopia)'
}
```
- example usage
```shell
...
}

var self = this
var headers = options.headers || {}
headers['Accept']          = headers['Accept']          || 'application/json'
headers['Accept-Encoding'] = headers['Accept-Encoding'] || 'gzip'
headers['User-Agent']      = headers['User-Agent']      || this.userAgent
this._add_proxy_headers(options.req, headers)

var method = options.method   || 'GET'
var uri    = options.uri_full || (this.config.url + options.uri)

self.logger.info({
  method  : method,
  headers : headers,
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.can_fetch_url"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>can_fetch_url (url)](#apidoc.element.sinopia.up_storage.prototype.can_fetch_url)
- description and source-code
```javascript
can_fetch_url = function (url) {
  url = URL.parse(url)

  return url.protocol === this.url.protocol
      && url.host === this.url.host
      && url.path.indexOf(this.url.path) === 0
}
```
- example usage
```shell
...
  rstream.pipe(stream)
})
return stream

function serve_file(file) {
  var uplink = null
  for (var p in self.uplinks) {
    if (self.uplinks[p].can_fetch_url(file.url)) {
      uplink = self.uplinks[p]
    }
  }
  if (uplink == null) {
    uplink = Proxy({
      url: file.url,
      _autogenerated: true,
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.get_package"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_package (name, options, callback)](#apidoc.element.sinopia.up_storage.prototype.get_package)
- description and source-code
```javascript
get_package = function (name, options, callback) {
  if (typeof(options) === 'function') callback = options, options = {}

  var headers = {}
  if (options.etag) {
    headers['If-None-Match'] = options.etag
    headers['Accept']        = 'application/octet-stream'
  }

  this.request({
    uri     : '/' + encode(name),
    json    : true,
    headers : headers,
    req     : options.req,
  }, function(err, res, body) {
    if (err) return callback(err)
    if (res.statusCode === 404) {
      return callback( Error[404]("package doesn't exist on uplink") )
    }
    if (!(res.statusCode >= 200 && res.statusCode < 300)) {
      var error = Error('bad status code: ' + res.statusCode)
      error.remoteStatus = res.statusCode
      return callback(error)
    }
    callback(null, body, res.headers.etag)
  })
}
```
- example usage
```shell
...
  })
  app.get('/-/whoami', function(req, res, next) {
    next({ username: req.remote_user.name })
  })

  // TODO: anonymous user?
  app.get('/:package/:version?', can('access'), function(req, res, next) {
    storage.get_package(req.params.package, { req: req }, function(err, info) {
if (err) return next(err)
info = Utils.filter_tarball_urls(info, req, config)

var version = req.params.version
if (!version) return next(info)

var t = Utils.get_version(info, version)
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.get_tarball"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_tarball (name, options, filename)](#apidoc.element.sinopia.up_storage.prototype.get_tarball)
- description and source-code
```javascript
get_tarball = function (name, options, filename) {
  if (!options) options = {}
  return this.get_url(this.config.url + '/' + name + '/-/' + filename)
}
```
- example usage
```shell
...
    }

    return next( Error[404]('version not found: ' + req.params.version) )
  })
})

app.get('/:package/-/:filename', can('access'), function(req, res, next) {
  var stream = storage.get_tarball(req.params.package, req.params.filename)
  stream.on('content-length', function(v) {
    res.header('Content-Length', v)
  })
  stream.on('error', function(err) {
    return res.report_error(err)
  })
  res.header('Content-Type', 'application/octet-stream')
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.get_url"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>get_url (url)](#apidoc.element.sinopia.up_storage.prototype.get_url)
- description and source-code
```javascript
get_url = function (url) {
  var stream = MyStreams.ReadTarballStream()
  stream.abort = function() {}
  var current_length = 0, expected_length

  var rstream = this.request({
    uri_full: url,
    encoding: null,
    headers: { Accept: 'application/octet-stream' },
  })

  rstream.on('response', function(res) {
    if (res.statusCode === 404) {
      return stream.emit('error', Error[404]("file doesn't exist on uplink"))
    }
    if (!(res.statusCode >= 200 && res.statusCode < 300)) {
      return stream.emit('error', Error('bad uplink status code: ' + res.statusCode))
    }
    if (res.headers['content-length']) {
      expected_length = res.headers['content-length']
      stream.emit('content-length', res.headers['content-length'])
    }

    rstream.pipe(stream)
  })

  rstream.on('error', function(err) {
    stream.emit('error', err)
  })
  rstream.on('data', function(d) {
    current_length += d.length
  })
  rstream.on('end', function(d) {
    if (d) current_length += d.length
    if (expected_length && current_length != expected_length)
      stream.emit('error', Error('content length mismatch'))
  })
  return stream
}
```
- example usage
```shell
...
    _autogenerated: true,
  }, self.config)
}

var savestream = self.local.add_tarball(name, filename)
var on_open = function() {
  on_open = function(){} // prevent it from being called twice
  var rstream2 = uplink.get_url(file.url)
  rstream2.on('error', function(err) {
    if (savestream) savestream.abort()
    savestream = null
    stream.emit('error', err)
  })
  rstream2.on('end', function() {
    if (savestream) savestream.done()
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.request"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>request (options, cb)](#apidoc.element.sinopia.up_storage.prototype.request)
- description and source-code
```javascript
request = function (options, cb) {
  if (!this.status_check()) {
    var req = new Stream.Readable()
    process.nextTick(function() {
      if (typeof(cb) === 'function') cb(Error('uplink is offline'))
      req.emit('error', Error('uplink is offline'))
    })
    // preventing 'Uncaught, unspecified "error" event'
    req.on('error', function(){})
    return req
  }

  var self = this
  var headers = options.headers || {}
  headers['Accept']          = headers['Accept']          || 'application/json'
  headers['Accept-Encoding'] = headers['Accept-Encoding'] || 'gzip'
  headers['User-Agent']      = headers['User-Agent']      || this.userAgent
  this._add_proxy_headers(options.req, headers)

  var method = options.method   || 'GET'
  var uri    = options.uri_full || (this.config.url + options.uri)

  self.logger.info({
    method  : method,
    headers : headers,
    uri     : uri,
  }, "making request: '@{method} @{uri}'")

  if (Utils.is_object(options.json)) {
    var json = JSON.stringify(options.json)
    headers['Content-Type'] = headers['Content-Type'] || 'application/json'
  }

  var request_callback = cb ? (function (err, res, body) {
    var error
    var res_length = err ? 0 : body.length

    do_decode()
    do_log()
    cb(err, res, body)

    function do_decode() {
      if (err) {
        error = err.message
        return
      }

      if (options.json && res.statusCode < 300) {
        try {
          body = JSON.parse(body.toString('utf8'))
        } catch(_err) {
          body = {}
          err = _err
          error = err.message
        }
      }

      if (!err && Utils.is_object(body)) {
        if (typeof(body.error) === 'string') {
          error = body.error
        }
      }
    }

    function do_log() {
      var message = '@{!status}, req: \'@{request.method} @{request.url}\''
      message += error
               ? ', error: @{!error}'
               : ', bytes: @{bytes.in}/@{bytes.out}'
      self.logger.warn({
        err     : err,
        request : { method: method, url: uri },
        level   : 35, // http
        status  : res != null ? res.statusCode : 'ERR',
        error   : error,
        bytes   : {
          in  : json ? json.length : 0,
          out : res_length || 0,
        }
      }, message)
    }
  }) : undefined

  var req = request({
    url      : uri,
    method   : method,
    headers  : headers,
    body     : json,
    ca       : this.ca,
    proxy    : this.proxy,
    encoding : null,
    gzip     : true,
    timeout  : this.timeout,
  }, request_callback)

  var status_called = false
  req.on('response', function(res) {
    if (!req._sinopia_aborted && !status_called) {
      status_called = true
      self.status_check(true)
    }

    if (!request_callback) {
      ;(function do_log() {
        var message = '@{!status}, req: \'@{request.method} @{request.url}\' (streaming)'
        self.logger.warn({
          request : { method: method, url: uri },
          level   : 35, // http
          status  : res != null ? res.statusCode : 'ERR',
        }, message)
      })()
    }
  })
  req.on('error', function(_err) {
    if (!req._sinopia_aborted && !status_called) {
      status_called = true
      self.status_check(false)
    }
  })
  return req
}
```
- example usage
```shell
...

var headers = {}
if (options.etag) {
  headers['If-None-Match'] = options.etag
  headers['Accept']        = 'application/octet-stream'
}

this.request({
  uri     : '/' + encode(name),
  json    : true,
  headers : headers,
  req     : options.req,
}, function(err, res, body) {
  if (err) return callback(err)
  if (res.statusCode === 404) {
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.search"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>search (startkey, options)](#apidoc.element.sinopia.up_storage.prototype.search)
- description and source-code
```javascript
search = function (startkey, options) {
  var self = this

  var stream = new Stream.PassThrough({ objectMode: true })

  var req = self.request({
    uri: options.req.url,
    req: options.req,
  })

  req.on('response', function (res) {
    if (!String(res.statusCode).match(/^2\d\d$/)) {
      return stream.emit('error', Error('bad status code ' + res.statusCode + ' from uplink'))
    }

    res.pipe(JSONStream.parse('*')).on('data', function (pkg) {
      if (Utils.is_object(pkg)) {
        stream.emit('data', pkg)
      }
    })

    res.on('end', function () {
      stream.emit('end')
    })
  })

  req.on('error', function (err) {
    stream.emit('error', err)
  })

  stream.abort = function () {
    req.abort()
    stream.emit('end')
  }

  return stream
}
```
- example usage
```shell
...
    var received_end      = false
    var response_finished = false
    var processing_pkgs   = 0

    res.status(200)
    res.write('{"_updated":' + Date.now());

    var stream = storage.search(req.param.startkey || 0, { req: req })

    stream.on('data', function each(pkg) {
processing_pkgs++

auth.allow_access(pkg.name, req.remote_user, function(err, allowed) {
  processing_pkgs--
...
```

#### <a name="apidoc.element.sinopia.up_storage.prototype.status_check"></a>[function <span class="apidocSignatureSpan">sinopia.up_storage.prototype.</span>status_check (alive)](#apidoc.element.sinopia.up_storage.prototype.status_check)
- description and source-code
```javascript
status_check = function (alive) {
  if (arguments.length === 0) {
    if (this.failed_requests >= this.max_fails
     && Math.abs(Date.now() - this.last_request_time) < this.fail_timeout) {
      return false
    } else {
      return true
    }
  } else {
    if (alive) {
      if (this.failed_requests >= this.max_fails) {
        this.logger.warn({ host: this.url.host }, 'host @{host} is back online')
      }
      this.failed_requests = 0
    } else {
      this.failed_requests++
      if (this.failed_requests === this.max_fails) {
        this.logger.warn({ host: this.url.host }, 'host @{host} is now offline')
      }
    }
    this.last_request_time = Date.now()
  }
}
```
- example usage
```shell
...
} else {
  this.logger.debug( { url: this.url.href, proxy: this.proxy }
                   , 'using proxy @{proxy} for @{url}' )
}
}

Storage.prototype.request = function(options, cb) {
if (!this.status_check()) {
  var req = new Stream.Readable()
  process.nextTick(function() {
    if (typeof(cb) === 'function') cb(Error('uplink is offline'))
    req.emit('error', Error('uplink is offline'))
  })
  // preventing 'Uncaught, unspecified "error" event'
  req.on('error', function(){})
...
```



# <a name="apidoc.module.sinopia.utils"></a>[module sinopia.utils](#apidoc.module.sinopia.utils)

#### <a name="apidoc.element.sinopia.utils.filter_tarball_urls"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>filter_tarball_urls (pkg, req, config)](#apidoc.element.sinopia.utils.filter_tarball_urls)
- description and source-code
```javascript
filter_tarball_urls = function (pkg, req, config) {
  function filter(_url) {
    if (!req.headers.host) return _url

    var filename = URL.parse(_url).pathname.replace(/^.*\//, '')

    if (config.url_prefix != null) {
      var result = config.url_prefix.replace(/\/$/, '')
    } else {
      var result = req.protocol + '://' + req.headers.host
    }

    return result + '/' + pkg.name.replace(/\//g, '%2f') + '/-/' + filename
  }

  for (var ver in pkg.versions) {
    var dist = pkg.versions[ver].dist
    if (dist != null && dist.tarball != null) {
      //dist.__sinopia_orig_tarball = dist.tarball
      dist.tarball = filter(dist.tarball)
    }
  }
  return pkg
}
```
- example usage
```shell
...
    next({ username: req.remote_user.name })
  })

  // TODO: anonymous user?
  app.get('/:package/:version?', can('access'), function(req, res, next) {
    storage.get_package(req.params.package, { req: req }, function(err, info) {
if (err) return next(err)
info = Utils.filter_tarball_urls(info, req, config)

var version = req.params.version
if (!version) return next(info)

var t = Utils.get_version(info, version)
if (t != null) return next(t)
...
```

#### <a name="apidoc.element.sinopia.utils.get_version"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>get_version (object, version)](#apidoc.element.sinopia.utils.get_version)
- description and source-code
```javascript
get_version = function (object, version) {
  if (object.versions[version] != null) return object.versions[version]

  try {
    version = Semver.parse(version, true)
    for (var k in object.versions) {
      if (version.compare(Semver.parse(k, true)) === 0) {
        return object.versions[k]
      }
    }
  } catch (err) {
    return undefined
  }
}
```
- example usage
```shell
...
    storage.get_package(req.params.package, { req: req }, function(err, info) {
if (err) return next(err)
info = Utils.filter_tarball_urls(info, req, config)

var version = req.params.version
if (!version) return next(info)

var t = Utils.get_version(info, version)
if (t != null) return next(t)

if (info['dist-tags'] != null) {
  if (info['dist-tags'][version] != null) {
    version = info['dist-tags'][version]
    t = Utils.get_version(info, version)
    if (t != null) return next(t)
...
```

#### <a name="apidoc.element.sinopia.utils.is_object"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>is_object (obj)](#apidoc.element.sinopia.utils.is_object)
- description and source-code
```javascript
is_object = function (obj) {
  return typeof(obj) === 'object' && obj !== null && !Array.isArray(obj)
}
```
- example usage
```shell
...
  assert(!arg.match(/\s/), 'CONFIG: invalid user name: ' + arg)
  assert(users[arg] == null, 'CONFIG: duplicate user/uplink name: ' + arg)
  users[arg] = true
}

;[ 'users', 'uplinks', 'packages' ].forEach(function(x) {
  if (self[x] == null) self[x] = {}
  assert(Utils.is_object(self[x]), 'CONFIG: bad "'+x+'" value (object expected)')
})

for (var i in self.users) check_user_or_uplink(i)
for (var i in self.uplinks) check_user_or_uplink(i)

for (var i in self.users) {
  assert(self.users[i].password, 'CONFIG: no password for user: ' + i)
...
```

#### <a name="apidoc.element.sinopia.utils.parse_address"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>parse_address (addr)](#apidoc.element.sinopia.utils.parse_address)
- description and source-code
```javascript
function parse_address(addr) {
  //
  // Allow:
  //
  //  - https:localhost:1234        - protocol + host + port
  //  - localhost:1234              - host + port
  //  - 1234                        - port
  //  - http::1234                  - protocol + port
  //  - https://localhost:443/      - full url + https
  //  - http://[::1]:443/           - ipv6
  //  - unix:/tmp/http.sock         - unix sockets
  //  - https://unix:/tmp/http.sock - unix sockets (https)
  //
  // TODO: refactor it to something more reasonable?
  //
  //        protocol :  //      (  host  )|(    ipv6     ):  port  /
  var m = /^((https?):(\/\/)?)?((([^\/:]*)|\[([^\[\]]+)\]):)?(\d+)\/?$/.exec(addr)

  if (m) return {
    proto: m[2] || 'http',
    host:  m[6] || m[7] || 'localhost',
    port:  m[8] || '4873',
  }

  var m = /^((https?):(\/\/)?)?unix:(.*)$/.exec(addr)

  if (m) return {
    proto: m[2] || 'http',
    path:  m[4],
  }

  return null
}
```
- example usage
```shell
...
  } else if (config.listen) {
addresses = [ config.listen ]
  } else {
addresses = [ '4873' ]
  }

  addresses = addresses.map(function(addr) {
var parsed_addr = Utils.parse_address(addr)

if (!parsed_addr) {
  logger.logger.warn({ addr: addr },
     'invalid address - @{addr}, we expect a port (e.g. "4873"),'
   + ' host:port (e.g. "localhost:4873") or full url'
   + ' (e.g. "http://localhost:4873/")')
}
...
```

#### <a name="apidoc.element.sinopia.utils.semver_sort"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>semver_sort (array)](#apidoc.element.sinopia.utils.semver_sort)
- description and source-code
```javascript
function semver_sort(array) {
  return array
        .filter(function(x) {
          if (!Semver.parse(x, true)) {
            Logger.logger.warn( {ver: x}, 'ignoring bad version @{ver}' )
            return false
          }
          return true
        })
        .sort(Semver.compareLoose)
        .map(String)
}
```
- example usage
```shell
...
    fs.stat(item.path, function(err, stats) {
      if (err) return cb(err)

      if (stats.mtime > startkey) {
        self.get_package(item.name, options, function(err, data) {
if (err) return cb(err)

var versions = Utils.semver_sort(Object.keys(data.versions))
var latest = versions[versions.length - 1]

if (data.versions[latest]) {
  stream.push({
    name           : data.versions[latest].name,
    description    : data.versions[latest].description,
    'dist-tags'    : { latest: latest },
...
```

#### <a name="apidoc.element.sinopia.utils.tag_version"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>tag_version (data, version, tag, config)](#apidoc.element.sinopia.utils.tag_version)
- description and source-code
```javascript
tag_version = function (data, version, tag, config) {
  if (!can_add_tag(tag, config)) return false

  switch (typeof(data['dist-tags'][tag])) {
    case 'string':
      data['dist-tags'][tag] = [ data['dist-tags'][tag] ]
      break
    case 'object': // array
      break
    default:
      data['dist-tags'][tag] = []
  }
  if (data['dist-tags'][tag].indexOf(version) === -1) {
    data['dist-tags'][tag].push(version)
    data['dist-tags'][tag] = module.exports.semver_sort(data['dist-tags'][tag])
    return data['dist-tags'][tag][data['dist-tags'][tag].length - 1] === version
  }
  return false
}
```
- example usage
```shell
...
      }

      data._attachments[tarball].version = version
    }
  }

  data.versions[version] = metadata
  Utils.tag_version(data, version, tag, self.config)
  self.config.localList.add(name)
  cb()
}, callback)
}

Storage.prototype.merge_tags = function(name, tags, callback) {
var self = this
...
```

#### <a name="apidoc.element.sinopia.utils.validate_metadata"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_metadata (object, name)](#apidoc.element.sinopia.utils.validate_metadata)
- description and source-code
```javascript
validate_metadata = function (object, name) {
  assert(module.exports.is_object(object), 'not a json object')
  assert.equal(object.name, name)

  if (!module.exports.is_object(object['dist-tags'])) {
    object['dist-tags'] = {}
  }

  if (!module.exports.is_object(object['versions'])) {
    object['versions'] = {}
  }

  return object
}
```
- example usage
```shell
...

if (Object.keys(req.body).length == 1 && Utils.is_object(req.body.users)) {
  // 501 status is more meaningful, but npm doesn't show error message for 5xx
  return next( Error[404]('npm star|unstar calls are not implemented') )
}

try {
  var metadata = Utils.validate_metadata(req.body, name)
} catch(err) {
  return next( Error[422]('bad incoming package data') )
}

if (req.params._rev) {
  storage.change_package(name, metadata, req.params.revision, function(err) {
    after_change(err, 'package changed')
...
```

#### <a name="apidoc.element.sinopia.utils.validate_name"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_name (name)](#apidoc.element.sinopia.utils.validate_name)
- description and source-code
```javascript
validate_name = function (name) {
  if (typeof(name) !== 'string') return false
  name = name.toLowerCase()

  // all URL-safe characters and "@" for issue #75
  if (!name.match(/^[-a-zA-Z0-9_.!~*'()@]+$/)
   || name.charAt(0) === '.' // ".bin", etc.
   || name.charAt(0) === '-' // "-" is reserved by couchdb
   || name === 'node_modules'
   || name === '__proto__'
   || name === 'package.json'
   || name === 'favicon.ico'
  ) {
    return false
  } else {
    return true
  }
}
```
- example usage
```shell
...
}, function(err) {
  if (err) return callback(err)
  callback()
})
}

Storage.prototype.remove_tarball = function(name, filename, revision, callback) {
assert(Utils.validate_name(filename))
var self = this

self.update_package(name, function updater(data, cb) {
  if (data._attachments[filename]) {
    delete data._attachments[filename]
    cb()
  } else {
...
```

#### <a name="apidoc.element.sinopia.utils.validate_package"></a>[function <span class="apidocSignatureSpan">sinopia.utils.</span>validate_package (name)](#apidoc.element.sinopia.utils.validate_package)
- description and source-code
```javascript
validate_package = function (name) {
  name = name.split('/', 2)
  if (name.length === 1) {
    // normal package
    return module.exports.validate_name(name[0])
  } else {
    // scoped package
    return name[0][0] === '@'
        && module.exports.validate_name(name[0].slice(1))
        && module.exports.validate_name(name[1])
  }
}
```
- example usage
```shell
...
  }
}

module.exports.validate_package = function validate_package(req, res, next, value, name) {
  if (value.charAt(0) === '-') {
    // special case in couchdb usually
    next('route')
  } else if (utils.validate_package(value)) {
    next()
  } else {
    next( Error[403]('invalid ' + name) )
  }
}

module.exports.media = function media(expect) {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
