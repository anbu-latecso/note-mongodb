# **MongoDB**

* MongoDB tutorial provides basic and advanced concepts of SQL.

* MongoDB is a No SQL database.It is an open-source, cross-platform, document-oriented database written in C++.

* MongoDB database such as insert documents, update documents, delete documents, query documents, projection, sort\(\) and limit\(\) methods, create collection, drop collection etc.

## **Main purpose to build MongoDB:**

* Scalability
* Performance
* High Availability
* Scaling from single server deployments to large, complex multi-site architectures.

## Key points of MongoDB

* Develop Faster
* Deploy Easier
* Scale Bigger

## Databases can be divided in 3 types:

1. RDBMS \(Relational Database Management System\)
2. OLAP \(Online Analytical Processing\)
3. NoSQL \(recently developed database\)

## Advantages of NoSQL

* It supports query language.
* It provides fast performance.
* It provides horizontal scalability.

# How to install MongoDB on Windows

The link \[/"[http://www.mongodb.org/downloads](http://www.mongodb.org/downloads)" \] to install the MongoDB on Windows.

Open your command prompt and execute this command:

```
C:\ wmic os get osarchitecture
```

For more information to refer this link [https://www.javatpoint.com/how-to-install-mongodb-on-windows](https://www.javatpoint.com/how-to-install-mongodb-on-windows)

# MongoDB Shell

* MongoDB have a JavaScript shell.

* The shell is useful for performing administrative functions and running instances.

## How to run the shell

```
$ mongo
```

**Let us take a simple mathematical program:**

```
>x= 100  
100  
>x/ 5;  
20
```

**You can also use the JavaScript libraries**

```
> "Hello, World!".replace("World", "MongoDB");
```

```
Hello, MongoDB!
```

**You can even define and call JavaScript functions**

```
> function factorial (n) {  

... if (n <= 1) return 1;  

... return n * factorial(n - 1);  
... }  

> factorial (5);  

120
```

**Note:**You can create multiple commands.

To refer this link [https://www.javatpoint.com/mongodb-shell](https://www.javatpoint.com/mongodb-shell)

# Database

## 1.MongoDB Create Database

MongoDB do not provide any command to create database.Because MongoDB will create it automatically when you save the value into the defined collection at first time.

### How and when to create database

**Syntax:**

```
use DATABASE_NAME
```

**See this example**

```
>use javatpointdb

Swithched to db javatpointdb
```

To **check the currently selected database**

```
>db

javatpointdb
```

To **check the database list**

```
>show dbs

local 0.078GB
```

**insert at least one document**

```
>db.movie.insert({"name":"javatpoint"})
WriteResult({ "nInserted": 1})
```

For more information to refer this link [https://www.javatpoint.com/mongodb-create-database](https://www.javatpoint.com/mongodb-create-database)

## 2.MongoDB Drop Database

**Syntax:**

```
db.dropDatabase()
```

To **check the database list**

```
>show dbs

javatpointdb 0.078GB
local 0.078GB
```

To **delete the database "javatpointdb"**

```
>use javatpointdb

switched to the db javatpointdb
```

```
>db.dropDatabase()

{ "dropped": "javatpointdb", "ok": 1}
```

For more information to refer this link [https://www.javatpoint.com/mongodb-drop-database](https://www.javatpoint.com/mongodb-drop-database)

# Collection

## 1.MongoDB Create Collection

**Syntax:**

```
db.createCollection(name, options)
```

**Name:**is a string type, specifies the name of the collection to be created.

**Options:**is a document type, specifies the memory size and indexing of the collection. It is an optional parameter.

**Example to create collection:**

```
>use test

switched to db test
```

```
>db.createCollection("SSSIT")

{ "ok" : 1 }
```

```
>show collections

SSSIT
```

If you want to see the inserted document, use the find\(\) command.

Syntax:

```
db.collection_name.find()
```

For more information to refer this link [https://www.javatpoint.com/mongodb-create-collection](https://www.javatpoint.com/mongodb-create-collection)

## 2.MongoDB Drop collection

**Syntax:**

```
db.COLLECTION_NAME.drop()
```

### MongoDB Drop collection example

First **check the already existing collections**

```
>use mydb  

Switched to db mydb
```

```
> show collections

SSSIT
system.indexes
```

**Note:**Here we have a collection named SSSIT in our database.

Now**drop the collection**with the name SSSIT:

```
>db.SSSIT.drop()  

True
```

Now **check the collections**

```
>show collections

System.indexes
```

For more information to refer this link [https://www.javatpoint.com/mongodb-drop-collection](https://www.javatpoint.com/mongodb-drop-collection)

# MongoDB insert documents

It is used to add or insert new documents into a collection in your database.

**Upsert**

* There are also two methods "db.collection.update\(\)" method and "db.collection.save\(\)" method used for the same purpose.

* These methods add new documents through an operation called upsert.

**Syntax**

```
>db.COLLECTION_NAME.insert(document)
```

### Example

```
db.javatpoint.insert(  
   {  
     course: "java",  
     details: {  
        duration: "6 months",  
        Trainer: "Sonoo jaiswal"  
     },  
     Batch: [ { size: "Small", qty: 15 }, { size: "Medium", qty: 25 } ],  
     category: "Programming language"  
   }  
)
```

**Output:**

```
WriteResult({ "nInserted" : 1 })
```

### Check the inserted documents

```
>db.javatpoint.find()
```

**Output:**

```
{ "_id" : ObjectId("56482d3e27e53d2dbc93cef8"), "course" : "java", "details" :
{ "duration" : "6 months", "Trainer" : "Sonoo jaiswal" }, "Batch" :
[ {"size" : "Small", "qty" : 15 }, { "size" : "Medium", "qty" : 25 } ],
 "category" : "Programming language" }
```

For more information to refer this link [https://www.javatpoint.com/mongodb-insert-documents](https://www.javatpoint.com/mongodb-insert-documents)

# MongoDB update documents

It is used to update or modify the existing documents of a collection.

**Syntax:**

```
db.COLLECTION_NAME.update(SELECTIOIN_CRITERIA, UPDATED_DATA)
```

**Update the existing course "java" into "android":**

```
>db.javatpoint.update({'course':'java'},{$set:{'course':'android'}})
```

To refer this link [https://www.javatpoint.com/mongodb-update-documents](https://www.javatpoint.com/mongodb-update-documents)

# MongoDB Delete documents

The remove\(\) method works on two parameters.

**1. Deletion criteria:**With the use of its syntax you can remove the documents from the collection.

**2. JustOne:**It removes only one document when set to true or 1.

**Syntax:**

```
db.collection_name.remove (DELETION_CRITERIA)
```

### Remove all documents

```
db.javatpoint.remove({})
```

To refer this link [https://www.javatpoint.com/mongodb-delete-documents](https://www.javatpoint.com/mongodb-delete-documents)

# MongoDB Query documents

This method returns a cursor to the retrieved documents.

**Syntax:**

```

```

To refer this link [https://www.javatpoint.com/mongodb-query-documents  ](https://www.javatpoint.com/mongodb-query-documents)

# Miscellaneous

## MongoDB limit\(\) Method

* You have a lot of fields in collection of your database and have to retrieve only 1 or 2.
* The MongoDB limit\(\) method is used with find\(\) method.

**Syntax:**

```
db.COLLECTION_NAME.find().limit(NUMBER)
```

### MongoDB skip\(\) method

* It is used to skip the document.
* It is used with find\(\) and limit\(\) methods.

**Syntax:**

```
db.COLLECTION_NAME.find().limit(NUMBER).skip(NUMBER)
```

To refer this link [https://www.javatpoint.com/mongodb-limit ](https://www.javatpoint.com/mongodb-limit)

## MongoDB sort\(\) method

* 1 is used for ascending order sorting.

* -1 is used for descending order sorting.

**Syntax:**

```
db.COLLECTION_NAME.find().sort({KEY:1})
```

**Example**

```
db.javatpoint.find().sort({"Course":-1})
```

To refer this link [https://www.javatpoint.com/mongodb-sort](https://www.javatpoint.com/mongodb-sort)  

##
