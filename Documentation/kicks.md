# Kick User

Kicks the specified user from the game

**URL** : `POST /api/v1/kick `

**Auth required** : YES

**Body:**
```json
{
    "user": Number,
    "reason": String,
    "type": String,
    "data": Object
}
```
## Success Response

**Code** : `200 OK`

**Content examples**

```json
{
    "status ": "success"
}
```