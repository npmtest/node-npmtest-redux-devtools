# npmtest-redux-devtools

#### basic test coverage for  [redux-devtools (v3.3.2)](https://github.com/gaearon/redux-devtools)  [![npm package](https://img.shields.io/npm/v/npmtest-redux-devtools.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-redux-devtools) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-redux-devtools.svg)](https://travis-ci.org/npmtest/node-npmtest-redux-devtools)

#### Redux DevTools with hot reloading and time travel

[![NPM](https://nodei.co/npm/redux-devtools.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/redux-devtools)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-redux-devtools/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-devtools/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-redux-devtools/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-redux-devtools/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-redux-devtools/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-redux-devtools/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-redux-devtools/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-redux-devtools/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-redux-devtools/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-redux-devtools/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-redux-devtools/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-redux-devtools/build/test-report.html](https://npmtest.github.io/node-npmtest-redux-devtools/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-redux-devtools/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-redux-devtools/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-redux-devtools/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-redux-devtools/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-redux-devtools/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-redux-devtools/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Abramov",
        "url": "http://github.com/gaearon"
    },
    "bugs": {
        "url": "https://github.com/gaearon/redux-devtools/issues"
    },
    "dependencies": {
        "lodash": "^4.2.0",
        "redux-devtools-instrument": "^1.0.1"
    },
    "description": "Redux DevTools with hot reloading and time travel",
    "devDependencies": {
        "babel-cli": "^6.3.17",
        "babel-core": "^6.3.17",
        "babel-eslint": "^4.1.6",
        "babel-loader": "^6.2.0",
        "babel-preset-es2015-loose": "^6.1.3",
        "babel-preset-react": "6.3.13",
        "babel-preset-stage-0": "^6.3.13",
        "cross-env": "3.1.3",
        "eslint": "^0.23",
        "eslint-config-airbnb": "0.0.6",
        "eslint-plugin-react": "^2.3.0",
        "expect": "^1.6.0",
        "isparta": "^3.0.3",
        "jsdom": "^6.5.1",
        "mocha": "^2.2.5",
        "mocha-jsdom": "^1.0.0",
        "react": "^0.14.0",
        "react-addons-test-utils": "^0.14.0",
        "react-dom": "^0.14.0",
        "react-redux": "^4.0.0",
        "redux": "^3.5.2",
        "rimraf": "^2.3.4",
        "webpack": "^1.11.0"
    },
    "directories": {},
    "dist": {
        "shasum": "f427f71964e2b3785b68834b6e4fe99d8da75b5e",
        "tarball": "https://registry.npmjs.org/redux-devtools/-/redux-devtools-3.3.2.tgz"
    },
    "files": [
        "lib",
        "src"
    ],
    "gitHead": "defc8100e1cc8e27b6f87e4e34a5eef5613ff4ec",
    "homepage": "https://github.com/gaearon/redux-devtools",
    "keywords": [
        "redux",
        "devtools",
        "flux",
        "hot reloading",
        "time travel",
        "live edit"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "gaearon"
        },
        {
            "name": "zalmoxisus"
        }
    ],
    "name": "redux-devtools",
    "optionalDependencies": {},
    "peerDependencies": {
        "react": "^0.14.0 || ^15.0.0",
        "react-redux": "^4.0.0 || ^5.0.0",
        "redux": "^3.5.2"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/gaearon/redux-devtools.git"
    },
    "scripts": {
        "build": "babel src --out-dir lib",
        "clean": "rimraf lib",
        "lint": "eslint src test examples",
        "prepublish": "npm run lint && npm run test && npm run clean && npm run build",
        "test": "cross-env NODE_ENV=test mocha --compilers js:babel-core/register --recursive",
        "test:cov": "babel-node ./node_modules/.bin/isparta cover ./node_modules/.bin/_mocha -- --recursive",
        "test:watch": "cross-env NODE_ENV=test mocha --compilers js:babel-core/register --recursive --watch"
    },
    "version": "3.3.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
