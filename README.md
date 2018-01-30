<h1 align="center">coinmarketcap-api</h1>
<div align="center">
  <strong>CoinMarketCap API wrapper for node</strong>
</div>
<br>
<div align="center">
  <a href="https://npmjs.org/package/coinmarketcap-api">
    <img src="https://img.shields.io/npm/v/coinmarketcap-api.svg?style=flat-square" alt="npm package version" />
  </a>
  <a href="https://npmjs.org/package/coinmarketcap-api">
  <img src="https://img.shields.io/npm/dm/coinmarketcap-api.svg?style=flat-square" alt="npm downloads" />
  </a>
  <a href="https://github.com/feross/standard">
    <img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square" alt="standard JS linter" />
  </a>
<a href="https://codecov.io/gh/tiaanduplessis/coinmarketcap-api">
  <img src="https://codecov.io/gh/tiaanduplessis/coinmarketcap-api/branch/master/graph/badge.svg?style=flat-square" alt="Codecov" />
</a>
  <a href="https://github.com/prettier/prettier">
    <img src="https://img.shields.io/badge/styled_with-prettier-ff69b4.svg?style=flat-square" alt="prettier code formatting" />
  </a>
  <a href="https://travis-ci.org/tiaanduplessis/coinmarketcap-api">
    <img src="https://img.shields.io/travis/tiaanduplessis/coinmarketcap-api.svg?style=flat-square" alt="travis ci build status" />
  </a>
  <a href="https://github.com/tiaanduplessis/coinmarketcap-api/blob/master/LICENSE">
    <img src="https://img.shields.io/npm/l/coinmarketcap-api.svg?style=flat-square" alt="project license" />
  </a>
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="make a pull request" />
  </a>
</div>
<br>
<div align="center">
  <a href="https://github.com/tiaanduplessis/coinmarketcap-api/watchers">
    <img src="https://img.shields.io/github/watchers/tiaanduplessis/coinmarketcap-api.svg?style=social" alt="Github Watch Badge" />
  </a>
  <a href="https://github.com/tiaanduplessis/coinmarketcap-api/stargazers">
    <img src="https://img.shields.io/github/stars/tiaanduplessis/coinmarketcap-api.svg?style=social" alt="Github Star Badge" />
  </a>
  <a href="https://twitter.com/intent/tweet?text=Check%20out%20coinmarketcap-api!%20https://github.com/tiaanduplessis/coinmarketcap-api%20%F0%9F%91%8D">
    <img src="https://img.shields.io/twitter/url/https/github.com/tiaanduplessis/coinmarketcap-api.svg?style=social" alt="Tweet" />
  </a>
</div>
<br>
<div align="center">
  Built with ❤︎ by <a href="https://github.com/tiaanduplessis">tiaanduplessis</a> and <a href="https://github.com/tiaanduplessis/coinmarketcap-api/contributors">contributors</a>
</div>

<h2>Table of Contents</h2>
<details>
  <summary>Table of Contents</summary>
  <li><a href="#install">Install</a></li>
  <li><a href="#usage">Usage</a></li>
  <li><a href="#api">API</a></li>
  <li><a href="#contribute">Contribute</a></li>
  <li><a href="#license">License</a></li>
</details>

## Install

[![Greenkeeper badge](https://badges.greenkeeper.io/tiaanduplessis/coinmarketcap-api.svg)](https://greenkeeper.io/)

```sh
$ npm install coinmarketcap-api
# OR
$ yarn add coinmarketcap-api
```

## Usage

```js
const CoinMarketCap = require('coinmarketcap-api')

const client = new CoinMarketCap()

client.getTicker().then(console.log).catch(console.error)
client.getGlobal().then(console.log).catch(console.error)
```

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### getTicker

Get ticker information

**Parameters**

-   `options` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)?** Options for the request:
    -   `options.start` **Int?** Return results from rank start and above
    -   `options.limit` **Int?** Only returns the top limit results
    -   `options.convert` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** Return price, 24h volume, and market cap in terms of another currency
    -   `options.currency` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** Return only specific currency

**Examples**

```javascript
const client = new CoinMarketCap()
client.getTicker({limit: 3}).then(console.log).catch(console.error)
client.getTicker({limit: 1, currency: 'bitcoin'}).then(console.log).catch(console.error)
client.getTicker({convert: 'EUR'}).then(console.log).catch(console.error)
client.getTicker({start: 0, limit: 5}).then(console.log).catch(console.error)
```

### getGlobal

Get global information

**Parameters**

-   `convert`  
-   `options` **([Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) \| [String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String))?** Options for the request
    -   `options.convert` **[String](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)?** Return price, 24h volume, and market cap in terms of another currency

**Examples**

```javascript
const client = new CoinMarketCap()
client.getGlobal('GBP').then(console.log).catch(console.error)
client.getGlobal({convert: 'GBP'}).then(console.log).catch(console.error)
```

## Contributing

Contributions are welcome!

1.  Fork it.
2.  Create your feature branch: `git checkout -b my-new-feature`
3.  Commit your changes: `git commit -am 'Add some feature'`
4.  Push to the branch: `git push origin my-new-feature`
5.  Submit a pull request :D

Or open up [a issue](https://github.com/tiaanduplessis/coinmarketcap-api/issues).

## License

Licensed under the MIT License.
