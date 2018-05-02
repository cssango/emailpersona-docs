# Profile

This method retrives the name and profile photo for the email provided and returns the information in JSON.

You will make a GET request to this endpoint:

```
[GET] https://api.emailpersona.net/profile/{email}?api_token={token}
```

## Example Successful Result:

```json
{
    "success": true,
    "source": "gravatar",
    "name": "Jon Snow",
    "profile_image": "https://www.gravatar.com/avatar/cfe42a7258a028d9c921be5429782f8b"
}
```

## Returned Values
| Key | Description |
| --- | ----------- |
| `success` | indicates if request was successful or not |
| `source` | `gravatar` or `googleplus`  |
| `name` | Name associated with the email provided |
| `profile_image` | URL to a profile thumbnail photo (128x128).  |


## Example Unsuccessful Result

```json
{
    "success": false,
    "error_message": "User not found"
}
```
