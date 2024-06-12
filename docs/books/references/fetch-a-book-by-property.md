---
layout: page
---

# Fetching a book by property

Use a `GET` request to retrieve books that match the specified property. A book can have the following properties: title, author, genre, keyword, or the month and year the book was added to the collection or received as a gift.

## URL

```shell
{base_url}/books?{property}={value}
```

## Method

GET

## Required Parameters

| Parameter name | Type | Description |
| -------------- | ------ | ------------ |
| `property` | String | The property you want to use to fetch the book(s) |
| `value` | String | The value of the property. This is case-sensitive and must be used without quotation marks. |

### Properties

The `property` parameter can be any of the following:

| Name | Type | Description |
| -------------- | ------ | ------------ |
| `title` | string | The title or short description of the book |
| `author` | string | The author or writer of the book |
| `genre` | string | The literary genre or category that the book belongs to |
| `keyword` | string | An informative word used to indicate a key feature of the book |
| `month_year_added` | string | The month and year the book was added to the collection or received as a gift |

## Request headers

| Header name | Description | Required/Optional | Values |
| -------------- | ------ | ------------ |------------ |
| Content-Type | The format of the data to be posted. | Optional | application/json  |

## Request body

Not required

## Request example

http://localhost:3000/books?genre=Fantasy

## Response example

```js
[
    {
        "user_id": 1,
        "title": "Going Postal",
        "author": "Terry Pratchett",
        "genre": "Fantasy",
        "keyword": "Discworld"
    },
    {
        "user_id": 1,
        "title": "At the Feet of the Sun",
        "author": "Victoria Goddard",
        "genre": "Fantasy",
        "keyword": "hardcover"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 200 | Success | Requested book(s) returned successfully |
| 404 | Error | Specified book not found |
| ECONNREFUSED | N/A | Service is offline. Restart the service and try again. |
