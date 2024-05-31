Users Table

```sql
CREATE TABLE users (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    bio TEXT,
    image_url VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

Comments Table

```sql
CREATE TABLE comments (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    post_id VARCHAR(24) NOT NULL,  -- Corresponds to MongoDB ObjectId
    user_id BIGINT NOT NULL,
    content TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

Claps Table
```sql
CREATE TABLE claps (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    post_id VARCHAR(24) NOT NULL,  -- Corresponds to MongoDB ObjectId
    user_id BIGINT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

Followers Table
```sql
CREATE TABLE followers (
    user_id BIGINT NOT NULL,
    follower_id BIGINT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY (user_id, follower_id),
    FOREIGN KEY (user_id) REFERENCES users(id),
    FOREIGN KEY (follower_id) REFERENCES users(id)
);
```

MongoDB Schemas
Posts Collection
```sql
{
  "_id": ObjectId("60b4d2bc953b6c3c7b6e7c17"),
  "title": "My First Blog Post",
  "content": "This is the content of the blog post.",
  "authorId": "60b4d2bc953b6c3c7b6e7c16",
  "tags": ["springboot", "java", "blog"],
  "createdAt": ISODate("2021-05-31T12:34:56Z"),
  "updatedAt": ISODate("2021-05-31T12:34:56Z")
}
```











