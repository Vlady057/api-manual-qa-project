
# API Test Cases

## TC-001 — Get All Posts

**Method:** GET

**Endpoint:** `/posts`

**Precondition:** API is available.

**Steps:**

1. Send GET request to `/posts`.
2. Verify response status.
3. Verify response type.
4. Verify number of posts.
5. Verify required fields.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response contains 100 posts.
- First post contains required fields.

**Actual Result:** Passed.

---

## TC-002 — Get Post By ID

**Method:** GET

**Endpoint:** `/posts/1`

**Steps:**

1. Send GET request to `/posts/1`.
2. Verify response status.
3. Verify response type.
4. Verify post ID.
5. Verify required fields.
6. Verify title and body.

**Expected Result:**

- Status code is 200.
- Response is an object.
- Post ID is 1.
- Required fields exist.
- Title and body are not empty.

**Actual Result:** Passed.

---

## TC-003 — Get Nonexistent Post

**Method:** GET

**Endpoint:** `/posts/9999`

**Steps:**

1. Send GET request.
2. Verify response status.
3. Verify response body.

**Expected Result:**

- Status code is 404.
- Response body is an empty object.

**Actual Result:** Passed.

---

## TC-004 — Create Post

**Method:** POST

**Endpoint:** `/posts`

**Request Body:**

    {
        "title": "Manual QA API Test",
        "body": "Testing POST request in Postman",
        "userId": 1
    }

**Steps:**

1. Send POST request.
2. Verify response status.
3. Verify title.
4. Verify body.
5. Verify userId.
6. Verify generated ID.

**Expected Result:**

- Status code is 201.
- Submitted data is returned.
- Generated ID is present.

**Actual Result:** Passed.

---

## TC-005 — Update Post

**Method:** PUT

**Endpoint:** `/posts/1`

**Request Body:**

    {
        "id": 1,
        "title": "Updated Manual QA Test",
        "body": "Post content was completely updated",
        "userId": 1
    }

**Steps:**

1. Send PUT request.
2. Verify response status.
3. Verify post ID.
4. Verify updated title.
5. Verify updated body.
6. Verify userId.

**Expected Result:**

- Status code is 200.
- Post ID remains 1.
- Title is updated.
- Body is updated.
- User ID remains 1.

**Actual Result:** Passed.

---

## TC-006 — Partial Update Post

**Method:** PATCH

**Endpoint:** `/posts/1`

**Request Body:**

    {
        "title": "Partially Updated Title"
    }

**Steps:**

1. Send PATCH request.
2. Verify response status.
3. Verify post ID.
4. Verify updated title.
5. Verify preserved userId.
6. Verify preserved body.

**Expected Result:**

- Status code is 200.
- Title is updated.
- Post ID remains 1.
- User ID is preserved.
- Body is preserved.

**Actual Result:** Passed.

---

## TC-007 — Delete Post

**Method:** DELETE

**Endpoint:** `/posts/1`

**Steps:**

1. Send DELETE request.
2. Verify response status.
3. Verify response type.
4. Verify post ID.

**Expected Result:**

- Status code is 200.
- Response is an object.
- Deleted post ID is 1.

**Actual Result:** Passed.

---

## TC-008 — Get Post With Invalid ID

**Method:** GET

**Endpoint:** `/posts/abc`

**Steps:**

1. Send GET request.
2. Verify response status.
3. Verify response body.

**Expected Result:**

- Status code is 404.
- Response body is an empty object.

**Actual Result:** Passed.

---

## TC-009 — Filter Posts By User ID

**Method:** GET

**Endpoint:** `/posts?userId=1`

**Steps:**

1. Send GET request.
2. Verify response status.
3. Verify response type.
4. Verify response is not empty.
5. Verify userId values.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response is not empty.
- All returned posts have userId equal to 1.

**Actual Result:** Passed.

---

## TC-010 — Filter Posts By Nonexistent User ID

**Method:** GET

**Endpoint:** `/posts?userId=999`

**Steps:**

1. Send GET request.
2. Verify response status.
3. Verify response type.
4. Verify response contents.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response is empty.

**Actual Result:** Passed.
