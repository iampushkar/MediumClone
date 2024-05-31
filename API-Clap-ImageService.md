## Clap Service or Like Service

### 1. Clap for Post

**Endpoint:** `POST /api/posts/{postId}/clap`

**Request:**
EMPTY

Response: Status 204 No Content

### 2. Get Claps for Post

**Endpoint:** `GET /api/posts/{postId}/claps`

Response:
```json
{
  "clapCount": 10
}
```

## Image Service

### 1. Upload Image
**Endpoint:** `POST /api/images/upload`

**Request:**
multipart/form-data with file field

Response:
```json
{
  "imageUrl": "https://s3.amazonaws.com/yourbucketname/filename.jpg"
}
```

### 2. Delete Image

**Endpoint:** `DELETE /api/images`

**Request:**
```json
{
  "imageUrl": "https://s3.amazonaws.com/yourbucketname/filename.jpg"
}
```

Response: Status 204 No Content
