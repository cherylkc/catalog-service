
# Tutorial: Updating a user's profile

This tutorial shows you how to modify a WordHoard user's last name, first name, or email by sending a `PATCH` request to the service.

These are the properties you can update in a user's profile:

| Property | Type | Description |
| ---- | ---- | ----------- |
| `last_name` | string | User's last name |
| `first_name` | string | User's first name |
| `email` | string | User's email address |

## Before you start

* Make sure you have the following on your system:
  * A [GitHub](https://github.com/) account, [GitHub Desktop](https://desktop.github.com/), and a fork of the [Wordhoard repository](https://github.com/cherylkc/catalog-service.git) cloned to your desktop
  * [Node.js](https://nodejs.org/en/download/package-manager) and [json-server](https://www.npmjs.com/package/json-server)
  * [Postman’s desktop app](https://www.postman.com/downloads/)
  * Command Prompt (Windows) or Terminal (macOS)

* Open [GitHub Desktop](https://desktop.github.com/) and make sure the current repository is **catalog-service**.
  * Create a new test branch.
  * Go to **Repository > Open in Command Prompt**.
  * In the Command Prompt window, run `cd api database`
  * Now run the command `json-server -w catalog-database.json`

Your service is now ready for HTTP requests.

## Updating a user's profile

To update a property in a user profile, send a `PATCH` request to the service. This example updates a user’s last name from 'Smith' to 'Magellan'.

1. Open the Postman desktop app.
2. Create a new HTTP request with these values:

* **Method**: PATCH
* **URL**: `http://localhost:3000/users/{id}`
* **Query params**: None
* **Headers** (optional):
  * Key: Content-Type
  * Value: application/json
* **Request body**:

```js
{
    "last_name": "Magellan"
}
```

Click **Send** to make the request.

A successful request will return a response body that looks like this:

```js
{
    "last_name": "Magellan",
    "first_name": "Ferdinand",
    "email": "ferdinand.smith@example.com",
    "id": 1
}
```

You have now successfully updated a user's profile.

### Related resources

* [Adding a new user](../references/add-a-new-user.md)
* [Deleting a user](../references/delete-a-user.md)
