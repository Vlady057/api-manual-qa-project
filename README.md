
# API Manual QA Project

Manual API testing project using Postman and the JSONPlaceholder REST API.

## Project Overview

The project demonstrates manual testing of REST API endpoints including CRUD operations, filtering, positive and negative scenarios, HTTP status validation, response structure validation, and response data validation.

## API

**API:** JSONPlaceholder

**Base URL:** https://jsonplaceholder.typicode.com

**Resource:** `/posts`

## Tools

- Postman
- Git
- GitHub

## Tested Requests

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

## Test Coverage

- REST API testing
- GET requests
- POST requests
- PUT requests
- PATCH requests
- DELETE requests
- CRUD operations
- Positive testing
- Negative testing
- HTTP status code validation
- Response structure validation
- Request and response data validation
- Query parameter testing

## Test Results

| Metric       | Result |
| ------------ | -----: |
| API Requests |     10 |
| Assertions   |     38 |
| Passed       |     38 |
| Failed       |      0 |
| Blocked      |      0 |
| Pass Rate    |   100% |

## Project Structure

    api-manual-qa-project/
    │
    ├── README.md
    │
    ├── bug-reports/
    │
    ├── checklists/
    │   └── api-checklist.md
    │
    ├── collection/
    │   └── api-test-collection.json
    │
    ├── docs/
    │   ├── api-documentation.md
    │   └── test-plan.md
    │
    ├── screenshots/
    │
    ├── test-cases/
    │   └── api-test-cases.md
    │
    ├── test-scenarios/
    │   └── api-test-scenarios.md
    │
    └── test-summary/
        └── test-summary.md

## Postman Collection

The Postman collection contains all 10 tested API requests with automated response assertions.

## Limitations

JSONPlaceholder is a mock API.

POST, PUT, PATCH, and DELETE operations are simulated and do not permanently modify server-side data.
