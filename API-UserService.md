## User Service

### 1. Register User

**Endpoint:** `POST /api/users/register`

**Request:**
```json
{
  "username": "john_doe",
  "password": "secure_password",
  "email": "john.doe@example.com",
  "bio": "This is John's bio.",
  "imageUrl": "http://example.com/profile.jpg"
}
```

Response:
```json
{
  "id": 1,
  "username": "john_doe",
  "email": "john.doe@example.com",
  "bio": "This is John's bio.",
  "imageUrl": "http://example.com/profile.jpg",
  "createdAt": "2021-05-31T12:34:56Z",
  "updatedAt": "2021-05-31T12:34:56Z"
}
```

### 2. Login User

**Endpoint:** `POST /api/users/login`

**Request:**
```json
{
  "username": "john_doe",
  "password": "secure_password"
}
```

Response:
```json
{
  "token": "jwt_token_here"
}
```

### 3. Get User Profile

**Endpoint:** `POST /api/users/{userId}`

Response:
```json
{
  "title": "My First Blog Post",
  "content": "This is the content of the blog post.",
  "authorId": "1",
  "tags": ["springboot", "java", "blog"]
}
```

### 4. Follow User

**Endpoint:** `POST /api/users/{userId}/follow`

**Request Body:** Empty

**Response:** Status `204 No Content`

### 5. Unfollow User

**Endpoint:** `DELETE /api/users/{userId}/follow`

**Request Body:** Empty

**Response:** Status `204 No Content`
