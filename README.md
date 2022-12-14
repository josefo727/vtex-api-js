<div align="center">
<h1>VTEX API</h1>

[![NPM][npm-badge]][npm]
[![Build Status][build-badge]][build]
[![Codecov][codecov-badge]][codecov]
[![Bundle Size][bundle-size-badge]][bundle-size]
[![David][deps-badge]][deps]
[![Known Vulnerabilities][snyk-badge]][snyk]
[![CodeFactor][codefactor-badge]][codefactor]
[![Total alerts][lgtm-badge]][lgtm]
[![MIT License][license-badge]][license]

<p>An isomorphic and depency free collection of VTEX APIs methods</p>
<hr />
</div>

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [API](#api)

## Install

```bash
# Yarn
yarn add vtex-api

# NPM
npm install --save vtex-api
```

## Usage

### Imports

You can import each method individually

```js
import searchDocument from 'vtex-api/lib/searchDocument';
```

or use ES6 named import (tree shaking recommended)

```js
import { searchDocument } from 'vtex-api';
```

### Old Browsers support

If you need coverage old browsers, you need use an `fetch` polyfill, like [whatwg-fetch](https://www.npmjs.com/package/whatwg-fetch) or [unfetch](https://www.npmjs.com/package/unfetch).

### Node
For [NodeJS][node] usage, you will need some Isomorphic Fetch lib, like [isomorphic-fetch](https://www.npmjs.com/package/isomorphic-fetch) (and [isomorphic-form-data](https://www.npmjs.com/package/isomorphic-form-data) if you will use `uploadFile()` method)

For **authentication**, each method has keys for this purpose:

```js
const response = await searchDocument({
  ...
  auth: { appKey: '123', appToken: 'abc' }, // Your private keys (use it ONLY on backend)
  accountName: 'storename', // Account name (will build full URL request)
})
```

## API

### Masterdata

Name | Description | Docs
:--- | :--- | :---
`searchDocument()` | Query a collection of documents | [📝](./docs/searchDocument.md)

### Product

### Helpers

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

<!-- GIT Variables -->
[node]: https://nodejs.org

[npm]: https://www.npmjs.com/package/vtex-api
[npm-badge]: https://img.shields.io/npm/v/vtex-api.svg

[build]: https://travis-ci.org/zeindelf/vtex-api
[build-badge]: https://img.shields.io/travis/zeindelf/vtex-api.svg?style=flat-square

[codecov]: https://codecov.io/gh/Zeindelf/vtex-api
[codecov-badge]: https://codecov.io/gh/Zeindelf/vtex-api/branch/master/graph/badge.svg

[bundle-size]: https://bundlephobia.com/result?p=vtex-api
[bundle-size-badge]: https://badgen.net/bundlephobia/minzip/vtex-api

[deps]: https://github.com/Zeindelf/vtex-api
[deps-badge]: https://david-dm.org/zeindelf/vtex-api.svg

[snyk]: https://snyk.io/test/npm/vtex-api
[snyk-badge]: https://snyk.io/test/npm/vtex-api/badge.svg

[codefactor]: https://www.codefactor.io/repository/github/zeindelf/vtex-api
[codefactor-badge]: https://www.codefactor.io/repository/github/zeindelf/vtex-api/badge

[lgtm]: https://lgtm.com/projects/g/Zeindelf/vtex-api/alerts/
[lgtm-badge]: https://img.shields.io/lgtm/alerts/g/Zeindelf/vtex-api.svg?logo=lgtm&logoWidth=18

[license]: https://github.com/zeindelf/vtex-api/blob/master/LICENSE
[license-badge]: https://img.shields.io/npm/l/vtex-api.svg?style=flat-square