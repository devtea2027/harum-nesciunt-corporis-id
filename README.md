# 🦋 @devtea2027/harum-nesciunt-corporis-id

docs.

[![example workflow](https://github.com/devtea2027/harum-nesciunt-corporis-id/actions/workflows/default.yml/badge.svg)](#) [![](https://img.shields.io/npm/v/@devtea2027/harum-nesciunt-corporis-id.svg)](https://www.npmjs.com/package/@devtea2027/harum-nesciunt-corporis-id) [![](https://img.shields.io/npm/dm/@devtea2027/harum-nesciunt-corporis-id?color=blue)](https://www.npmjs.com/package/@devtea2027/harum-nesciunt-corporis-id) [![All Contributors](https://img.shields.io/badge/all_contributors-54-darkcyan.svg?style=flat)](#contributors) [![Coverage Status](https://coveralls.io/repos/github/cdimascio/@devtea2027/harum-nesciunt-corporis-id/badge.svg?branch=master)](https://coveralls.io/github/cdimascio/@devtea2027/harum-nesciunt-corporis-id?branch=master) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/1570a06f609345ddb237114bbd6ceed7)](https://www.codacy.com/manual/cdimascio/@devtea2027/harum-nesciunt-corporis-id?utm_source=github.com&utm_medium=referral&utm_content=cdimascio/@devtea2027/harum-nesciunt-corporis-id&utm_campaign=Badge_Grade) [![](https://img.shields.io/gitter/room/cdimascio-oss/community?color=%23eb205a)](https://gitter.im/cdimascio-oss/community) [![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/devtea2027/harum-nesciunt-corporis-id) [![](https://img.shields.io/badge/documentation-yes-informational)](https://cdimascio.github.io/@devtea2027/harum-nesciunt-corporis-id-documentation/) [![](https://img.shields.io/badge/license-MIT-blue.svg)](#license)

**An OpenApi validator for ExpressJS** that automatically validates **API** _**requests**_ and _**responses**_ using an **OpenAPI 3** specification.

<p align="center">
<img src="https://raw.githubusercontent.com/cdimascio/@devtea2027/harum-nesciunt-corporis-id/master/assets/@devtea2027/harum-nesciunt-corporis-id-logo-v2.png" width="600">
</p>

[🦋@devtea2027/harum-nesciunt-corporis-id](https://github.com/devtea2027/harum-nesciunt-corporis-id) is an unopinionated library that integrates with new and existing API applications. @devtea2027/harum-nesciunt-corporis-id lets you write code the way you want; it does not impose any coding convention or project layout. Simply, install the validator onto your express app, point it to your OpenAPI 3 specification, then define and implement routes the way you prefer. See an [example](https://cdimascio.github.io/@devtea2027/harum-nesciunt-corporis-id-documentation/guide-standard/).

**Features:**

- ✔️ request validation
- ✔️ response validation (json only)
- 👮 security validation / custom security functions
- 👽 3rd party / custom formats / custom data serialization-deserialization
- 🧵 optionally auto-map OpenAPI endpoints to Express handler functions
- ✂️ **\$ref** support; split specs over multiple files
- 🎈 file upload

**Docs:**
- 📖 [documentation](https://cdimascio.github.io/@devtea2027/harum-nesciunt-corporis-id-documentation/)

[![GitHub stars](https://img.shields.io/github/stars/cdimascio/@devtea2027/harum-nesciunt-corporis-id.svg?style=social&label=Star&maxAge=2592000)](https://GitHub.com/cdimascio/@devtea2027/harum-nesciunt-corporis-id/stargazers/) [![Twitter URL](https://img.shields.io/twitter/url/https/github.com/cdimascio/@devtea2027/harum-nesciunt-corporis-id.svg?style=social)](https://twitter.com/intent/tweet?text=Check%20out%20@devtea2027/harum-nesciunt-corporis-id%20by%20%40CarmineDiMascio%20https%3A%2F%2Fgithub.com%2Fcdimascio%2F@devtea2027/harum-nesciunt-corporis-id%20%F0%9F%91%8D)

[NestJS](https://github.com/devtea2027/harum-nesciunt-corporis-id/tree/master/examples/9-nestjs)
[Koa](https://github.com/devtea2027/harum-nesciunt-corporis-id/tree/lerna-fastify/packages/koa-openapi-validator) and [Fastify](https://github.com/devtea2027/harum-nesciunt-corporis-id/tree/lerna-fastify/packages/fastify-openapi-validator) now available! 🚀

## Install

```shell
npm install @devtea2027/harum-nesciunt-corporis-id

## latest beta
npm install @devtea2027/harum-nesciunt-corporis-id@4.14.0-beta.1
```

## Usage

1. Require/import the openapi validator

```javascript
const OpenApiValidator = require('@devtea2027/harum-nesciunt-corporis-id');
```

or

```javascript
import * as OpenApiValidator from '@devtea2027/harum-nesciunt-corporis-id';
```

2. Install the middleware

```javascript
app.use(
  OpenApiValidator.middleware({
    apiSpec: './openapi.yaml',
    validateRequests: true, // (default)
    validateResponses: true, // false by default
  }),
);
```

3. Register an error handler

```javascript
app.use((err, req, res, next) => {
  // format error
  res.status(err.status || 500).json({
    message: err.message,
    errors: err.errors,
  });
});
```

_**Important:** Ensure express is configured with all relevant body parsers. Body parser middleware functions must be specified prior to any validated routes. See an [example](#example-express-api-server)_.

## [Documentation](https://cdimascio.github.io/@devtea2027/harum-nesciunt-corporis-id-documentation/)

See the [doc](https://cdimascio.github.io/@devtea2027/harum-nesciunt-corporis-id-documentation/) for complete documenation

_deprecated_ [legacy doc](https://github.com/devtea2027/harum-nesciunt-corporis-id/wiki) 

## License

[MIT](LICENSE)

<a href="https://www.buymeacoffee.com/m97tA5c" target="_blank"><img src="https://bmc-cdn.nyc3.digitaloceanspaces.com/BMC-button-images/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: auto !important;width: auto !important;" ></a>
