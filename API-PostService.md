## Post Service

### 1. Create Post

**Endpoint:** `POST /api/posts`

**Request:**
```json
{
  "title": "My First Blog Post",
  "content": "This is the content of the blog post.",
  "authorId": "1",
  "tags": ["springboot", "java", "blog"]
}
```

Response:
```json
{
  "id": "60b4d2bc953b6c3c7b6e7c17",
  "title": "My First Blog Post",
  "content": "This is the content of the blog post.",
  "authorId": "1",
  "tags": ["springboot", "java", "blog"],
  "createdAt": "2021-05-31T12:34:56Z",
  "updatedAt": "2021-05-31T12:34:56Z"
}
```

### 2. Get Post

**Endpoint:** `GET /api/posts/{postId}`

Response:
```json
{
  "id": "60b4d2bc953b6c3c7b6e7c17",
  "title": "My First Blog Post",
  "content": "This is the content of the blog post.",
  "authorId": "1",
  "tags": ["springboot", "java", "blog"],
  "createdAt": "2021-05-31T12:34:56Z",
  "updatedAt": "2021-05-31T12:34:56Z"
}
```

### 3. Update Post

**Endpoint:** `PUT /api/posts/{postId}`

Request:
```json
{
  "title": "Updated Blog Post Title",
  "content": "This is the updated content of the blog post.",
  "tags": ["springboot", "java", "blog"]
}
```

Response:
```json
{
  "id": "60b4d2bc953b6c3c7b6e7c17",
  "title": "Updated Blog Post Title",
  "content": "This is the updated content of the blog post.",
  "authorId": "1",
  "tags": ["springboot", "java", "blog"],
  "createdAt": "2021-05-31T12:34:56Z",
  "updatedAt": "2021-06-01T12:34:56Z"
}
```

### 4. Delete Post

**Endpoint:** `DELETE /api/posts/{postId}`

**Request Body:** Empty

**Response:** Status `204 No Content`

### 5. List Posts

**Endpoint:** `GET /api/posts`
Query Parameters: `page`, `size`, `authorId`, `tag`

**Request Body:** Empty

**Response:** 
```json
[
  {
    "id": "60b4d2bc953b6c3c7b6e7c17",
    "title": "My First Blog Post",
    "content": "This is the content of the blog post.",
    "authorId": "1",
    "tags": ["springboot", "java", "blog"],
    "createdAt": "2021-05-31T12:34:56Z",
    "updatedAt": "2021-05-31T12:34:56Z"
  }
]
```
