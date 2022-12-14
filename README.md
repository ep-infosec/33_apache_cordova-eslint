<!--
#
# Licensed to the Apache Software Foundation (ASF) under one
# or more contributor license agreements.  See the NOTICE file
# distributed with this work for additional information
# regarding copyright ownership.  The ASF licenses this file
# to you under the Apache License, Version 2.0 (the
# "License"); you may not use this file except in compliance
# with the License.  You may obtain a copy of the License at
#
# http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
#  KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.
#
-->

# @cordova/eslint-config

[![NPM](https://nodei.co/npm/cordova-eslint.png)](https://nodei.co/npm/cordova-eslint/)

[![Node CI](https://github.com/apache/cordova-eslint/workflows/Node%20CI/badge.svg?branch=master)](https://github.com/apache/cordova-eslint/actions?query=branch%3Amaster)

This repository centralizes the ESLint configuration used for Cordova's development.

## Installation

`@cordova/eslint-config` comes with all plugins configs and even `eslint` itself. So all you need to do to get started is:

```shell
npm i -D @cordova/eslint-config
```

## Usage

```yml
# In package.json
{
  "scripts": {
    "lint": "eslint ."
  }
}
```

```yml
# In .eslintrc.yml
root: true

extends: '@cordova/eslint-config/node'

overrides:

- files: [spec/**/*.js]
  extends: '@cordova/eslint-config/node-tests'

- files: [cordova-js-src/**/*.js]
  extends: '@cordova/eslint-config/browser'
```

## Reference

This package exposes the following shareable ESLint configurations:

### `@cordova/eslint-config/node` (or simply `@cordova`)

For linting scripts intended to be run with Node.js.

### `@cordova/eslint-config/node-tests`

For linting Jasmine tests of Cordova's Node.js scripts.

### `@cordova/eslint-config/browser`

For linting cordova-style CommonJS modules intended to be run in the browser (before they are bundled).

### `@cordova/eslint-config/browser-tests`

For linting Jasmine tests of Cordova's browser code.
