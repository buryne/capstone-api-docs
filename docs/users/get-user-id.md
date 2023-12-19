## **GET BY ID**

Endpoint to retrieve information about a specific post.

### Endpoint

```http
GET /api/users/:id
```

-   Replace `:id` with the actual post ID.

### Request

-   Request parameters:
    -   `id` (string): ID of the post to retrieve.

### Response

-   **200 OK**:

    -   Content-Type: `application/json`
    -   Body:
        ```json
        {
            "id": "utWnXnhpjPEINAuBjQVT",
            "uid": "118235995435385156808",
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
        ```

-   **404 Not Found**:
    -   Content-Type: `application/json`
    -   Body:
        ```json
        {
            "message": "Not found User"
        }
        ```

### Example

**Request:**

Some code with the `http` at the start:

```http
GET /api/posts/07r719qaQoFIb3L2T5LN
```

**Response:**

```json
{
    "id": "07r719qaQoFIb3L2T5LN",
    "uid": "118235995435385156808",
    "title": "Ancol",
    "location": "Jakarta Pusat, Jakarta",
    "caption": "Monas at night",
    "image": "https://storage.googleapis.com/percobaan-dulu-2e8d8.appspot.com/images/1701440700536_marc-x-ducati.jpeg",
    "tags": ["awesome", "cool", "jakarta"],
    "create_at": {
        "_seconds": 1701440700,
        "_nanoseconds": 536000000
    },
    "updateAt": {
        "_seconds": 1702051375,
        "_nanoseconds": 761000000
    }
}
```
