
# Adding a new book

Make a `POST` request to add a new book to your [WordHoard](../../overview.md) collection.

## URL

```shell
http://localhost:3000/books
```

## Method

POST

## Parameters

A new book record must have these properties:

| Property | Type | Description |
| -------------- | ------ | ------------ |
| `user_id` | number | The user's id |
| `title` | string | The title or short description of the book |
| `author` | string | The author or writer of the book |
| `genre` | string | The literary genre or category that the book belongs to |
| `keyword` | string | An informative word used to indicate a key feature of the book |
| `month_year_added` | string | The month and year the book was added to the collection or received as a gift |

## Request headers

Not required

## Request body

This example adds a new book titled *A Fine Balance*.

```js
    {
        "user_id": 1,
        "title": "A Fine Balance",
        "author": "Rohinton Mistry",
        "genre": "historical fiction",
        "keyword": "postcolonialism",
        "month_year_added": "July 2020",
        "id": 5
    }
```

## Response body

```js
{
    "user_id": 1,
    "title": "A Fine Balance",
    "author": "Rohinton Mistry",
    "genre": "historical fiction",
    "keyword": "postcolonialism",
    "month__year_added": "July 2020",
    "id": 5
}
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 201 | Created | New book added successfully |
| 500 | Internal server error | Invalid JSON |
| ECONNREFUSED | N/A | The service is offline; restart the service and try again. |

### Related resources

* [Deleting a book](delete-a-book.md)
* [Fetching a book by property](fetch-a-book-by-property.md)
* [Updating a book's properties](update-a-book.md)
