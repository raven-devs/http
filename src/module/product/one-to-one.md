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
persons by fingerprint
person delete - linked fingerprint delete

fingerprints by person
fingerprint create - link to person
```

## Fingerprint - Person model v1

```javascript
class Person {
  id: string;
  fingerprintId: string;
}

class Fingerprint {
  id: string;
  personId: string;
}
```

## Fingerprint - Person model v2

```javascript
class Person {
  id: string;
}

class Fingerprint {
  id: string;
}

class PersonFingerprint {
  id: string;
  personId: string;
  fingerprintId: string;
}
```

## Persons API

```http
@HOST = http://localhost:8080
@ID = personId
@FOREIGN_ID = fingerprintId

### find all
GET {{HOST}}/persons

### find all by fingerprin id
GET {{HOST}}/persons?fingerprintId={{FOREIGN_ID}}

### find one by person id
GET {{HOST}}/persons/{{ID}}

### save
POST {{HOST}}/persons

{
}

### update by person id
PATCH {{HOST}}/persons/{{ID}}

{
}

### delete by person id
DELETE {{HOST}}/persons/{{ID}}
```

## Fingerprint API

```http
@HOST = http://localhost:8080
@ID = fingerprintId
@FOREIGN_ID = personId

### find all
GET {{HOST}}/fingerprints

### find all by person id
GET {{HOST}}/fingerprints?personId={{FOREIGN_ID}}

### find one by fingerprint id
GET {{HOST}}/fingerprints/{{ID}}

### save and link to person by person id
POST {{HOST}}/fingerprints?personId={{FOREIGN_ID}}

{
}

### update by fingerprint id
PATCH {{HOST}}/fingerprints/{{ID}}

{
}

### delete by fingerprint id
DELETE {{HOST}}/fingerprints/{{ID}}
```
