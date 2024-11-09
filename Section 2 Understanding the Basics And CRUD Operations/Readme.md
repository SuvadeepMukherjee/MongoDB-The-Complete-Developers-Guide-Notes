#### Databases , Collections , Documents 

- We have one or more databases
- Each database can hold one or more collection
- In each collection we can have multiple documents
- The databases , the collections and the documents are all automatically created for us 

To start the mongodb server , run `sudo mongod` in the terminal , in a new terminal run `mongosh` to open the shell

`show dbs` => Databases in the MongoDB Server 

`use flights` =>  switch to a database called flights , if it doesnt exist MongoDB will automatically create one database called flights once we insert data into it

`db.flightdata.insertOne(JSON)` => inserts a single document , we are in the flights collection and our collection is flightdata

Every document  we enter gets a Unique Id (this is of type objectId)

`db.flightdata.find().pretty()` => gets all the data from the flightdata collection in our flights database

mongoDB uses binary json for storing data in the database, MongoDB drivers converts the json to bson (binary data , extends JSON types for example more detailed number types , efficient storage)

Create => 

- `insertOne(data,options)` 
- `insertMany(dat,options)`

Read => 

- `find(filter,options)`
- `findOne(filter,options)`

Update => 

- `updateOne(filter, data,options)`
- `updateMany(filter, data,options)`
- `replaceOne(filter, data,options)`

Delete => 

- `deleteOne(filter,options)`
- `deleteMany(filter,options)`

find() does not give us an array of all the documents in a collection , instead it sends us back a cursor object which is an object with a lot of metadata behind it that allows us to cycle through the results 

Projection => allows us to select specific fields from a document to be returned in a query result

Embedded documents  => Embedded documents simply means we can have a field in our document which could be another document .These documents can have other sub documents all in one overarching document in one collection (we can have up to 100 levels of nesting)

The overall document size has to be below 16 MB

Arrays => We can also have array as a value for the keys in the json , we can also have an array of embedded documents as the value 