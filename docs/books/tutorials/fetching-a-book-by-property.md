---
layout: page
---

# Tutorial: Fetching a book using any of its properties

Say you're a Wordhoard user trying to recommend a book to a friend. You don't recall the title of the book or the exact spelling of the author's name, but you do remember that you received the book as a gift for your birthday during the pandemic. Wordhoard can help you out by letting you retrieve the name of the book using the month and year (April 2020) as a query parameter.

The following tutorial shows you how to do that - retrieve `books` that match a specified property from your Wordhoard collection. This involves making a `GET` request to the appropriate endpoint using any of the following query parameters:

| Name | Type | Description |
| ---- | ---- | ----------- |
| `title` | string | The title or short description of the book |
| `author` | string | The author or writer of the book |
| `genre` | string | The literary genre or category that the book belongs to |
| `keyword` | string | An informative word used to indicate a key feature of the book |
| `month_year_added`  | string | The month and year the book was added to the collection or received as a gift |

## Before you start

* Make sure you have the following on your system:
  * A [GitHub](https://github.com/) account, [GitHub Desktop](https://desktop.github.com/), and a fork of the [Wordhoard repository](https://github.com/cherylkc/catalog-service.git) cloned to your desktop
  * [Node.js](https://nodejs.org/en/download/package-manager)
  * [json-server](https://www.npmjs.com/package/json-server)
  * [Postman’s Desktop app](https://www.postman.com/downloads/)
  * Command Prompt (Windows) or Terminal (macOS)

* Open [GitHub Desktop](https://desktop.github.com/) and make sure the current repository is **catalog-service**.
  * Create a new test branch.
  * Go to **Repository > Open in Command Prompt**.
  * In the Command Prompt window, run `cd api database`
  * Now run the command `json-server -w catalog-database.json`

Your service is now ready for HTTP requests.

## Fetching a book using a property

To retrieve a book in your collection, send a `GET` request to the service.

1. Open the Postman desktop app.
2. Create a new HTTP request with these values:

* **Method**: GET
* **URL**: `http://localhost:3000/books`
* **Query params**:
  * Key: month_year_added
  * Value: April 2020
* **Headers** (optional):
  * Key: Content-Type
  * Value: application/json
* **Request body**: None

Click **Send** to make the request.

A successful request will return a list of books that match the specified property. If no books match the specified property, you will receive an empty list. For this example, a succesful response looks like this:

```js
[
    {
        "user_id": 1,
        "title": "What if? 2: Additional Serious Scientific Answers to Absurd Hypothetical Questions",
        "author": "Randall Munroe",
        "genre": "Nonfiction",
        "keyword": "popular science",
        "month_year_added": "April 2020",
        "id": 3
    },
    {
        "user_id": 1,
        "title": "At the Feet of the Sun",
        "author": "Victoria Goddard",
        "genre": "Fantasy",
        "keyword": "softcover",
        "month_year_added": "April 2020",
        "id": 4
    }
]
```

You can now try fetching books using another property if you'd like to play around a bit more with this. This functionality allows you to efficiently search for and retrieve books based on specific criteria, making it easier to manage and organize your collection.

For more detailed information about Wordhoard and its other nifty features, check out our [documentation](/docs/index.md).

### Related resources

* [Adding a book](adding-a-book.md)
* [Listing all books in a collection](listing-all-books.md)
