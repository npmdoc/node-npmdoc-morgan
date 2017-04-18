# npmdoc-morgan

#### api documentation for  [morgan (v1.8.1)](https://github.com/expressjs/morgan#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-morgan.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-morgan) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-morgan.svg)](https://travis-ci.org/npmdoc/node-npmdoc-morgan)

#### HTTP request logger middleware for node.js

[![NPM](https://nodei.co/npm/morgan.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/morgan)

- [https://npmdoc.github.io/node-npmdoc-morgan/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-morgan/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-morgan/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-morgan/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-morgan/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-morgan/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/expressjs/morgan/issues"
    },
    "contributors": [
        {
            "name": "Douglas Christopher Wilson"
        },
        {
            "name": "Jonathan Ong",
            "url": "http://jongleberry.com"
        }
    ],
    "dependencies": {
        "basic-auth": "~1.1.0",
        "debug": "2.6.1",
        "depd": "~1.1.0",
        "on-finished": "~2.3.0",
        "on-headers": "~1.0.1"
    },
    "description": "HTTP request logger middleware for node.js",
    "devDependencies": {
        "eslint": "3.15.0",
        "eslint-config-standard": "6.2.1",
        "eslint-plugin-markdown": "1.0.0-beta.3",
        "eslint-plugin-promise": "3.4.0",
        "eslint-plugin-standard": "2.0.1",
        "istanbul": "0.4.5",
        "mocha": "2.5.3",
        "split": "1.0.0",
        "supertest": "1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f93023d3887bd27b78dfd6023cea7892ee27a4b1",
        "tarball": "https://registry.npmjs.org/morgan/-/morgan-1.8.1.tgz"
    },
    "engines": {
        "node": ">= 0.8.0"
    },
    "files": [
        "LICENSE",
        "HISTORY.md",
        "README.md",
        "index.js"
    ],
    "gitHead": "29daba369e388522656183463fae1fb1a1dda609",
    "homepage": "https://github.com/expressjs/morgan#readme",
    "keywords": [
        "express",
        "http",
        "logger",
        "middleware"
    ],
    "license": "MIT",
    "maintainers": [
        {
            "name": "dougwilson"
        }
    ],
    "name": "morgan",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/expressjs/morgan.git"
    },
    "scripts": {
        "lint": "eslint --plugin markdown --ext js,md .",
        "test": "mocha --check-leaks --reporter spec --bail",
        "test-cov": "istanbul cover node_modules/mocha/bin/_mocha -- --check-leaks --reporter dot",
        "test-travis": "istanbul cover node_modules/mocha/bin/_mocha --report lcovonly -- --check-leaks --reporter spec"
    },
    "version": "1.8.1"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
