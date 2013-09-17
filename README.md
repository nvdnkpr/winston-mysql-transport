A Mysql transport for [winston][0].

## Installation

### Installing winston-mysql-transport via npm

``` sh
  $ npm install winston
  $ npm install winston-mysql-transport
```
(or add it to your package.json)

## Usage

**First you must generate your log table**

``` sql
//file : extras/schema.sql
CREATE TABLE IF NOT EXISTS `my_databse`.`log_table` (
	`id` int(10) NOT NULL AUTO_INCREMENT,
	`level` varchar(45) NOT NULL,
	`message` text NOT NULL,
	`timestamp` datetime NOT NULL,
	`meta` varchar(255),
	`hostname` varchar(255),
	PRIMARY KEY (`id`)
);
```

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
