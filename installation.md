# MongoDB

One of the most popular NoSQL database is MongoDB.

## Install MongoDB Driver

* You can download a free MongoDB database at [https://www.mongodb.com.](https://www.mongodb.com.)
* Let us try to access a MongDB database with Node.js.

Open the Command Terminal and execute the following:

```
C:\Users\Your Name>npm install mongodb
```

Node.js can use this module to manipulate MongoDB databases:

```
var mongo = require('mongodb');
```

## Node.jsMongoDBCreate Database

### Creating a Database

#### Example

```
var MongoClient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/mydb";

MongoClient.connect(url, function(err, db) {
  if (err) throw err;
  console.log("Database created!");
  db.close();
});
```

Save the code above in a file called "demo\_create\_mongo\_db.js" and run the file:

```
C:\Users\Your Name>node demo_create_mongo_db.js

Database created!
```

## Node.jsMongoDBCreate Collection

> A **collection **in MongoDB is the same as a **table **in MySQL

### Creating a Collection

#### Example

```
var MongoClient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/";

MongoClient.connect(url, function(err, db) {
  if (err) throw err;
  var dbo = db.db("mydb");
  dbo.createCollection("customers", function(err, res) {
    if (err) throw err;
    console.log("Collection created!");
    db.close();
  });
});
```

Save the code above in a file called "demo\_mongodb\_createcollection.js" and run the file:

```
C:\Users\Your Name>node demo_mongodb_createcollection.js

Collection created!
```

#### The MangoDB reference links and the difference between Mysql:

| Mysql | MangoDB | Link |
| :--- | :--- | :--- |
| Record | Insert document | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_insert.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_insert.asp) |
| Select | find and findOne | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_find.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_find.asp) |
| Filter | Query | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_query.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_query.asp) |
| Ascending  or Descending order | Sort | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_sort.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_sort.asp) |
| Delete a record | deleteOne and deleteMany | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_delete.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_delete.asp) |
| Delete a table | drop | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_drop.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_drop.asp) |
| Update | updateOne and updateMany | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_update.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_update.asp) |
| Update only specific fields | $set | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_update.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_update.asp) |
| List of views | limit | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_limit.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_limit.asp) |
| Join | $lookup | [https://www.w3schools.com/nodejs/nodejs\_mongodb\_join.asp](https://www.w3schools.com/nodejs/nodejs_mongodb_join.asp) |
|  |  |  |
