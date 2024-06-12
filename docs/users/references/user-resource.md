---
layout: page
---
# `user` resource

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the Wordhoard service.

To have a book in the service, the user must first be added to the service by admin.

## Resource properties

Sample `user` resource

```js
{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "user_id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `user_id` | number | The user's unique ID |

## Operations

The `user` resource supports the following operations:

### READ (GET)

* Get all users (admin only)

### CREATE (POST)

* Create a user (admin only)

### UPDATE (PUT/PATCH)

* Update a user's profile (first name, last name, or email)

### DELETE

* Delete a user (admin only)
