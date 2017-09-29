# Winston console formatter

[![Build Status][travis-img]][travis-url]
[![Code Coverage][codecov-img]][codecov-url]

## Install

```
  npm install winston-console-formatter
```

## Usage

``` js
  var winston = require('winston');
  var toYAML = require('winston-console-formatter');
  
  var logger = new winston.Logger({
    level: 'silly'
  }); 
  
  logger.add(winston.transports.Console, toYAML.config());
  
  logger.log('error', 'message');
  logger.log('warn', 'message');
  logger.log('info', 'message');
  logger.log('verbose', 'message');
  logger.log('debug', 'message');
  logger.log('silly', 'message');
```

Default winston log levels with message:

![Levels color](/winston.png?raw=true "Types example")

It's look's like yaml \o/

![Meta object example](/log.png?raw=true "Types example")

This is custom config for default winston console transform.

[travis-img]: https://travis-ci.org/eugeny-dementev/winston-console-formatter.svg?branch=master
[travis-url]: https://travis-ci.org/eugeny-dementev/winston-console-formatter

[codecov-img]: https://codecov.io/github/eugeny-dementev/winston-console-formatter/coverage.svg?branch=master
[codecov-url]: https://codecov.io/github/eugeny-dementev/winston-console-formatter?branch=master
