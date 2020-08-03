# Warn User

Warns the specified user

**URL** : `POST /api/v1/warn`

**Auth required** : YES

**Body:**
```json
{
    "user": Number,
    "content": String
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