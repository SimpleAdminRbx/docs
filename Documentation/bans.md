# Get Ban

Get the details if someone is currently banned on a certain API key.

**URL** : `GET /api/v1/bans?user=id`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples**

For the ID 2482 sent.

```json
{
    "status ": "success",
    "id": 2482,
    "banned": true,
    "reason": "this is a reason for the ban",
    "start": "2020-07-19T21:19:04Z",
    "end": "2020-07-21T21:19:04Z"

}
```

For the ID 21898128 sent.

```json
{
    "status": "success",
    "id": 21898128,
    "banned": false
}
```

# Get Ban List

Gets a list of every active ban

**URL** : `GET /api/v1/bans/list`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples**

```json

    "status": "success",
    "data": [{
            "id": 25,
            "userId": 23665982,
            "reason": "test",
            "timestamp": {
                "start": "2020-07-28T15:15:13.715Z",
                "end": "2020-08-07T15:15:13.715Z"
            }
        },
        {
            "id": 26,
            "userId": 316145082,
            "reason": "test",
            "timestamp": {
                "start": "2020-07-28T15:15:18.300Z",
                "end": "2320-01-01T00:00:00.000Z"
            }
        }
    ]
}
```
# Add Ban

Bans a user

**URL** : `POST /api/v1/bans/add`

**Auth required** : YES

**Body:**
```json
{
    "user": Number,
    "length": String (xs, xm, xh, xd, xm, xy),
    "reason": String (Optional),
    "admin": String (Optional)
}
```
## Success Response

**Code** : `200 OK`

**Content examples**

For the ID 316145082 sent with 30d and the reason "bruheo".

```json
{
    "status": "success",
    "data":{
        "userId": 316145082,
        "username": "Ulferno",
        "length":{
            "fullLength": "30 days",
            "msLength": 2592000000
        },
        "timestamp":{
            "start": "2020-07-28T01:08:49.926Z",
            "end": "2020-08-27T01:08:49.926Z"
        },
        "reason": "bruheo",
        "admin": "NO_ADMIN_PROVIDED"
    }

}
```

## Notes

* The end time will be 2320-01-01T00:00:00.000Z if the ban never expires

# Unban

Removes the active ban of a user

**URL** : `POST /api/v1/bans/unban`

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

For the ID 316145082 sent.

```json
{
    "status": "success",
    "data": {
        "username": "Ulferno",
        "id": 316145082
    }
}
```