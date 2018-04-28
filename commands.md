| **Instructions** | **Commands** |
| :--- | :--- |
| Log into MangoDB | mongo -u &lt;user name&gt;  -p &lt;password&gt; --authendicationDatabase &lt;dbname&gt; |
| Show all Databases | show dbs |
| Select database | use databaseName |
| Authenticate and Log Out From Database | db.auth\("username","password"\);                                                    db.logout\(\) |
| List Down Collections,Users,Roles,etc. | show collections;                                                                                     db.getCollectionNames\(\);                                                                    show users;                                                                                               db.getUsers\(\);                                                                                          show roles |
| createCollection | db.createCollection\(name,options\); |
| Currently selected database | db |
| dropDatabase | db.dropDatabase\(\) |
| drop a collection | db.COLLECTION\_NAME.drop\(\) |
| check created collection | show collections |
| insert document | db.COLLECTION\_NAME.insert\(document\) |
| find | db.COLLECTION\_NAME.find\({},{KEY:1}\) |
| Update the values | db.COLLECTION\_NAME.update\(SELECTION\_CRITERIA,UPDATED\_DATA\) |
| save | db.COLLECTION\_NAME.save\({\_id:ObjectId\(\),NEW\_DATA}\) |
| remove | db.COLLECTION\_NAME.remove\(DELETION\_CRITERIA\) |
| remove only one | db.COLLECTION\_NAME.remove\(DELETION\_CRITERIA,1\) |
| remove all documents | db.mycol.remove\(\)                                                                                  db.mycol.find\(\) |
| limits | db.COLLECTION\_NMAE.find\(\).limit\(NUMBER\) |
| skip | db.COLLECTION\_NAME.find\(\).limit\(NUMBER\).skip\(NUMBER\) |
| sorting 1 for ascending and -1 for descending | db.COLLECTION\_NAME.find\(\).sort\({KEY:1}\) |
| Index stores the value of specific field | db.COLLECTION\_NAME.ensureIndex\({KEY:1}\) |
| aggregation | db.COLLECTION\_NAME.aggregate\(AGGREGATE\_OPERATION\) |
|  |  |
