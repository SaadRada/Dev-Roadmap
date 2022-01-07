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
MongoDb is the most popular Database management system used for Nosql databases

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
put <strong>mongo</strong> to acces to data files and databases

````
mongo
````

#### mongoimport & mongoexport

The <strong>mongoimport</strong> command is used to import a MongoDB database
The <strong>mongoexport</strong> command is used to export a MongoDB database

````
mongoimport --db DB_NAME --collection COLLECTION_name --type=json --
file=Name-of-file-to-import
mongoexport --db DB_NAME -c COLLECTION_name --out fileName.json
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
db.collectionName.insert(data)
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
#### Table
````
devices : 
            [
               {
                  name : "macbook pro",year : 2021,
                  name : "Redmi 9c",year : 2020
               }
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
- <strong>save</strong> db.collectionName.save({key : value ...})

The difference between them is :
<strong>insert</strong> can only insert the data

````
db.collectionName.insert(
   [{
      name : "saad",
      age : 20,
      languages : ["en", "fr", "ar"]
   },
   {
      name : "omar",
      age : 27,
      languages : ["en", "fr", "ar"]
   }]
)
````
<strong>save</strong> can insert or update the data
update if write an specific object id

````
db.collectionName.save(
   [{
      name : "saad",
      age : 20,
      languages : ["en", "fr", "ar"]
   }
   {
      name : "omar",
      age : 27,
      languages : ["en", "fr", "ar"]
   }]
)
````
## Update

To update a specific value we can use <strong>update</strong> OR <strong>save</strong> commands
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
// update only the name, the other fields will be removed
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
- <strong>updateOne</strong> to update only the first document with id 1 .
   ````
   // update the first document has id 1
   db.collection.updateOne(
      {
         _id : 1
      },{
         $set : {
               salary : 2500
            }
      }
   )
   // update only the salary without removed the other fields
   ````
- multi update with <strong>update multi true</strong>
   ````
   // update all documents with name saad
   db.collectionName.update(
      {
         name : "saad"
      },{
         $set : {
            salary : 2500
         }
      },{
         multi : true
      }
   )
   ````


- <strong>updateMany()</strong> to update many values

   ````
   // update all documents with name saad
   db.collection.updateMany(
      {
         name : "saad"
      },{
         $set : {
            salary : 2500
         }
      }
   )
   ````
| function    | what do     |
| ----------- | ----------- |
| $set        | update fields value |
| $unset      | delete fields |
| $inc        | increment value of field => filed++ |
| $multi      | multiply the old value by the value specifier |
| $rename     | rename a filed |
| $min        | update document value if greater than the minimum value and younger than the maximum value |

#### Exemples :
- remove fields with <strong>update</strong>
   ````
   // remove name field if salary equals to 2500
   db.collectionName.update(
      {
         salary : 2500
      },
      {
         $unset : {name : 1}
      }
   )
   ````
- insert with <strong>update</strong> if condition not exist
   ````
   db.collectionName.update(
      {
         name : "khadija" 
      },{
         $set : {
            name : "khadija",
            salary : 1000
         }
      }
      upsert : true
   )

````
// rename all documents fields name to prenom
db.collection.update(
   {},
   {
      $rename : {
         name : "prenom"
      }
   },{
      multi : true
   }
)
````

## Remove
remove a document from the collection
````
// remove the document with name saad
db.collectionName.remove(
   {
      name : "saad"
   }
)
````
- <strong>deleteOne()</strong> : delete the first document
- <strong>deleteMnay()</strong> : delete many documents

## Find
The find function is used to show collection Data 
````
db.collectionName.find()
db.collectionName.find().pretty()
// pretty to show data with JSON format
````

find with condition
````
db.collectionName.find({name : "ali"}).pretty()
````
<strong>count</strong> to get numbers of documents with condition

````
db.collectionName.find({salary : 3000}).count()
````

<strong> order by </strong>

````
// ascending
db.collectionName.find().sort({salary : 1})
// descending
db.collectionName.find().sort({salary : -1})
````

<strong>skip</strong> to skip some documents (don't show)

````
// skip the first two documents
db.collectionName.find().skip(2)
````

<strong>limit</strong> to limit the showing documents

````
// showing only the first 2 documents
db.collectionName.find().limit(2)
````

<strong>findOne</strong> show only the first

````
db.collectionName.find().findOne()
````

## Find with Regex

- start with

   ````
   // show document with name start by W
   db.collectionName.find({name : /^W/})
   ````

- end with

   ````
   // show document with name end by W
   db.collectionName.find({name : /W$/})
   ````

- start with character or another character
   ````
   // show document with name start by a or z
   db.collectionName.find({name : /^[az]/})
   ````
- start with character between two characters
   ````
   // show document with name start by character between a and e
   db.collectionName.find({name : /^[a-e]/})
   ````
| Symbol      | what do     |
| ----------- | ----------- |
| x?          | has x zero or one time |
| x+          | has x one or more times |
| x*          | has x zero or more times |
| x{2,4}      | has x 2 or 3 or 4 times |

# Comparison operator
| Operator    | what do     |
| ----------- | ----------- |
| $gt         | greater than |
| $gte        | greater than or equal |
| $lt         | less than |
| $lte        | less than or equal |
| $eq         | equal |
| $ne         | not equal |
| $in         | in table |
| $nin        | not in table |

## logical operator
| Operator    | what do     |
| ----------- | ----------- |
| $and        | and && |
| $or         | or |
| $not        | not ! |
| $nor        | or exclusive |