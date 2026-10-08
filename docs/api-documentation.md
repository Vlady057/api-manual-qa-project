# API Documentation

## 1. API Overview

This project uses the JSONPlaceholder REST API for manual API testing.

**Base URL:**
https://jsonplaceholder.typicode.com

**Resource:**
`/posts`

JSONPlaceholder is a fake REST API used for testing and prototyping.

POST, PUT, PATCH, and DELETE operations are simulated and do not permanently modify server-side data.

## 2. Post Object Structure

```json
# API Documentation

## 1. API Overview

This project uses the JSONPlaceholder REST API for manual API testing.

**Base URL:**  
https://jsonplaceholder.typicode.com

**Resource:**  
`/posts`

JSONPlaceholder is a fake REST API used for testing and prototyping.

POST, PUT, PATCH, and DELETE operations are simulated and do not permanently modify server-side data.

## 2. Post Object Structure

Example Post object:

    {
        "userId": 1,
        "id": 1,
        "title": "Example title",
        "body": "Example body"
    }

| Field | Type | Description |
|---|---|---|
| `userId` | Integer | ID of the user who owns the post |
| `id` | Integer | Unique post ID |
| `title` | String | Post title |
| `body` | String | Post content |

## 3. API Endpoints

### 3.1 GET - Get All Posts

**Method:** `GET`

**Endpoint:** `/posts`

**URL:** https://jsonplaceholder.typicode.com/posts

**Purpose:** Retrieve all available posts.

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Response is an array.
- Response contains 100 posts.
- First post contains the required fields.

### 3.2 GET - Get Post By ID

**Method:** `GET`

**Endpoint:** `/posts/1`

**URL:** https://jsonplaceholder.typicode.com/posts/1

**Purpose:** Retrieve a specific post by ID.

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Response is an object.
- Post ID is 1.
- Required fields are present.
- Title is not empty.
- Body is not empty.

### 3.3 GET - Get Nonexistent Post

**Method:** `GET`

**Endpoint:** `/posts/9999`

**URL:** https://jsonplaceholder.typicode.com/posts/9999

**Purpose:** Verify API behavior when requesting a nonexistent post.

**Expected Status Code:** `404 Not Found`

**Expected Response:**

    {}

**Validation:**
- Status code is 404.
- Response body is an empty object.

### 3.4 POST - Create Post

**Method:** `POST`

**Endpoint:** `/posts`

**URL:** https://jsonplaceholder.typicode.com/posts

**Purpose:** Verify that a new post can be created.

**Content-Type:** `application/json`

**Request Body:**

    {
        "title": "Manual QA API Test",
        "body": "Testing POST request in Postman",
        "userId": 1
    }

**Expected Status Code:** `201 Created`

**Validation:**
- Status code is 201.
- Response contains the submitted title.
- Response contains the submitted body.
- Response contains the correct userId.
- Response contains a generated ID.

### 3.5 PUT - Update Post

**Method:** `PUT`

**Endpoint:** `/posts/1`

**URL:** https://jsonplaceholder.typicode.com/posts/1

**Purpose:** Verify that an existing post can be completely updated.

**Content-Type:** `application/json`

**Request Body:**

    {
        "id": 1,
        "title": "Updated Manual QA Test",
        "body": "Post content was completely updated",
        "userId": 1
    }

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Post ID remains 1.
- Title is updated.
- Body is updated.
- User ID remains 1.

### 3.6 PATCH - Partial Update Post

**Method:** `PATCH`

**Endpoint:** `/posts/1`

**URL:** https://jsonplaceholder.typicode.com/posts/1

**Purpose:** Verify that an individual field of an existing post can be updated.

**Content-Type:** `application/json`

**Request Body:**

    {
        "title": "Partially Updated Title"
    }

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Post ID remains 1.
- Title is updated.
- User ID is preserved.
- Body is preserved.

### 3.7 DELETE - Delete Post

**Method:** `DELETE`

**Endpoint:** `/posts/1`

**URL:** https://jsonplaceholder.typicode.com/posts/1

**Purpose:** Verify that an existing post can be deleted.

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Response is an object.
- Deleted post has ID 1.

### 3.8 GET - Get Post With Invalid ID

**Method:** `GET`

**Endpoint:** `/posts/abc`

**URL:** https://jsonplaceholder.typicode.com/posts/abc

**Purpose:** Verify API behavior when an invalid post ID is provided.

**Expected Status Code:** `404 Not Found`

**Expected Response:**

    {}

**Validation:**
- Status code is 404.
- Response body is an empty object.

### 3.9 GET - Filter Posts By User ID

**Method:** `GET`

**Endpoint:** `/posts?userId=1`

**URL:** https://jsonplaceholder.typicode.com/posts?userId=1

**Purpose:** Verify that posts can be filtered by user ID.

**Expected Status Code:** `200 OK`

**Validation:**
- Status code is 200.
- Response is an array.
- Response is not empty.
- All returned posts have `userId` equal to 1.

### 3.10 GET - Filter Posts By Nonexistent User ID

**Method:** `GET`

**Endpoint:** `/posts?userId=999`

**URL:** https://jsonplaceholder.typicode.com/posts?userId=999

**Purpose:** Verify API behavior when filtering by a user ID that has no posts.

**Expected Status Code:** `200 OK`

**Expected Response:**

    []

**Validation:**
- Status code is 200.
- Response is an array.
- Response is empty.

## 4. HTTP Methods

| Method | Purpose |
|---|---|
| GET | Retrieve data |
| POST | Create a resource |
| PUT | Completely update a resource |
| PATCH | Partially update a resource |
| DELETE | Delete a resource |

## 5. HTTP Status Codes Tested

| Status Code | Meaning |
|---|---|
| 200 | OK |
| 201 | Created |
| 404 | Not Found |

## 6. Test Results

Total API requests tested: **10**

Total assertions executed: **38**

| Result | Count |
|---|---:|
| Passed | 38 |
| Failed | 0 |

**Overall Result: PASS**
```
