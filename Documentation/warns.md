# Warn User

Warns the specified user

**URL** : `POST /api/v1/warns/add`

**Auth required** : YES

**Body:**
```json
{
    "user": Number,
    "content": String,
    "adminid": Optional String
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

# Remove Warning

Removes a warning by id

**URL** : `POST /api/v1/warns/remove`

**Auth required** : YES

**Body:**
```json
{
    "id": Number
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

# List Warnings

List a player's warnings

**URL** : `POST /api/v1/warns/list`

**Auth required** : YES

**Body:**
```json
{
    "user": Number
}
```
## Success Response

**Code** : `200 OK`

**Content examples**

```json
{
    "status ": "success",
    "data": []
}
```

```json
{
    "status": "success",
    "data":[
        {"id": 18, "userId": 1, "content": "test", "timestamp": "2020-08-17T15:14:31.607Z", "adminid": "281218998203580426"}
    ]
}```