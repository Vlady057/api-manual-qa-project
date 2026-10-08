
# API Test Plan

## 1. Project Information

**Project:** API Manual QA Project

**API:** JSONPlaceholder

**Base URL:** https://jsonplaceholder.typicode.com

**Resource:** `/posts`

**Testing Tool:** Postman

**Testing Type:** Manual API Testing

**Author:** Volodymyr

## 2. Test Objective

The objective is to verify the functionality, response structure, status codes, request data, and error handling of the `/posts` REST API.

The project covers CRUD operations and filtering functionality.

## 3. Scope

### In Scope

- GET requests
- POST requests
- PUT requests
- PATCH requests
- DELETE requests
- Positive scenarios
- Negative scenarios
- HTTP status code validation
- Response structure validation
- Required field validation
- Request and response data validation
- Query parameter filtering
- Invalid resource handling

### Out of Scope

- Performance testing
- Load testing
- Stress testing
- Security testing
- Authentication and authorization
- Database testing
- UI testing
- Mobile testing

## 4. Test Environment

| Parameter        | Value              |
| ---------------- | ------------------ |
| Operating System | Windows            |
| Tool             | Postman            |
| API              | JSONPlaceholder    |
| Protocol         | HTTPS              |
| Data Format      | JSON               |
| Testing Type     | Manual API Testing |

## 5. API Operations Under Test

1. GET - Get All Posts
2. GET - Get Post By ID
3. GET - Get Nonexistent Post
4. POST - Create Post
5. PUT - Update Post
6. PATCH - Partial Update Post
7. DELETE - Delete Post
8. GET - Get Post With Invalid ID
9. GET - Filter Posts By User ID
10. GET - Filter Posts By Nonexistent User ID

## 6. Test Approach

Each request is executed in Postman and validated using Postman test scripts.

Validation includes:

- HTTP status codes
- Response structure
- Response data types
- Required fields
- Field values
- IDs
- Request and response data consistency
- Query parameter results
- Negative scenarios

## 7. Entry Criteria

- API endpoint is available.
- Postman is installed.
- API requests are configured.
- Test data is prepared.
- Expected results are defined.

## 8. Exit Criteria

- All planned requests are executed.
- Positive scenarios are tested.
- Negative scenarios are tested.
- All assertions are executed.
- Test results are documented.
- No unresolved test failures remain.

## 9. Test Data

### Create Post

    {
        "title": "Manual QA API Test",
        "body": "Testing POST request in Postman",
        "userId": 1
    }

### Update Post

    {
        "id": 1,
        "title": "Updated Manual QA Test",
        "body": "Post content was completely updated",
        "userId": 1
    }

### Partial Update

    {
        "title": "Partially Updated Title"
    }

### Negative Test Data

| Test                | Value    |
| ------------------- | -------- |
| Nonexistent Post ID | `9999` |
| Invalid Post ID     | `abc`  |
| Nonexistent User ID | `999`  |

## 10. Expected Results

| Request                       | Expected Status |
| ----------------------------- | --------------: |
| Get All Posts                 |             200 |
| Get Post By ID                |             200 |
| Get Nonexistent Post          |             404 |
| Create Post                   |             201 |
| Update Post                   |             200 |
| Partial Update Post           |             200 |
| Delete Post                   |             200 |
| Invalid Post ID               |             404 |
| Filter By User ID             |             200 |
| Filter By Nonexistent User ID |             200 |

## 11. Test Results

| Metric     | Result |
| ---------- | -----: |
| Requests   |     10 |
| Assertions |     38 |
| Passed     |     38 |
| Failed     |      0 |
| Blocked    |      0 |

**Pass Rate:** 100%

**Overall Result:** PASS

## 12. Limitations

JSONPlaceholder is a mock API.

POST, PUT, PATCH, and DELETE operations are simulated and do not permanently modify server-side data.

Database persistence is outside the scope of this project.
