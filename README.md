# api documentation for  [grunt-githooks (v0.6.0)](https://github.com/wecodemore/grunt-githooks)  [![npm package](https://img.shields.io/npm/v/npmdoc-grunt-githooks.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-grunt-githooks) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-grunt-githooks.svg)](https://travis-ci.org/npmdoc/node-npmdoc-grunt-githooks)
#### A Grunt plugin to help bind Grunt tasks to Git hooks

[![NPM](https://nodei.co/npm/grunt-githooks.png?downloads=true)](https://www.npmjs.com/package/grunt-githooks)

[![apidoc](https://npmdoc.github.io/node-npmdoc-grunt-githooks/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-grunt-githooks_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-grunt-githooks/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-grunt-githooks/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-grunt-githooks/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Romaric Pascal",
        "url": "http://rhumaric.com"
    },
    "bugs": {
        "url": "https://github.com/wecodemore/grunt-githooks/issues"
    },
    "contributors": [
        {
            "name": "Franz Josef Kaiser",
            "email": "wecodemore@gmail.com",
            "url": "http://unserkaiser.com"
        },
        {
            "name": "Romaric Pascal",
            "url": "http://rhumaric.com"
        },
        {
            "name": "Contributors on GitHub",
            "url": "https://github.com/wecodemore/grunt-githooks/graphs/contributors"
        }
    ],
    "dependencies": {
        "handlebars": "~1.0.12"
    },
    "description": "A Grunt plugin to help bind Grunt tasks to Git hooks",
    "devDependencies": {
        "grunt": "~0.4.1",
        "grunt-contrib-clean": "~0.4.0",
        "grunt-contrib-copy": "~0.4.1",
        "grunt-contrib-jshint": "~0.6.0",
        "grunt-contrib-nodeunit": "~0.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "10c6a40c537c1b6c65648c6b7edf0018a00fc3f0",
        "tarball": "https://registry.npmjs.org/grunt-githooks/-/grunt-githooks-0.6.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "f03120ac0019f058f0b8c01cc3231f888b97106c",
    "homepage": "https://github.com/wecodemore/grunt-githooks",
    "keywords": [
        "gruntplugin",
        "git",
        "hook"
    ],
    "license": "MIT",
    "main": "Gruntfile.js",
    "maintainers": [
        {
            "name": "rhumaric",
            "email": "romaric.pascal@gmail.com"
        },
        {
            "name": "wecodemore",
            "email": "wecodemore@gmail.com"
        }
    ],
    "name": "grunt-githooks",
    "optionalDependencies": {},
    "peerDependencies": {
        "grunt": ">=0.4.1"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/wecodemore/grunt-githooks.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.6.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module grunt-githooks](#apidoc.module.grunt-githooks)
1.  object <span class="apidocSignatureSpan">grunt-githooks.</span>githooks

#### [module grunt-githooks.githooks](#apidoc.module.grunt-githooks.githooks)
1.  [function <span class="apidocSignatureSpan">grunt-githooks.githooks.</span>Hook (hookName, taskNames, options)](#apidoc.element.grunt-githooks.githooks.Hook)



# <a name="apidoc.module.grunt-githooks"></a>[module grunt-githooks](#apidoc.module.grunt-githooks)



# <a name="apidoc.module.grunt-githooks.githooks"></a>[module grunt-githooks.githooks](#apidoc.module.grunt-githooks.githooks)

#### <a name="apidoc.element.grunt-githooks.githooks.Hook"></a>[function <span class="apidocSignatureSpan">grunt-githooks.githooks.</span>Hook (hookName, taskNames, options)](#apidoc.element.grunt-githooks.githooks.Hook)
- description and source-code
```javascript
function Hook(hookName, taskNames, options) {

<span class="apidocCodeCommentSpan">  /**
   * The name of the hook
   * @property hookName
   * @type {String}
   */
</span>  this.hookName = hookName;

  /**
   * The name of the tasks that should be run by the hook, space separated
   * @property taskNames
   * @type {String}
   */
  this.taskNames = taskNames;

  /**
   * Options for the creation of the hook
   * @property options
   * @type {Object}
   */
  this.options = options || {};

  this.markerRegExp = new RegExp(this.options.startMarker.replace(/\//g, '\\/') +
                      '[\\s\\S]*' + // Not .* because it needs to match \n
                      this.options.endMarker.replace(/\//g, '\\/'), 'm');
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
