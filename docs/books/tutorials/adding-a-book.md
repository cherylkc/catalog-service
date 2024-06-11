---
layout: page
---

# Tutorial: Adding a book to your collection

This tutorial shows you how to add a `book` to your Wordhoard collection. Once a `book` is added to your collection and tagged with properties such as `author`, `keyword`, or `genre`, you can retrieve that `book` from the collection using any of its associated properties.

For instance, if you’re at a bookstore browsing books by your favorite author and want to check if you own a particular book already, you can simply pull up Wordhoard, input the author’s name, and view all the books in your collection by the same author.

This tutorial assumes you’re familiar with web programming concepts and web data formats.

## Before you start

* Check to see if you have Postman installed on your system. If not, download the [Postman desktop app](https://www.postman.com/downloads/).
* Make sure you have the necessary information about the book you’d like to add i.e. title, author, keyword, and/or genre.
* Start the following server on your development system:

    ```shell
     cd <your-github-workspace>/catalog-service/api database
    json-server -w catalog-database.json
    ```

## Add a book to your collection

Adding a `book` to a collection involves sending a `POST` request with the details of the book.

1. Open the Postman desktop app.
2. Set your base url to `http://localhost:3000`
3. Create a new HTTP request with these values:

* **METHOD**: POST
* **URL**: `http://localhost:3000/books`
* **Headers**:
  * Key: Content-Type, Value: application/json
* **Request body**: You can modify the value of any property here.

```js
    {
        "user_id": 1,
        "title": "A Fine Balance",
        "author": "Rohinton Mistry",
        "genre": "historical fiction",
        "keyword": "post colonialism",
        "month_added: "July 2020",
        "id": 5
    }
```

1. Click **Send** to make the request.

You'll receive a response body that looks like this:

```js
{
    "user_id": 1,
    "title": "A Fine Balance",
    "author": "Rohinton Mistry",
    "genre": "historical fiction",
    "keyword": "post colonialism",
    "month_added: "July 2020",
    "id": 5
}
```

You have now successfully added a `book` to your Wordhoard collection! You can now try [retrieving this book](/docs/books/references/fetch-a-book-by-property.md) by any property to view the latest addition to your collection.

### Related resources

* [Fetching a book by property](/docs/books/references/fetch-a-book-by-property.md)
* Deleting a book
