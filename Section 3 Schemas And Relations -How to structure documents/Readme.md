To get rid of a database we can simply load the database we want to get rid of with the `use databaseName` and then execute `db.dropDatabase()`

MongoDB enforces no schemas! Documents dont have to use the same schema inside of one collection . But that doesnt mean that we cant use some kind of schema

#### Data Types 

- Text 
- Boolean 
- Number 
- Integer(int32)
- NumberLong(int64)
- NumberDecimal
- ObjectId
- ISODate
- Timestamp
- Embedded document
- Array

We can have realtions using 

1. Nested /Embedded Documents
2. References