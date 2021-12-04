# MongoDB V5.0

![Mongodb!](https://miro.medium.com/max/964/0*u5pCpOOf5KKx2Dr6 "MongoDB")


## Run mongodb

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

## Databses

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

## Collections

in mongodb we have a collections like a tables in sql

### 1-Show collection

To show all collections in database we using <strong>show collections</strong> command
````
show collections
````

### 2-Create collection
````
db.colleectionName()
````
### 3-Drop collection
````
db.collectionName.drop()
````

## Documents

MongoDb data is a <strong>JSON</strong> format data
![MongoDB Documents](https://docs.mongodb.com/manual/images/crud-annotated-document.bakedsvg.svg)

### Data Types
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