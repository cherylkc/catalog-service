
# `user` resource

Base endpoint:

```shell
{server_url}/users
```

Contains information about the users of the WordHoard service.

To have a book in the service, the user must first be added to the service by admin.

## Resource properties

Sample `user` resource

```js
{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "f.smith@example.com",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `last_name` | string | The user's last name |
| `first_name` | string | The user's first name |
| `email` | string | The user's email address |
| `id` | number | The user's unique ID |

## Operations

The `user` resource supports the following operations:

### CREATE (POST)

* Create a user (admin only)

### UPDATE (PATCH)

* [Update a user's profile](docs/users/references/update-a-user-profile.md) (first name, last name, or email)

### DELETE

* [Delete a user](docs/users/references/delete-a-user.md) (admin only)
