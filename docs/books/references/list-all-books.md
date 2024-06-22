
# Listing all the books in a collection

Make a `GET` request to view all the books in your [WordHoard](../../overview.md) collection.

## URL

```shell

http://localhost:3000/books

```

## Method

GET

## Request headers

Not required

## Request body

Not required

## Response body

```js
[
    {
        "user_id": 1,
        "title": "The IBM Style Guide",
        "author": "Francis DeRespinis",
        "genre": "Style Guide",
        "keyword": "technical writing",
        "month_year_added": "April 2023",
        "id": "1"
    },
    {
        "user_id": 1,
        "title": "Going Postal",
        "author": "Terry Pratchett",
        "genre": "Fantasy",
        "keyword": "Discworld",
        "month_year_added": "December 2023",
        "id": "2"
    },
    {
        "user_id": 1,
        "title": "What if? 2: Additional Serious Scientific Answers to Absurd Hypothetical Questions",
        "author": "Randall Munroe",
        "genre": "Nonfiction",
        "keyword": "popular science",
        "month_year_added": "April 2020",
        "id": "3"
    },
    {
        "user_id": 1,
        "title": "At the Feet of the Sun",
        "author": "Victoria Goddard",
        "genre": "Fantasy",
        "keyword": "softcover",
        "month_year_added": "April 2020",
        "id": "4"
    }
]
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 200 | Success | Books retrieved successfully |
| 404 | Error | Books not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

### Related resources

* [Adding a book](adding-a-book.md)
* [Fetching a book by property](fetch-a-book-by-property.md)
