API Documentation
---

## Endpoints that require Authentication

Closed endpoints require a valid `apikey` header to be included.

* [Bans](Documentation/bans.md)
* [Kicks](Documentation/kicks.md)
* [Warnings](Documentation/warns.md)
* [Broadcast](Documentation/broadcast.md)
* [Shutdown](Documentation/shutdown.md)

## Validate API key

Check if the current API key is valid.

**URL** : `GET /api/v1/validate`

**Auth required** : YES

### Success Response

**Code** : `200 OK`

**Content examples**

```json
{
    "status ": "success",
    "valid": true
}
```

# Error Codes
* 0 - No api-key specified
* 1 - Invalid api-key
* 2 - Bad Request, required field(s) not specified.
* 3 - Bad Request, invalid type specified.
* 4 - User not found
* 5 - User (not) already banned
* 500 - Internal Server Error
