# Broadcast

Send a message to all servers of your game

**URL** : `POST /api/v1/broadcast`

**Auth required** : YES

**Body:**
```json
{
    "message": String
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