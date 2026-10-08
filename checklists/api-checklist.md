
# API Testing Checklist

## General API Checks

- [X] API endpoint is available
- [X] Correct base URL is used
- [X] Correct HTTP methods are used
- [X] Requests return responses
- [X] Response format is JSON

## GET - Get All Posts

- [X] GET request is sent
- [X] Status code is 200
- [X] Response is an array
- [X] Response contains 100 posts
- [X] Required fields are present

## GET - Get Post By ID

- [X] Valid post ID is used
- [X] Status code is 200
- [X] Response is an object
- [X] Post ID is correct
- [X] Required fields are present
- [X] Title is not empty
- [X] Body is not empty

## GET - Get Nonexistent Post

- [X] Nonexistent post ID is used
- [X] Status code is 404
- [X] Response body is an empty object

## POST - Create Post

- [X] POST request is sent
- [X] Correct Content-Type is used
- [X] Request body is valid JSON
- [X] Status code is 201
- [X] Submitted title is returned
- [X] Submitted body is returned
- [X] Correct userId is returned
- [X] Generated ID is returned

## PUT - Update Post

- [X] PUT request is sent
- [X] Correct Content-Type is used
- [X] Complete request body is provided
- [X] Status code is 200
- [X] Post ID is preserved
- [X] Title is updated
- [X] Body is updated
- [X] User ID is preserved

## PATCH - Partial Update Post

- [X] PATCH request is sent
- [X] Correct Content-Type is used
- [X] Partial request body is provided
- [X] Status code is 200
- [X] Title is updated
- [X] Post ID is preserved
- [X] User ID is preserved
- [X] Body is preserved

## DELETE - Delete Post

- [X] DELETE request is sent
- [X] Correct endpoint is used
- [X] Status code is 200
- [X] Response is an object
- [X] Deleted post ID is returned

## GET - Invalid Post ID

- [X] Invalid post ID is used
- [X] Status code is 404
- [X] Response body is an empty object

## GET - Filter By User ID

- [X] Query parameter is provided
- [X] Status code is 200
- [X] Response is an array
- [X] Response is not empty
- [X] Returned posts belong to requested user

## GET - Filter By Nonexistent User ID

- [X] Nonexistent user ID is provided
- [X] Status code is 200
- [X] Response is an array
- [X] Response is empty

## Final Validation

- [X] All planned requests executed
- [X] Positive scenarios tested
- [X] Negative scenarios tested
- [X] Response validation completed
- [X] All assertions passed
- [X] No failed tests
- [X] No unresolved defects
