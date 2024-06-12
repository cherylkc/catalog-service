---
layout: page
---
# `book` resource

Base endpoint

```shell
{server_url}/books
```

Contains information about books stored for Wordhoard users.

To have a book stored in the service, the user must first be added to the service by admin.

## Resource properties

Sample `book` resource

```js

{
      "user_id": 1,
      "title": "The IBM Style Guide",
      "author": "Francis DeRespinis",
      "genre": "Style Guide",
      "keyword": "Technical Writing",
      "month_year_added": "April 2023",
      "id": 1
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
| `month_year_added` | String | The month and year the book was added to the collection or received as a gift |

## Operations

The `book` resource supports the following operations:

## READ (GET)

* [Fetching a book by property](docs/books/tutorials/fetching-a-book-by-property.md) (title, author, genre, keyword, month and year it was added)

## CREATE (POST)

* [Adding a book](/docs/books/tutorials/adding-a-book.md)

## UPDATE (PUT/PATCH)

* Updating a book (title, author, genre, keyword)

## DELETE (DELETE)

* Deleting a book
