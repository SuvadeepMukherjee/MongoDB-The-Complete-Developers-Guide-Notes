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