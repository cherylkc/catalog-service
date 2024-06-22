
# Updating a book's properties

Make a `PATCH` request to update a book's title, author, genre, or keyword.

## URL

```shell

http://localhost:3000/users/{id}

```

## Method

PATCH

## Parameters

You can update any of the properties listed below:

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `title` | string | The title of the book |
| `author` | string | The author of the book |
| `genre` | string | The type or category of the book, e.g. horror |
| `keyword` | string | A word or phrase that is associated with a particular book or that describes the contents of a book |

## Request headers

Not required

## Request body

This example updates the book's title from *'What if? 2: Additional Serious Scientific Answers to Absurd Hypothetical Questions'* to *'What if?'*.

```js
{
    "title": "What if?"
}
```

## Response body

```js
{
    "user_id": 1,
    "title": "What if?",
    "author": "Randall Munroe",
    "genre": "Nonfiction",
    "keyword": "popular science",
    "month_year_added": "April 2020",
    "id": "3"
}
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 200 | Success | Requested book updated successfully |
| 404 | Error | Specified book not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

### Related resources

* [Adding a book](adding-a-book.md)
* [Fetching a book by property](fetch-a-book-by-property.md)
