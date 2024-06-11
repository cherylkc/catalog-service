
# Getting started with Wordhoard

Welcome to [Wordhoard](overview.md)! This tutorial will walk you through the basics of getting started with Wordhoard, including set-up, key features, and making your first API call.

## What is Wordhoard

Wordhoard is a powerful API that enables you to create and maintain a record of your books. You can search for and retrieve books by various properties at any time, ensuring that you never buy the same book twice (unless you really want to, of course).

With Wordhoard, you can:

* Look up books by title, author, genre, keyword, or month added, while making purchasing decisions or recommending books to a friend
* Add, modify, or delete books in your book collection to keep it up to date
* Add, update, or delete users in your account (admin only).

## Setting up

These are the prerequisites for exploring Wordhoard:

* A [GitHub](https://github.com/) account, [GitHub Desktop](https://desktop.github.com/), and a fork of the [Wordhoard repository](https://github.com/cherylkc/catalog-service.git) cloned to your desktop
* [Node.js](https://nodejs.org/en/download/package-manager)
* [json-server](https://www.npmjs.com/package/json-server)
* [Postman’s Desktop app](https://www.postman.com/downloads/)
* Command Prompt (Windows) or Terminal (macOS)

> You do not need an API key to try Wordhoard out.

When you have all the prerequisites sorted, start the server on your development system:

* Open [GitHub Desktop](https://desktop.github.com/) and make sure the current repository is **catalog-service**.
* Create a new test branch.
* Go to **Repository > Open in Command Prompt**.
* In the Command Prompt window that pops up, run `cd api database`
* Now run the command `json-server -w catalog-database.json`

The service should now be up and running.

## Endpoints supported by Wordhoard

| HTTP Method | Endpoint                           |
|-------------|------------------------------------|
| GET         | List all the books in your collection  |
| GET         | List all the users in your service |
| GET         | Retrieve a book by any property        |
| CREATE      | Add a new book to a collection     |
| CREATE      | Create a new user                  |
| PATCH       | Modify a user’s details            |
| PATCH       | Modify a book’s details            |
| DELETE      | Delete a book from a collection    |

## Making your first API call - view all books in a user’s collection

Let’s assume you’re a Wordhoard user who wants to take a quick look at all the books in their collection.

* Open the Postman desktop app and click **+** to create a new HTTP request.
* Make sure the **GET** method is selected in the dropdown, then paste `http://localhost:3000/books` in the URL box.
* Click **Send** to send the request to the API server.

You'll see the following response in the response pane.

```shell
[
    {
        "user_id": 1,
        "title": "The IBM Style Guide",
        "author": "Francis DeRespinis",
        "genre": "Style Guide",
        "keyword": "technical writing",
        "month_added": "April 2023",
        "id": "1"
    },
    {
        "user_id": 1,
        "title": "Going Postal",
        "author": "Terry Pratchett",
        "genre": "Fantasy",
        "keyword": "Discworld",
        "month_added": "December 2023",
        "id": "2"
    },
    {
        "user_id": 1,
        "title": "What if? 2: Additional Serious Scientific Answers to Absurd Hypothetical Questions",
        "author": "Randall Munroe",
        "genre": "Nonfiction",
        "keyword": "popular science",
        "month_added": "April 2020",
        "id": "3"
    },
    {
        "user_id": 1,
        "title": "At the Feet of the Sun",
        "author": "Victoria Goddard",
        "genre": "Fantasy",
        "keyword": "softcover",
        "month_added": "April 2020",
        "id": "4"
    }
]
```

Congratulations! You have just made your first API call to Wordhoard!

## What’s next

With your Wordhoard API set up and ready to go, you could now try [adding a new book](books/tutorials/adding-a-book.md) to the collection, or [retrieving a book](books/references/fetch-a-book-by-property.md) using any of its properties. For more detailed information about Wordhoard and its other nifty features, check out our [documentation](index.md).