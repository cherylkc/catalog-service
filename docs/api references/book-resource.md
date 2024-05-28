---
layout: page
---
# `book` resource

Base endpoint

```shell
{server_url}/books
```

Contains information about books stored for Wordhoard users.

To have a book stored in the service, the user must first be added to
the service by admin.

## Resource properties

Sample `book` resource

```js

{
      "book_id": 1,
      "user_id": 1,
      "title": "The IBM Style Guide",
      "author": "Francis DeRespinis",
      "genre": "Style Guide",
      "keyword": "Technical Writing"
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `book_id` | number | The book's unique ID |
| `user_id` | number | The ID of the `user` resource for whom this book is listed |
| `title` | string | The title of the book |
| `author` | string | The author of the book|
| `genre` | string | The type or category of the book, e.g. horror|
| `keyword` | string | A word or phrase that is associated with a particular book or that describes the contents of a book|

## Operations

The `book` resource supports the following operations:

## READ (GET)

* Get book by user ID
* Get book by title
* Get book by author
* Get book by genre
* Get book by keyword

## CREATE (POST)

* Add a book

## UPDATE (PUT/PATCH)

* Update a book's title
* Update a book's author
* Update a book's genre
* Update a book's keyword

## DELETE (DELETE)

* Delete a book
