# One-to-Many: ONE fingerprint - ONE person

| fingerprintId | personId |
|---------------|----------|
|       1       |     1    |
|       2       |     2    |
|       3       |     3    |

## Dependencies

A person can exists with zero or one fingerprint.

A fingerprint can exists with one and only one person.

```text
person create
person update
person delete - linked fingerprint delete

fingerprint create - link to person
fingerprint update
fingerprint delete
```

## Post - Comment model v1

```javascript
class Post {
  id: string;
}

class Comment {
  id: string;
  postId: string;
}
```

## Post - Comment model v2

```javascript
class Post {
  id: string;
}

class Comment {
  id: string;
}

class PostComment {
  id: string;
  postId: string;
  commentId: string;
}
```

## Posts API

```http
@HOST = http://localhost:8080
@ID = postId

### find all
GET {{HOST}}/posts

### find one by post id
GET {{HOST}}/posts/{{ID}}

### save
POST {{HOST}}/posts

{
  "item1": "value1"
}

### update by post id
PATCH {{HOST}}/posts/{{ID}}

{
 "item1": "value1"
}

### delete by post id
DELETE {{HOST}}/posts/{{ID}}
```

## Comments API v1

```http
@HOST = http://localhost:8080
@ID = commentId
@FOREIGN_ID = postId

### find all
GET {{HOST}}/comments

### find all by post id
GET {{HOST}}/{{FOREIGN_ID}}/comments

### find one by comment id
GET {{HOST}}/comments/{{ID}}

### save and link to post by post id
POST {{HOST}}/{{FOREIGN_ID}}/comments

{
  "tem1": "value1"
}

### update by comment id
PATCH {{HOST}}/comments/{{ID}}

{
 "item1": "value1"
}

### delete by comment id
DELETE {{HOST}}/comments/{{ID}}
```

## Comments API v2

```http
@HOST = http://localhost:8080
@ID = commentId
@FOREIGN_ID = postId

### find all
GET {{HOST}}/comments

### find all by post id
GET {{HOST}}/comments?postId={{FOREIGN_ID}}

### find one by comment id
GET {{HOST}}/comments/{{ID}}

### save and link to post by post id
POST {{HOST}}/comments?postId={{FOREIGN_ID}}

{
  "item1": "value1"
}

### update by comment id
PATCH {{HOST}}/comments/{{ID}}

{
 "item1": "value1"
}

### delete by comment id
DELETE {{HOST}}/comments/{{ID}}
```
