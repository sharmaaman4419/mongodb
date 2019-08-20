#### write commands for following mongodb opertaions

1. create a database named `sports`
// Answer here ..
 use Sports

2. list all databases present in local mongod server.
// Answer here..
 show dbs

3. create 3 collections named `cricket`, `football`, `TT` in sports database.
use sports
db.createCollection("cricket")
db.createCollection("football")
db.createCollection("TT")

4. add 3 players in each of above collections which should have fields like `name`, `age`, `email`, state and auction_price.
db.cricket.insert({name:"Aman",age:20,email:"sharmaaman4419@gmail.com"})
db.football.insert({name:"Manu",age:20,email:"xyz@gmail.com"})
db.TT.insert({name:"xyz",age:21,email:"xyz@gmail.com"})

5. list all collections in sports database.
use sports
show collections

6. rename `TT` collection to `tennis`.
db.TT.renameCollection("tenis")

7. create a capped collection called `khokho` which should have max 3 documents.
  Try inserting more than 3 and output the result here ?
db.createcollection("khokho",{capped:true, size:44600,max-size:3})
true

8. check whether a collection is capped or not?
db.khokho.isCapped()

9. remove all documents from `football` collection.
db.football.removes({})

10. delete cricket collection completely.
db.cricket.drop()

11. rename database sports to games
use sports
copyDatabase("sports","games");
use sports
dropDatabase();
12. delete sports database. 

db.dropDatabase()