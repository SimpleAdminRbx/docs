# Shutdown all servers

Kicks everyone from every server of your game

**URL** : `POST /api/v1/shutdown`

**Auth required** : YES

**Body:**
```json
{
    "reason": String
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