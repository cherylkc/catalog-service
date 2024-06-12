---
layout: page
---

# Updating a user's profile

Use a `PATCH` request to update a user's last name, first name, or email.

## URL

```shell

http://localhost:3000/users/{id}

```

## Method

PATCH

## Parameters

The following user properties can be updated.

| Property | Type | Description |
| -------------- | ------ | ------------ |
| `last_name` | string | User's last name |
| `first_name` | string | User's first name |
| `email` | string | User's email address |

## Request headers

Not required

## Request body

This example updates the user's email address from `f.smith@example.com` to `ferdinand.smith@example.com`.

```js
{
    "email": "ferdinand.smith@example.com"
}
```

## Response body

```js
{
    "last_name": "Smith",
    "first_name": "Ferdinand",
    "email": "ferdinand.smith@example.com",
    "id": 1
}
```

## Response status

| Status value | Return status | Description |
| ------------ | ------------- | ----------- |
| 200 | Success | Requested user property updated successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
