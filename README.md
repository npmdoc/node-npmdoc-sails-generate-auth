# api documentation for  [sails-generate-auth (v0.3.1)](https://github.com/kasperisager/sails-generate-auth)  [![npm package](https://img.shields.io/npm/v/npmdoc-sails-generate-auth.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sails-generate-auth) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sails-generate-auth.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sails-generate-auth)
#### Generate a Passport.js authentication layer for your Sails app that will Rock Your Socks™.

[![NPM](https://nodei.co/npm/sails-generate-auth.png?downloads=true)](https://www.npmjs.com/package/sails-generate-auth)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sails-generate-auth/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sails-generate-auth_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sails-generate-auth/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sails-generate-auth/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sails-generate-auth/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Kasper Isager",
        "email": "kasperisager@gmail.com"
    },
    "bugs": {
        "url": "http://github.com/kasperisager/sails-generate-auth/issues",
        "email": "kasperisager@gmail.com"
    },
    "dependencies": {
        "lodash": ">=2.4.x",
        "merge-defaults": ">=0.1.0"
    },
    "deprecated": "No longer maintained",
    "description": "Generate a Passport.js authentication layer for your Sails app that will Rock Your Socks™.",
    "devDependencies": {
        "fs-extra": "*",
        "reportback": "*",
        "sails-generate": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "acc12ef8a1308cf689ffb555fcda65c93e9767d9",
        "tarball": "https://registry.npmjs.org/sails-generate-auth/-/sails-generate-auth-0.3.1.tgz"
    },
    "gitHead": "d3d181f66ca694a5462a2168ac4f41f18fc0c6aa",
    "homepage": "https://github.com/kasperisager/sails-generate-auth",
    "keywords": [
        "auth",
        "generator",
        "sails",
        "generate",
        "plugin",
        "passport"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "kasperisager",
            "email": "kasperisager@gmail.com"
        }
    ],
    "name": "sails-generate-auth",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/kasperisager/sails-generate-auth.git"
    },
    "sailsGenerator": {
        "type": "auth",
        "behavior": "overrides 'sails generate auth'",
        "sailsVersion": "0.10.x"
    },
    "scripts": {},
    "version": "0.3.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sails-generate-auth](#apidoc.module.sails-generate-auth)
1.  [function <span class="apidocSignatureSpan">sails-generate-auth.</span>before (scope, cb)](#apidoc.element.sails-generate-auth.before)
1.  object <span class="apidocSignatureSpan">sails-generate-auth.</span>targets
1.  string <span class="apidocSignatureSpan">sails-generate-auth.</span>templatesDirectory



# <a name="apidoc.module.sails-generate-auth"></a>[module sails-generate-auth](#apidoc.module.sails-generate-auth)

#### <a name="apidoc.element.sails-generate-auth.before"></a>[function <span class="apidocSignatureSpan">sails-generate-auth.</span>before (scope, cb)](#apidoc.element.sails-generate-auth.before)
- description and source-code
```javascript
before = function (scope, cb) {

  //
  // scope.args are the raw command line arguments.
  //
  // e.g. if you run:
  // sails generate controlller user find create update
  // then:
  // scope.args = ['user', 'find', 'create', 'update']
  //

  _.defaults(scope, {
    // foo: scope.args[0]
  });



  //
  // Validate custom scope variables which
  // are required by this generator.
  //

  if ( !scope.rootPath ) {
    return cb(new Error(
      'Missing scope variable: 'rootPath'\n' +
      'Please make sure it is specified and try again.'
    ));
  }


  //
  // Determine default values based on the
  // available scope.
  //

  _.defaults(scope, {
    currentTime: new Date()
  });



  //
  // Take multiple "passes" if necessary.
  //

  _.defaults(scope, {
    rootPath: scope.rootPath
  });



  //
  // Trigger callback with no error to proceed.
  //

  cb();
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
