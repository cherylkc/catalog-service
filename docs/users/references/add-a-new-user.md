
# Adding a new user

Make a `POST` request to enroll a new [WordHoard](../../overview.md) `user`. This function is available only to those with WordHoard admin rights.

## URL

```shell
http://localhost:3000/users
```

## Method

POST

## Parameters

A new user record needs to have these properties:

| Property | Type | Description |
| -------------- | ------ | ------------ |
| `last_name` | string | User's last name |
| `first_name` | string | User's first name |
| `email` | string | User's email address |
| `id` | number | User's id |

> If you do not add an id, WordHoard will generate one for you.

## Request headers

Not required

## Request body

This example adds a new user named Amy Tan.

```js
{
    "last_name": "Tan",
    "first_name": "Amy",
    "email": "amy.tan@example.com",
    "id": "2"
}
```

## Response body

```js
{
    "last_name": "Tan",
    "first_name": "Amy",
    "email": "amy.tan@example.com",
    "id": "2"
}
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 201 | Created | User added successfully |
| 500 | Internal server error | Invalid JSON |
| ECONNREFUSED | N/A | The service is offline; restart the service and try again. |

### Related resources

* [Updating a user's profile](update-a-user-profile.md)
* [Deleting a user](delete-a-user.md)
