
# Deleting a user

Use a `DELETE` request to delete a user from a [WordHoard](../../overview.md) account. This feature is available only to those with WordHoard admin rights.

## URL

```shell

http://localhost:3000/users/{id}

```

## Method

DELETE

## Request headers

Not required

## Request body

Not required

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
| 200 | Success | User deleted successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
