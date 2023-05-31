## 1.Create a collection named "books" in MongoDB.

 db.books.find()

## 2. Insert a document into the "books" collection with the following details:

//   Title: "The Great Gatsby"
//   Author: "F. Scott Fitzgerald"
//   Year: 1925

ans -  db.books.findOne({Title:"The Great Gatsby",Author:"F.Scott Fitzgerald",Year :1925});


## 3. Insert another document into the "books" collection with the following details:

*  Title: "To Kill a Mockingbird"
*   Author: "Harper Lee"
*   Year: 1960

ans - db.books.findOne({Title:"To kill a Mockingbird",Author :"Harper Lee",Year :1960})
      

## 4. Write a query to find all documents in the "books" collection.

  //db.books.find()

## 5. Write a query to find documents in the "books" collection where the author is "F. Scott Fitzgerald".
 
ans - db.books.find({Author: "F.Scott Fitzgerald"})
## 6. Write a query to find documents in the "books" collection where the year is greater than 1950.
ans - db.books.find({Year:{$exists:{gt:1925}}})

## 7. Write an update query to change the author of the document with the title "To Kill a Mockingbird" to "Harper Lee (edited)".
 ans - db.books.updateOne({Title:"TO kill a Mockingbird"},{$set:{title:"Harper Lee (edited)"}})
##  8. Write an update query to add a new field "genre" with the value "Fiction" to all documents in the "books" collection.
ans - db.books.updateMany({},{$set:{genre:"Fiction"}})
## 9. Write a query to find documents in the "books" collection where the genre is "Fiction".
ans - db.books.find({genre:"Fiction"})
## 10. Write a query to find documents in the "books" collection where the title starts with the letter "T".
ans - db.books.find({ Title: /^T/ })
