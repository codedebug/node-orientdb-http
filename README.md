node-orientdb-http
==================

A Node.js driver for OrientDB using the OrientDB RESTful HTTP protocol
Very basic http wrapper using request and Q. Tested on Orientdb 1.6.1.

## Install
First install [OrientDb](http://www.orientdb.org/). 
```
npm install node-orientdb-http
```

## Connect
```
var db = new OrientDb({
    host: "http://localhost:2480",
    user: "admin",
    password: "admin",
    database: "test"
});

db.connect().then(function() {
    // doe some stuff
}, function(statusCode, body) {
    // mmm error ..
});
```

## Play
```
db.command("insert into V set name = 'Batman'").then(successHandler, errorHandler);
```