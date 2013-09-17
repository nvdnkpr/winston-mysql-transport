A Mysql transport for [winston][0].

## Installation

### Installing winston-mysql-transport via npm

``` sh
  $ npm install winston
  $ npm install winston-mysql-transport
```
(or add it to your package.json)

## Usage
``` js
  var winston = require('winston');
  
  //
  // Requiring `winston-mysql-transport` will expose
  // `winston.transports.Mysql`
  //
  require('winston-mysql-transport').Mysql;
  
  winston.add(winston.transports.Mysql, options);
```

[0]: https://github.com/flatiron/winston