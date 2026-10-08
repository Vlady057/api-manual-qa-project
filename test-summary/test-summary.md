
# API Test Summary

## 1. Project Information

**Project:** API Manual QA Project

**API:** JSONPlaceholder

**Base URL:** https://jsonplaceholder.typicode.com

**Resource:** `/posts`

**Tool:** Postman

**Testing Type:** Manual API Testing

**Author:** Volodymyr

## 2. Test Execution Summary

A total of 10 API requests were tested.

The test suite covered:

- GET
- POST
- PUT
- PATCH
- DELETE
- CRUD operations
- Filtering
- Positive scenarios
- Negative scenarios
- HTTP status validation
- Response structure validation
- Response data validation

## 3. Requests Tested

| ID | Request                                   | Result |
| -- | ----------------------------------------- | ------ |
| 1  | GET - Get All Posts                       | Passed |
| 2  | GET - Get Post By ID                      | Passed |
| 3  | GET - Get Nonexistent Post                | Passed |
| 4  | POST - Create Post                        | Passed |
| 5  | PUT - Update Post                         | Passed |
| 6  | PATCH - Partial Update Post               | Passed |
| 7  | DELETE - Delete Post                      | Passed |
| 8  | GET - Get Post With Invalid ID            | Passed |
| 9  | GET - Filter Posts By User ID             | Passed |
| 10 | GET - Filter Posts By Nonexistent User ID | Passed |

## 4. Test Statistics

| Metric       | Result |
| ------------ | -----: |
| API Requests |     10 |
| Assertions   |     38 |
| Passed       |     38 |
| Failed       |      0 |
| Blocked      |      0 |
| Pass Rate    |   100% |

## 5. Tested Functionality

### GET

- Retrieve all posts.
- Retrieve post by ID.
- Handle nonexistent post.
- Handle invalid post ID.
- Filter posts by user ID.
- Handle empty filter result.

### POST

- Create a new post.
- Validate submitted data.
- Validate generated ID.

### PUT

- Completely update a post.
- Validate updated fields.

### PATCH

- Partially update a post.
- Validate updated field.
- Validate preserved fields.

### DELETE

- Delete a post.
- Validate response object.
- Validate post ID.

## 6. Defects

No defects were identified during testing.

The 404 responses for nonexistent and invalid resources were expected behavior and were not reported as defects.

## 7. Limitations

JSONPlaceholder is a mock API.

POST, PUT, PATCH, and DELETE operations are simulated and do not permanently modify server-side data.

Database persistence is therefore outside the scope of this project.

## 8. Final Result

**TEST STATUS: PASSED**

All 10 planned requests were executed successfully.

All 38 Postman assertions passed.

No failed tests or unresolved defects remained at the end of testing.
