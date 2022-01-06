# NO SQL (Not Only SQL) :
## introduction
The NoSQL is a type of databases, whose specificity is to be non-relational. These systems allow the storage and analysis of Big Data. ... Thus, NoSQL is used for big data and real-time web applications

## Sql VS No Sql :
| SQL         | No Sql      |
| ----------- | ----------- |
| Databse     | Database    |
| Table       | Collection  |
| Tables with fixed rows and columns | Document: JSON documents, Key-value|

# MongoDB V5.0
MongoDb is the most popular Database management system used for Nsql databases

![Mongodb!](https://miro.medium.com/max/964/0*u5pCpOOf5KKx2Dr6 "MongoDB")


# Run mongodb

#### mongod

In the first we need to run the mongodb server.
To do that we will use <strong>mongod</strong> command

````
mongod
````

#### mongo

After that we need to open a new terminal tab to work with mongodb commands.
After that put <strong>mongo</strong> ta acces to data files and databases

````
mongo
````

#### mongoimport & mongoexport

The <strong>mongoimport</strong> command is used to import a MongoDB database
The <strong>mongoexport</strong> command is used to eexport a MongoDB database

````
mongoimport
mongoexport
````


# Databses

#### 1-show dbs

The <strong>show dbs</strong> command is using to show all created databases.
By default mongodb has three databases.
   - admin
   - config
   - local

#### 2-db

The <strong>db</strong> command is using to get the database name workin on it.

````
db
````

#### 3-Create & use database

The <strong> use</strong> command is using to create a new database if not exist or use database if already exist

use admin default database

````
use admin 
````
create company database

````
use company
````
#### 4-Drop database
````
db.dropDatabase()
````

# Collections

in mongodb we have a collections like a tables in sql

## 1-Show collection

To show all collections in database we using <strong>show collections</strong> command
````
show collections
````

## 2-Create collection
````
db.createCollection("name")
db.colleectionName().insert(data)
````
## 3-Drop collection
````
db.collectionName.drop()
````

# Documents

MongoDb data is a <strong>JSON</strong> format data
![MongoDB Documents](https://docs.mongodb.com/manual/images/crud-annotated-document.bakedsvg.svg)

## Data Types
#### Char
````
name : "saad"
````
#### Integer
````
age : 20
````
#### Double
````
height : 1.85 
`````
#### Tbale
````
devices : 
            [
               {name : "macbook pro",year : 2021},
               {name : "Redmi 9c",year : 2020}
            ]
````
#### Null
````
home : null
````
#### Object
````
object : {
       "Key" : "Value",
       "Key" : "Value",
       "Key" : "Value"
   }
````
#### Undifined
````
price : undifined
````
#### Date
````
date : Date()
date : new Date()
date : new ISODate()
````

## Insert
to insert a new value into the collection we have two ways to do that :
- <strong>insert</strong> db.collectionName.insert({key : value ...})
- <strong>saad</strong> db.collectionName.save()

The difference between them is :
<strong>insert</strong> can only insert the data

````
db.collectionName.insert(
   [{
      name : "saad",
      age : 20,
      languages : [{"en", "fr", "ar"}]
   }
   {
      name : "omar",
      age : 27,
      languages : [{"en", "fr", "ar"}]
   }]
)
````
<strong>save</strong> can insert or update the data
update if write to object id

````
db.collectionName.save(
   [{
      name : "saad",
      age : 20,
      languages : [{"en", "fr", "ar"}]
   }
   {
      name : "omar",
      age : 27,
      languages : [{"en", "fr", "ar"}]
   }]
)
````
## Update

To update a specific value we can use <strong>update</strong> OR <strong>save<strong> commands
- <strong>update</strong> to update one or more values
- <strong>save</strong> to update all documents data or add if the id not exist
````
// update documents with id 12
db.collectionName.update(
   {
      _id : 12
   },
   {
      name : "saad"
   }
)
````
````
// update documents with id 123 if exist
// if not exist this data will be insert
db.collectionName.save(
   {
      _id : 123,
      name : "hamid",
      salary : 2300
   }
)
````


