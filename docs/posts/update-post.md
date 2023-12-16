## **UPDATE**

Endpoint to update an existing post. Only the user who created the post can update it.

### Endpoint

`PUT /api/posts/:id`

-   Replace `:id` with the actual post ID.

### Request

-   **Headers**:
    -   Content-Type: `multipart/form-data`
-   **Parameters**:

    -   `id`: The ID of the post to be updated.

-   **Body**: (at least one of the following)

    -   `title` (_`string`_): Updated title of the post.
    -   `location` (_`string`_): Updated location information for the post.
    -   `caption` (_`string`_): Updated caption for the post.
    -   `tags` (_`array(string)`_): Updated comma-separated tags for the post.
    -   `image`(_`file`_): Update image file to be uploaded.

### Response

-   **200 OK**:

    -   Content-Type: `application/json`
    -   Body:

        ```json
        {
            "message": "Post updated successfully."
        }
        ```

-   **403 Forbidden**:

    -   Content-Type: `application/json`
    -   Body:

        ```json
        {
            "error": "You do not have permission to edit this post."
        }
        ```

-   **404 Not Found**:

    -   Content-Type: `application/json`
    -   Body:

        ```json
        {
            "error": "Post not found."
        }
        ```

-   **500 Internal Server Error**:

    -   Content-Type: `application/json`
    -   Body:

        ```json
        {
            "error": "Trouble server side"
        }
        ```

### Examples

#### 200 OK

**Response:**

```json
{
    "message": "Post updated successfully."
}
```

### Example

**Request:**

```http
PUT /api/posts/07r719qaQoFIb3L2T5LN
Content-Type: multipart/form-data

title: Updated Title
caption: Updated Caption
location: Updated Location
tags: updated, tags
file: [binary data]
```
