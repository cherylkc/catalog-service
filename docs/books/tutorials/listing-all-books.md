---
layout: page
---

# Tutorial: Listing all the books in a collection

This tutorial shows you how to retrieve all the `books` in your Wordhoard collection. It assumes you’re familiar with web programming concepts and web data formats.

## Before you start

* Check to see if you have the following on your system:
  * A [GitHub](https://github.com/) account, [GitHub Desktop](https://desktop.github.com/), and a fork of the [Wordhoard repository](https://github.com/cherylkc/catalog-service.git) cloned to your desktop
  * [Node.js](https://nodejs.org/en/download/package-manager)
  * [json-server](https://www.npmjs.com/package/json-server)
  * [Postman’s Desktop app](https://www.postman.com/downloads/)
  * Command Prompt (Windows) or Terminal (macOS)

* Open [GitHub Desktop](https://desktop.github.com/) and make sure the current repository is **catalog-service**.
  * Create a new test branch.
  * Go to **Repository > Open in Command Prompt**.
  * In the Command Prompt window that pops up, run `cd api database`
  * Now run the command `json-server -w catalog-database.json`

The service should now be ready for your HTTP requests.

## Listing all the books in your collection

Retrieving a list of the `books` in your collection involves sending a `GET` request to the service.

1. Open the Postman desktop app.
2. Set your base url to `http://localhost:3000`
3. Create a new HTTP request with these values:

* **METHOD**: GET
* **URL**: `http://localhost:3000/books`
* **Headers**:
  * Key: Content-Type, Value: application/json
* **Request body**: None

Click **Send** to make the request.

You should receive a response body that looks like this:

```js
[
    {
        "user_id": 1,
        "title": "The IBM Style Guide",
        "author": "Francis DeRespinis",
        "genre": "Style Guide",
        "keyword": "technical writing",
        "month_year_added": "April 2023",
        "id": 1
    },
    {
        "user_id": 1,
        "title": "Going Postal",
        "author": "Terry Pratchett",
        "genre": "Fantasy",
        "keyword": "Discworld",
        "mmonth_year_added": "December 2023",
        "id": 2
    },
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

You have now successfully retrieved all the `books` in your Wordhoard collection! Explore Wordhoard further and try [fetching a book using any property](/docs/books/references/fetch-a-book-by-property.md).

### Related resources

* [Fetching a book by property](/docs/books/references/fetch-a-book-by-property.md)
* Updating a book
* Deleting a book
