# npmtest-angular2-data-table

#### basic test coverage for  [angular2-data-table (v3.0.0)](https://github.com/swimlane/angular2-data-table#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-angular2-data-table.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-angular2-data-table) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-angular2-data-table.svg)](https://travis-ci.org/npmtest/node-npmtest-angular2-data-table)

#### angular2-data-table is a Angular2 component for presenting large and complex data.

[![NPM](https://nodei.co/npm/angular2-data-table.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/angular2-data-table)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-angular2-data-table/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-angular2-data-table/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-angular2-data-table/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-angular2-data-table/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-angular2-data-table/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-angular2-data-table/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-angular2-data-table/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-angular2-data-table/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-angular2-data-table/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-angular2-data-table/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-angular2-data-table/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-angular2-data-table/build/test-report.html](https://npmtest.github.io/node-npmtest-angular2-data-table/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-angular2-data-table/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-angular2-data-table/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-angular2-data-table/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-angular2-data-table/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-angular2-data-table/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-angular2-data-table/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-angular2-data-table/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-angular2-data-table/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "angular2-data-table",
    "version": "3.0.0",
    "description": "angular2-data-table is a Angular2 component for presenting large and complex data.",
    "main": "release/index.js",
    "typings": "release/index.d.ts",
    "scripts": {
        "check": "npm-check --skip-unused",
        "test": "karma start",
        "watch:test": "npm run test -- --auto-watch --no-single-run",
        "lint": "tslint ./src/**/*.ts ./test/**/*.ts",
        "version": "npm run release",
        "preversion": "npm test",
        "postversion": "git push && git push --tags",
        "clean": "npm-run-all -p clean:*",
        "clean:dist": "rimraf dist",
        "clean:release": "rimraf release",
        "build": "webpack --display-error-details",
        "build:release": "cross-env NODE_ENV=production npm run build",
        "build:package": "cross-env NODE_ENV=package npm run build",
        "build:ts": "tsc",
        "build:aot": "ngc",
        "build:sass": "node-sass -o dist/ src/",
        "build:css": "postcss --use autoprefixer dist/*.css -d dist/",
        "watch": "webpack --display-error-details --watch",
        "start": "webpack-dev-server",
        "start:hmr": "webpack-dev-server --env.HMR",
        "release": "npm-run-all build:release",
        "package": "npm-run-all -s clean:release package:css package:aot build:package package:replace package:minify",
        "package:ts": "tsc --outDir release",
        "package:aot": "ngc -p tsconfig-aot.json",
        "package:replace": "node ./config/replace.js",
        "package:css": "node-sass -o release/ src/themes && node-sass -o release/ src/components",
        "package:minify": "uglifyjs release/index.js --source-map release/index.min.js.map --source-map-url release/index.js.map --compress --mangle --screw-ie8 --output release/index.min.js",
        "deploy": "node ./config/deploy.js"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/swimlane/angular2-data-table.git"
    },
    "keywords": [
        "angularjs",
        "angular",
        "javascript",
        "angular2",
        "datatable",
        "grid",
        "table"
    ],
    "author": "",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/swimlane/angular2-data-table/issues"
    },
    "homepage": "https://github.com/swimlane/angular2-data-table#readme",
    "peerDependencies": {
        "@angular/common": "^2.3.1",
        "@angular/compiler": "^2.3.1",
        "@angular/core": "^2.3.1",
        "@angular/platform-browser": "^2.3.1",
        "@angular/platform-browser-dynamic": "^2.3.1",
        "zone.js": "^0.7.2",
        "rxjs": "^5.0.1",
        "core-js": "^2.4.0"
    },
    "devDependencies": {
        "@angular/common": "~2.3.1",
        "@angular/compiler": "~2.3.1",
        "@angular/compiler-cli": "^2.3.1",
        "@angular/core": "~2.3.1",
        "@angular/platform-browser": "~2.3.1",
        "@angular/platform-browser-dynamic": "~2.3.1",
        "@angular/platform-server": "~2.3.1",
        "@angularclass/hmr": "^1.2.2",
        "@angularclass/hmr-loader": "^3.0.2",
        "@types/jasmine": "^2.5.37",
        "@types/node": "^6.0.52",
        "autoprefixer": "^6.5.4",
        "awesome-typescript-loader": "~3.0.0-beta.10",
        "chalk": "^1.1.3",
        "clean-webpack-plugin": "^0.1.10",
        "copy-webpack-plugin": "^4.0.0",
        "core-js": "^2.4.0",
        "cross-env": "^3.1.3",
        "css-loader": "^0.26.1",
        "extract-text-webpack-plugin": "^2.0.0-beta.4",
        "fs-extra": "^1.0.0",
        "gh-pages": "^0.12.0",
        "html-webpack-plugin": "^2.22.0",
        "istanbul-instrumenter-loader": "^1.1.0",
        "jasmine-core": "^2.5.2",
        "karma": "^1.3.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-coverage": "^1.1.1",
        "karma-jasmine": "^1.0.2",
        "karma-mocha-reporter": "^2.0.0",
        "karma-remap-coverage": "^0.1.3",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-webpack": "^1.8.0",
        "node-sass": "^4.0.0",
        "npm-run-all": "^3.1.0",
        "postcss": "^5.1.1",
        "postcss-loader": "^1.2.1",
        "progress-bar-webpack-plugin": "^1.9.0",
        "replace": "^0.3.0",
        "rimraf": "^2.5.2",
        "rxjs": "^5.0.1",
        "sass-loader": "^4.1.0",
        "source-map-loader": "^0.1.5",
        "style-loader": "0.13.1",
        "ts-helpers": "^1.1.2",
        "tslint": "^4.0.2",
        "tslint-loader": "^3.3.0",
        "typescript": "~2.0.3",
        "webpack": "2.2.0-rc.0",
        "webpack-dev-server": "2.1.0-beta.12",
        "webpack-merge": "^1.1.1",
        "webpack-notifier": "^1.5.0",
        "zone.js": "^0.7.2"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
