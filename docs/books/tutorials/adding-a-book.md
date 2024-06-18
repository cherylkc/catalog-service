---
layout: page
---

# Tutorial: Adding a book to your collection

This tutorial shows you how to add a `book` to your [WordHoard](./overview.md) collection. Once a `book` is added to your collection and tagged with properties such as `author`, `keyword`, or `genre`, you can retrieve that `book` from the collection using any of its associated properties.

For instance, if you’re at a bookstore browsing books by your favorite author and want to check if you own a particular book already, you can simply pull up WordHoard, input the author’s name, and view all the books in your collection by the same author.

This tutorial assumes you’re familiar with web programming concepts and web data formats.

## Before you start

* Check to see if you have the following on your system:
  * A [GitHub](https://github.com/) account, [GitHub Desktop](https://desktop.github.com/), and a fork of the [WordHoard repository](https://github.com/cherylkc/catalog-service.git) cloned to your desktop
  * [Node.js](https://nodejs.org/en/download/package-manager)
  * [json-server](https://www.npmjs.com/package/json-server)
  * [Postman’s desktop app](https://www.postman.com/downloads/)
  * Command Prompt (Windows) or Terminal (macOS)

* Make sure you have the necessary information about the book you’d like to add i.e. title, author, keyword, and/or genre.
* Open [GitHub Desktop](https://desktop.github.com/) and make sure the current repository is **catalog-service**.
  * Create a new test branch.
  * Go to **Repository > Open in Command Prompt**.
  * In the Command Prompt window that pops up, run `cd api database`
  * Now run the command `json-server -w catalog-database.json`

The service should now be ready for your HTTP requests.

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
        "keyword": "postcolonialism",
        "month_added: "July 2020",
        "id": 5
    }
```

Click **Send** to make the request.

You'll receive a response body that looks like this:

```js
{
    "user_id": 1,
    "title": "A Fine Balance",
    "author": "Rohinton Mistry",
    "genre": "historical fiction",
    "keyword": "postcolonialism",
    "month_added: "July 2020",
    "id": 5
}
```

You have now successfully added a `book` to your WordHoard collection! You can now try [retrieving this book](/docs/books/references/fetch-a-book-by-property.md) by any property to view the latest addition to your collection.

### Related resources

* [Fetching a book by property](fetching-a-book-by-property.md)
* [Deleting a book](../references/delete-a-book.md)
