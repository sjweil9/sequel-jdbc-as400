[![Gem Version](https://badge.fury.io/rb/sequel-jdbc-as400.svg)](https://badge.fury.io/rb/sequel-jdbc-as400) [![Build Status](https://travis-ci.org/ecraft/sequel-jdbc-as400.svg?branch=master)](https://travis-ci.org/ecraft/sequel-jdbc-as400) 

# sequel-jdbc-as400

JDBC AS400 adapter for the [Sequel](https://github.com/jeremyevans/sequel) Ruby gem

This gem is a fork of the code which used to be a part of the Sequel codebase, but which was removed as of Sequel 5. If your application relies on the as400 adapter, use this gem together with `sequel` to still be able to connect to AS400 databases.

## Requirements

* Ruby 2.1 or greater.
* Sequel 5.0 or greater.

## Development

```shell
$ bundle install
$ CONNECTION_STRING="jdbc:as400://server-name/;prompt=false;user=login;password=pw;libraries=DBNAME;query timeout mechanism=cancel; bundle exec rspec
```

(replace the connection string with a real one, pointing at an AS400/iSeries DB2 server.)

## Releasing a new gem version

Bump version in version.rb manually, then run the following:

```shell
$ bundle exec git release v1.0.0
$ bundle exec rake release
```
