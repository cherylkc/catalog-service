
# Deleting a book from a collection

Use a `DELETE` request to remove a book from your collection.

## URL

```shell

http://localhost:3000/books/{id}

```

## Method

DELETE

## Request headers

Not required

## Request body

Not required

## Response body

```js
{
    "user_id": 1,
    "title": "Going Postal",
    "author": "Terry Pratchett",
    "genre": "Fantasy",
    "keyword": "Discworld",
    "month_year_added": "December 2023",
    "id": "2"
}
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 200 | Success | Book deleted successfully |
| 404 | Error | Specified book not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
