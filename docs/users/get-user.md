# Get Users

Endpoint to retrieve information about all users.

### Endpoint

`GET /api/users`

### Request

No request body is required.

### Response

-   **200 OK**:

    -   Content-Type: `application/json`
    -   Body:

```json
{
    "users": [
        {
            "uid": "string",
            "displayName": "string",
            "email": "string",
            "photoURL": "string",
            "provider": "string",
            "verified": true,
            "accessToken": "string",
            "posts": ["string"]
        }
    ]
}
```

-   **500 Internal Server Error**:
    -   Content-Type: `application/json`
    -   Body:
        ```json
        {
            "message": "server error",
            "error": "string"
        }
        ```

### Example

**Request:**

```http
GET /api/users

```

**Response:**

```json
{
    "users": [
        {
            "id": "utWnXnhpjPEINAuBjQVT",
            "photoURL": "https://lh3.googleusercontent.com/a/ACg8ocI_gZFdmdWJ_TG7OWLXtWKcB-qmxIBUmnHlDd3Db4XRAg=s96-c",
            "provider": "google",
            "displayName": "shigure yukikaze",
            "verified": true,
            "email": "shigurekawai@gmail.com",
            "posts": [
                "AQogY1wde8NfzlbHOLJP",
                "Bk0aoG76PfdOmPHYmw69",
                "qYyYK388dK5XDA473AfL"
            ]
        }
    ]
}
```

**Error Response:**

```json
{
    "message": "Something Error",
    "error": "Error message details"
}
```

