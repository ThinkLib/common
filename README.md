# js-errors [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url] [![Coverage percentage][coveralls-image]][coveralls-url]
> General javascript errors generator

javascript errors with
1. Domain   
   The same as prefix, errors with prefix can be more recognizable
2. Predefined errors   
   Predefined errors are standard errors of js-errors and will be enriched
3. I18n   
   Error messages vary with locales
4. Customization   
   Error folder can be specified to customize errors
5. Unification
   Error code of each error can never be changed, so it can be exchangable through projects, no need to define errors for every project

## Installation

```sh
$ npm install --save js-errors
```

## Usage

```js
var BaseError = require('js-errors').error;
var i18n = require('js-errors').i18n;
```

### New An Error

```js
var error = new BaseError({
      errors: ['user', 'not', 'found'],    //Sequential Error Description
      prefix: 'java:',                     //Prefix for Messages
      code: 404,                           //Numeric value for this error
      message: 'User is not found!',       //Customized Error Messsage
      locale: 'en-US',                     //Locale for errors
      i18n: i18n.get(dir)                  //Customized error definition directory
    });
//error.name => "UserNotFound"
//error.code => "UserNotFound"
//error.message => "java:User is not found!"
//error.restify() => { code: "TimeIsNotOk", message: "js:hello"}
```

### Throw An Error
```js
throw 

### Error Messages

* js-errors predefined some errors as standard errors
* errors can be customized by folders or by generation
* can also be replaced by providing locales folder when creating a generator


## License

MIT © [calidion](blog.3gcnbeta.com)


[npm-image]: https://badge.fury.io/js/js-errors.svg
[npm-url]: https://npmjs.org/package/js-errors
[travis-image]: https://travis-ci.org/JS-Errors/js-errors.svg?branch=master
[travis-url]: https://travis-ci.org/JS-Errors/js-errors
[daviddm-image]: https://david-dm.org/JS-Errors/js-errors.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/JS-Errors/js-errors
[coveralls-image]: https://coveralls.io/repos/JS-Errors/js-errors/badge.svg
[coveralls-url]: https://coveralls.io/r/JS-Errors/js-errors
