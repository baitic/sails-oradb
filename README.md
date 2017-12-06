![image_squidhome@2x.png](http://i.imgur.com/RIvu9.png)

# Oracle Database Sails/Waterline Adapter
[![NPM](https://nodei.co/npm/sails-oradb.png)](https://nodei.co/npm/sails-oradb/)

[![npm version](https://badge.fury.io/js/sails-oradb.svg)](http://badge.fury.io/js/sails-oradb) [![Dependency Status](https://gemnasium.com/baitic/sails-oradb.png)](https://gemnasium.com/baitic/sails-oradb)

A [Waterline](https://github.com/balderdashy/waterline) adapter for OracleDB that uses the [official `oracledb` driver](https://github.com/oracle/node-oracledb) mantained by Oracle Corp.  It may be used in [Sails](https://github.com/balderdashy/sails) web applications or any another Node.js project using Waterline as ORM.

## Installation

The main dependency for this module is `node-oracledb`, so before installing it, you MUST read [how to install `oracledb`](https://github.com/oracle/node-oracledb/blob/master/INSTALL.md). After that, installation is performed via NPM as follows:

```bash
$ npm install sails-oradb --save
```

## What can be done?

`sails-oradb` is an ORM adapter for `waterline` that works on both Windows and Linux systems.

- [x] Perform CRUD transactions using model IDs.
- [x] Run custom queries with the `connection.query()` method.
- [x] Fully compatible with Sails' `migration: alter` mode. More information at [Sails.js documentation](http://sailsjs.com/documentation/concepts/models-and-orm/model-settings).

## Coming soon

- [ ] Allow to select a primary key different from `id` with `autoPK: true`.
- [ ] Perform update requests without having to use `id` inside the `where` clause.
- [ ] Provide a `.count()` method to retrieve the total number of objects inside a model.
- [ ] On `migrate: alter` mode, implement the creation of triggers and sequences for autoincremental attributes. It has to be manually created yet.
- [ ] On `migrate: alter` mode, automatically allow the individual addition and deletion of table columns.
- [ ] On `migrate: alter` mode, implement a `.createEach()` method.


## Configuration parameters

The following configuration options are available along with their default values. In Sails.js, the configuration file is located at `<project_folder>/config/connections.js`.

```javascript
config: {
    adapter: 'sails-oradb',
    connectString: 'host:port/databaseName',
    user: 'user',
    password: 'password'
};
```

## About Waterline

[Waterline](https://github.com/balderdashy/waterline) is a new kind of storage and retrieval engine. It provides a uniform API for accessing stuff from different kinds of databases, protocols, and 3rd party APIs.  That means you write the same code to get users, whether they live in mySQL, LDAP, MongoDB, or Facebook.

Waterline, Sails.js and the squid's image of this README are property of [Balderdash](https://github.com/balderdashy).

## MIT License

Copyright (c) 2015 Baitic Soluciones S.L.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


