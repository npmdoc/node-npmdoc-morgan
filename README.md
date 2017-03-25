# api documentation for  [morgan (v1.8.1)](https://github.com/expressjs/morgan#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-morgan.svg)](https://travis-ci.org/npmdoc/node-npmdoc-morgan)
#### HTTP request logger middleware for node.js

[![NPM](https://nodei.co/npm/morgan.png?downloads=true)](https://www.npmjs.com/package/morgan)

[![apidoc](https://npmdoc.github.io/node-npmdoc-morgan/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-morgan_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-morgan/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-morgan/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/expressjs/morgan/issues"
    },
    "contributors": [
        {
            "name": "Douglas Christopher Wilson",
            "email": "doug@somethingdoug.com"
        },
        {
            "name": "Jonathan Ong",
            "email": "me@jongleberry.com",
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
            "name": "dougwilson",
            "email": "doug@somethingdoug.com"
        }
    ],
    "name": "morgan",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module morgan](#apidoc.module.morgan)
1.  [function <span class="apidocSignatureSpan">morgan.</span>compile (format)](#apidoc.element.morgan.compile)
1.  [function <span class="apidocSignatureSpan">morgan.</span>date (req, res, format)](#apidoc.element.morgan.date)
1.  [function <span class="apidocSignatureSpan">morgan.</span>dev (tokens, req, res)](#apidoc.element.morgan.dev)
1.  [function <span class="apidocSignatureSpan">morgan.</span>format (name, fmt)](#apidoc.element.morgan.format)
1.  [function <span class="apidocSignatureSpan">morgan.</span>http-version (req)](#apidoc.element.morgan.http-version)
1.  [function <span class="apidocSignatureSpan">morgan.</span>method (req)](#apidoc.element.morgan.method)
1.  [function <span class="apidocSignatureSpan">morgan.</span>referrer (req)](#apidoc.element.morgan.referrer)
1.  [function <span class="apidocSignatureSpan">morgan.</span>remote-addr (req)](#apidoc.element.morgan.remote-addr)
1.  [function <span class="apidocSignatureSpan">morgan.</span>remote-user (req)](#apidoc.element.morgan.remote-user)
1.  [function <span class="apidocSignatureSpan">morgan.</span>req (req, res, field)](#apidoc.element.morgan.req)
1.  [function <span class="apidocSignatureSpan">morgan.</span>res (req, res, field)](#apidoc.element.morgan.res)
1.  [function <span class="apidocSignatureSpan">morgan.</span>response-time (req, res, digits)](#apidoc.element.morgan.response-time)
1.  [function <span class="apidocSignatureSpan">morgan.</span>status (req, res)](#apidoc.element.morgan.status)
1.  [function <span class="apidocSignatureSpan">morgan.</span>token (name, fn)](#apidoc.element.morgan.token)
1.  [function <span class="apidocSignatureSpan">morgan.</span>url (req)](#apidoc.element.morgan.url)
1.  [function <span class="apidocSignatureSpan">morgan.</span>user-agent (req)](#apidoc.element.morgan.user-agent)
1.  string <span class="apidocSignatureSpan">morgan.</span>combined
1.  string <span class="apidocSignatureSpan">morgan.</span>common
1.  string <span class="apidocSignatureSpan">morgan.</span>default
1.  string <span class="apidocSignatureSpan">morgan.</span>short
1.  string <span class="apidocSignatureSpan">morgan.</span>tiny



# <a name="apidoc.module.morgan"></a>[module morgan](#apidoc.module.morgan)

#### <a name="apidoc.element.morgan.compile"></a>[function <span class="apidocSignatureSpan">morgan.</span>compile (format)](#apidoc.element.morgan.compile)
- description and source-code
```javascript
function compile(format) {
  if (typeof format !== 'string') {
    throw new TypeError('argument format must be a string')
  }

  var fmt = format.replace(/"/g, '\\"')
  var js = '  "use strict"\n  return "' + fmt.replace(/:([-\w]{2,})(?:\[([^\]]+)\])?/g, function (_, name, arg) {
    var tokenArguments = 'req, res'
    var tokenFunction = 'tokens[' + String(JSON.stringify(name)) + ']'

    if (arg !== undefined) {
      tokenArguments += ', ' + String(JSON.stringify(arg))
    }

    return '" +\n    (' + tokenFunction + '(' + tokenArguments + ') || "-") + "'
  }) + '"'

  // eslint-disable-next-line no-new-func
  return new Function('tokens, req, res', js)
}
```
- example usage
```shell
...

The URL of the request. This will use 'req.originalUrl' if exists, otherwise 'req.url'.

##### :user-agent

The contents of the User-Agent header of the request.

### morgan.compile(format)

Compile a format string into a 'format' function for use by 'morgan'. A format string
is a string that represents a single log line and can utilize token syntax.
Tokens are references by ':token-name'. If tokens accept arguments, they can
be passed using '[]', for example: ':token-name[pretty]' would pass the string
''pretty'' as an argument to the token 'token-name'.
...
```

#### <a name="apidoc.element.morgan.date"></a>[function <span class="apidocSignatureSpan">morgan.</span>date (req, res, format)](#apidoc.element.morgan.date)
- description and source-code
```javascript
function getDateToken(req, res, format) {
  var date = new Date()

  switch (format || 'web') {
    case 'clf':
      return clfdate(date)
    case 'iso':
      return date.toISOString()
    case 'web':
      return date.toUTCString()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.dev"></a>[function <span class="apidocSignatureSpan">morgan.</span>dev (tokens, req, res)](#apidoc.element.morgan.dev)
- description and source-code
```javascript
function developmentFormatLine(tokens, req, res) {
  // get the status code if response written
  var status = res._header
    ? res.statusCode
    : undefined

  // get status color
  var color = status >= 500 ? 31 // red
    : status >= 400 ? 33 // yellow
    : status >= 300 ? 36 // cyan
    : status >= 200 ? 32 // green
    : 0 // no color

  // get colored function
  var fn = developmentFormatLine[color]

  if (!fn) {
    // compile
    fn = developmentFormatLine[color] = compile('\x1b[0m:method :url \x1b[' +
      color + 'm:status \x1b[0m:response-time ms - :res[content-length]\x1b[0m')
  }

  return fn(tokens, req, res)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.format"></a>[function <span class="apidocSignatureSpan">morgan.</span>format (name, fmt)](#apidoc.element.morgan.format)
- description and source-code
```javascript
function format(name, fmt) {
  morgan[name] = fmt
  return this
}
```
- example usage
```shell
...
''pretty'' as an argument to the token 'token-name'.

The function returned from 'morgan.compile' takes three arguments 'tokens', 'req', and
'res', where 'tokens' is object with all defined tokens, 'req' is the HTTP request and
'res' is the HTTP response. The function will return a string that will be the log line,
or 'undefined' / 'null' to skip logging.

Normally formats are defined using 'morgan.format(name, format)', but for certain
advanced uses, this compile function is directly available.

## Examples

### express/connect

Simple app that will log all request in the Apache combined format to STDOUT
...
```

#### <a name="apidoc.element.morgan.http-version"></a>[function <span class="apidocSignatureSpan">morgan.</span>http-version (req)](#apidoc.element.morgan.http-version)
- description and source-code
```javascript
function getHttpVersionToken(req) {
  return req.httpVersionMajor + '.' + req.httpVersionMinor
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.method"></a>[function <span class="apidocSignatureSpan">morgan.</span>method (req)](#apidoc.element.morgan.method)
- description and source-code
```javascript
function getMethodToken(req) {
  return req.method
}
```
- example usage
```shell
...
#### Using a custom format function

<!-- eslint-disable no-undef -->

''' js
morgan(function (tokens, req, res) {
  return [
    tokens.method(req, res),
    tokens.url(req, res),
    tokens.status(req, res),
    tokens.res(req, res, 'content-length'), '-',
    tokens['response-time'](req, res), 'ms'
  ].join(' ')
})
'''
...
```

#### <a name="apidoc.element.morgan.referrer"></a>[function <span class="apidocSignatureSpan">morgan.</span>referrer (req)](#apidoc.element.morgan.referrer)
- description and source-code
```javascript
function getReferrerToken(req) {
  return req.headers['referer'] || req.headers['referrer']
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.remote-addr"></a>[function <span class="apidocSignatureSpan">morgan.</span>remote-addr (req)](#apidoc.element.morgan.remote-addr)
- description and source-code
```javascript
function getip(req) {
  return req.ip ||
    req._remoteAddress ||
    (req.connection && req.connection.remoteAddress) ||
    undefined
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.remote-user"></a>[function <span class="apidocSignatureSpan">morgan.</span>remote-user (req)](#apidoc.element.morgan.remote-user)
- description and source-code
```javascript
function getRemoteUserToken(req) {
  // parse basic credentials
  var credentials = auth(req)

  // return username
  return credentials
    ? credentials.name
    : undefined
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.req"></a>[function <span class="apidocSignatureSpan">morgan.</span>req (req, res, field)](#apidoc.element.morgan.req)
- description and source-code
```javascript
function getRequestToken(req, res, field) {
  // get header
  var header = req.headers[field.toLowerCase()]

  return Array.isArray(header)
    ? header.join(', ')
    : header
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.res"></a>[function <span class="apidocSignatureSpan">morgan.</span>res (req, res, field)](#apidoc.element.morgan.res)
- description and source-code
```javascript
function getResponseHeader(req, res, field) {
  if (!res._header) {
    return undefined
  }

  // get header
  var header = res.getHeader(field)

  return Array.isArray(header)
    ? header.join(', ')
    : header
}
```
- example usage
```shell
...

''' js
morgan(function (tokens, req, res) {
  return [
    tokens.method(req, res),
    tokens.url(req, res),
    tokens.status(req, res),
    tokens.res(req, res, 'content-length'), '-',
    tokens['response-time'](req, res), 'ms'
  ].join(' ')
})
'''

#### Options
...
```

#### <a name="apidoc.element.morgan.response-time"></a>[function <span class="apidocSignatureSpan">morgan.</span>response-time (req, res, digits)](#apidoc.element.morgan.response-time)
- description and source-code
```javascript
function getResponseTimeToken(req, res, digits) {
  if (!req._startAt || !res._startAt) {
    // missing request and/or response start time
    return
  }

  // calculate diff
  var ms = (res._startAt[0] - req._startAt[0]) * 1e3 +
    (res._startAt[1] - req._startAt[1]) * 1e-6

  // return truncated value
  return ms.toFixed(digits === undefined ? 3 : digits)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.morgan.status"></a>[function <span class="apidocSignatureSpan">morgan.</span>status (req, res)](#apidoc.element.morgan.status)
- description and source-code
```javascript
function getStatusToken(req, res) {
  return res._header
    ? String(res.statusCode)
    : undefined
}
```
- example usage
```shell
...
<!-- eslint-disable no-undef -->

''' js
morgan(function (tokens, req, res) {
  return [
    tokens.method(req, res),
    tokens.url(req, res),
    tokens.status(req, res),
    tokens.res(req, res, 'content-length'), '-',
    tokens['response-time'](req, res), 'ms'
  ].join(' ')
})
'''

#### Options
...
```

#### <a name="apidoc.element.morgan.token"></a>[function <span class="apidocSignatureSpan">morgan.</span>token (name, fn)](#apidoc.element.morgan.token)
- description and source-code
```javascript
function token(name, fn) {
  morgan[name] = fn
  return this
}
```
- example usage
```shell
...
:method :url :status :res[content-length] - :response-time ms
'''

#### Tokens

##### Creating new tokens

To define a token, simply invoke 'morgan.token()' with the name and a callback function.
This callback function is expected to return a string value. The value returned is then
available as ":type" in this case:

<!-- eslint-disable no-undef -->

'''js
morgan.token('type', function (req, res) { return req.headers['content-type'] })
...
```

#### <a name="apidoc.element.morgan.url"></a>[function <span class="apidocSignatureSpan">morgan.</span>url (req)](#apidoc.element.morgan.url)
- description and source-code
```javascript
function getUrlToken(req) {
  return req.originalUrl || req.url
}
```
- example usage
```shell
...

<!-- eslint-disable no-undef -->

''' js
morgan(function (tokens, req, res) {
  return [
    tokens.method(req, res),
    tokens.url(req, res),
    tokens.status(req, res),
    tokens.res(req, res, 'content-length'), '-',
    tokens['response-time'](req, res), 'ms'
  ].join(' ')
})
'''
...
```

#### <a name="apidoc.element.morgan.user-agent"></a>[function <span class="apidocSignatureSpan">morgan.</span>user-agent (req)](#apidoc.element.morgan.user-agent)
- description and source-code
```javascript
function getUserAgentToken(req) {
  return req.headers['user-agent']
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
