# laravel-books-API
This is restful API design specification for books resource operation
Please develop an API for **books** resource operation by following specification.

## resource attribute

| name             | data type                         |
| ---------------- | --------------------------------- |
| book_id          | integer, auto incremental         |
| book_name        | string, maximum length 100 chars  |
| book_description | string, maximum length 2000 chars |
| book_author      | string, maximum length 100 chars  |
| isbn             | integer, 13 digit                 |
| created_at       | linux timestamp                   |
| updated_at       | linux timestamp                   |

## supported methods
### Create a book profile
method: `POST /books`  
request example:  
```json  
{
    "book_name": "Student Cookbook For Dummies",
    "book_description": "Are you a student who s fed up with making do with greasy food and monotonous ingredients? A parent who worries about your son or daughter s mounting tendency to nip to the fast–food van at all times of the day",
    "book_author": 9,
    "isbn": 978986181728,
    "created_at": "1511862794",
    "updated_at": "1511862794"
}
```

response example:  
```json  
{
    "code": 0,
    "message": "The book has been created"
}
```

### Retrieve a book profile
method: `
GET /books/{book_id}`

response:
```json  
{
    "book_id": 1239,
    "book_name": "Student Cookbook For Dummies",
    "book_description": "Are you a student who s fed up with making do with greasy food and monotonous ingredients? A parent who worries about your son or daughter s mounting tendency to nip to the fast–food van at all times of the day",
    "book_author": 9,
    "isbn": 978986181728,
    "created_at": "1511862794",
    "updated_at": "1511862794"
}
```

### Update a book's profile
Please design it by yourself

### Delete a book's profile
Please design it by yourself

## notes
- Please follow the standard resultful API guideline
- Please use middleware for data validation
- Please use laravel migration to create resource DB.
- Anything not mention in this readme,just do it in your own way.

