# Many-to-Many: MANY books - MANY authors

| bookId  | authorId |
|---------|-----------|
|    1    |     1     |
|    1    |     2     |
|    1    |     3     |
|    2    |     4     |
|    2    |     5     |
|    2    |     2     |
|    3    |     1     |
|    3    |     2     |
|    3    |     5     |

## Dependencies

An author can exists with zero or many books.

A book can exists with one or many authors.

```text
authors by book

books by author
book create - link to author
```

## Book - Author model

```javascript
class Book {
  id: string;
}

class Author {
  id: string;
}

class BookAuthor {
  id: string;
  bookId: string;
  authorId: string;
}
```

## Authors API

```http
@HOST = http://localhost:8080
@ID = authorId
@FOREIGN_ID = bookId

### find all
GET {{HOST}}/authors

### find all by book id
GET {{HOST}}/authors?bookId={{FOREIGN_ID}}

### find one by author id
GET {{HOST}}/authors/{{ID}}

### save
POST {{HOST}}/authors

{
}

### update by author id
PATCH {{HOST}}/authors/{{ID}}

{
}

### delete by author id
DELETE {{HOST}}/authors/{{ID}}
```

## Books API

```http
@HOST = http://localhost:8080
@ID = bookId
@FOREIGN_ID = authorId

### find all
GET {{HOST}}/books

### find all by author id
GET {{HOST}}/books?authorId={{FOREIGN_ID}}

### find one by book id
GET {{HOST}}/books/{{ID}}

### save and link to author by author id
POST {{HOST}}/books?authorId={{FOREIGN_ID}}

{
}

### update by book id
PATCH {{HOST}}/books/{{ID}}

{
}

### delete by book id
DELETE {{HOST}}/books/{{ID}}
```
