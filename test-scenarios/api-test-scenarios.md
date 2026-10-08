
# API Test Scenarios

## API-SC-001 — Get All Posts

**Method:** GET

**Endpoint:** `/posts`

**Objective:** Verify that all posts can be retrieved.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response contains 100 posts.
- Posts contain required fields.

## API-SC-002 — Get Post By ID

**Method:** GET

**Endpoint:** `/posts/1`

**Objective:** Verify that a specific post can be retrieved by ID.

**Expected Result:**

- Status code is 200.
- Response is an object.
- Post ID is 1.
- Required fields exist.
- Title and body are not empty.

## API-SC-003 — Get Nonexistent Post

**Method:** GET

**Endpoint:** `/posts/9999`

**Objective:** Verify handling of a nonexistent post.

**Expected Result:**

- Status code is 404.
- Response body is an empty object.

## API-SC-004 — Create Post

**Method:** POST

**Endpoint:** `/posts`

**Objective:** Verify that a new post can be created.

**Expected Result:**

- Status code is 201.
- Submitted title is returned.
- Submitted body is returned.
- Correct userId is returned.
- Generated ID is returned.

## API-SC-005 — Update Post

**Method:** PUT

**Endpoint:** `/posts/1`

**Objective:** Verify complete update of an existing post.

**Expected Result:**

- Status code is 200.
- Post ID remains 1.
- Title is updated.
- Body is updated.
- User ID remains 1.

## API-SC-006 — Partial Update Post

**Method:** PATCH

**Endpoint:** `/posts/1`

**Objective:** Verify partial update of an existing post.

**Expected Result:**

- Status code is 200.
- Post ID remains 1.
- Title is updated.
- User ID is preserved.
- Body is preserved.

## API-SC-007 — Delete Post

**Method:** DELETE

**Endpoint:** `/posts/1`

**Objective:** Verify that an existing post can be deleted.

**Expected Result:**

- Status code is 200.
- Response is an object.
- Deleted post has ID 1.

## API-SC-008 — Get Post With Invalid ID

**Method:** GET

**Endpoint:** `/posts/abc`

**Objective:** Verify handling of an invalid post ID.

**Expected Result:**

- Status code is 404.
- Response body is an empty object.

## API-SC-009 — Filter Posts By User ID

**Method:** GET

**Endpoint:** `/posts?userId=1`

**Objective:** Verify filtering posts by user ID.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response is not empty.
- All posts have userId equal to 1.

## API-SC-010 — Filter Posts By Nonexistent User ID

**Method:** GET

**Endpoint:** `/posts?userId=999`

**Objective:** Verify filtering by a nonexistent user ID.

**Expected Result:**

- Status code is 200.
- Response is an array.
- Response is empty.
