## Comment Service

### 1. Add Comment

**Endpoint:** `POST /api/comments`

**Request:**
```json
{
  "postId": "60b4d2bc953b6c3c7b6e7c17",
  "userId": "1",
  "content": "This is a comment."
}
```

Response:
```json
{
  "id": "2",
  "postId": "60b4d2bc953b6c3c7b6e7c17",
  "userId": "1",
  "content": "This is a comment.",
  "createdAt": "2021-05-31T12:34:56Z",
  "updatedAt": "2021-05-31T12:34:56Z"
}
```

### 2. Get Comments for Post

**Endpoint:** `GET /api/posts/{postId}/comments`

Response:
```json
[
  {
    "id": "2",
    "postId": "60b4d2bc953b6c3c7b6e7c17",
    "userId": "1",
    "content": "This is a comment.",
    "createdAt": "2021-05-31T12:34:56Z",
    "updatedAt": "2021-05-31T12:34:56Z"
  }
]
```

### 3.  Delete Comment

**Endpoint:** `DELETE /api/posts/{postId}/comments`

**Request Body:** Empty

**Response:** Status `204 No Content`
