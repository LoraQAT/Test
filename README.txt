
Test Case #1: Check that the pet ID is an integer
Objective: Validate that the id field in the response is an integer.
Preconditions: Ensure valid data is provided for creating the pet.
Steps:
1.	Send a POST request to create a pet.
2.	Capture the pet ID from the response.
3.	Verify that the pet ID is an integer.
Expected Result: The pet ID in the response should be an integer.

Test Case #2: Validate the presence of a pet name
Objective: Ensure that the pet has a valid name.
Preconditions: Valid name is passed in the request.
Steps:
1.	Send a POST request with a valid pet name.
2.	Ensure that the name field in the response is not empty or null.
Expected Result: The pet name should be present in the response and match the requested name.

Test Case #3: Check that the pet category ID is correctly set
Objective: Ensure that the category.id is correctly set in the response.
Preconditions: Valid category ID is passed in the request.
Steps:
1.	Send a POST request with a valid category ID.
2.	Verify that the category.id in the response matches the provided category ID.
Expected Result: The pet's category ID should match the ID provided in the request.

Test Case #4: Check photoUrls array in the response
Objective: Validate that the photoUrls array contains valid URLs.
Preconditions: A valid URL is passed in the request for photoUrls.
Steps:
1.	Send a POST request with a valid URL in the photoUrls field.
2.	Verify that the photoUrls field in the response contains valid URLs.
Expected Result: The photoUrls field should be an array containing valid URLs.

Test Case #5: Validate missing required field for pet creation (name)
Objective: Ensure that missing required fields result in an error.
Preconditions: Send a POST request with a missing name field.
Steps:
1.	Send a POST request to create a pet without providing the name field.
2.	Ensure the response contains a validation error indicating that name is required.
Expected Result: The response should return an error indicating that the name field is required.

Test Case #6: Validate missing required field for pet creation (photoUrls)
Objective: Ensure that missing required fields result in an error.
Preconditions: Send a POST request with a missing photoUrls field.
Steps:
1.	Send a POST request to create a pet without providing the photoUrls field.
2.	Ensure the response contains a validation error indicating that photoUrls is required.
Expected Result: The response should return an error indicating that the photoUrls field is required.

Test Case #7: Check response time for creating a pet
Objective: Ensure that the response time for creating a pet is within acceptable limits.
Preconditions: Ensure that the API is operational.
Steps:
1.	Send a POST request to create a pet.
2.	Measure the response time.
Expected Result: The response time should be under 500ms.

Test Case #8: Verify multiple tags for the pet
Objective: Ensure that multiple tags can be added to a pet successfully.
Preconditions: Valid tag IDs for multiple tags are provided.
Steps:
1.	Send a POST request to create a pet with multiple tags.
2.	Verify that all provided tags are included in the response.
Expected Result: The tags array in the response should contain all the tags that were provided.

Test Case #9: Validate the creation of a pet with special characters in the name
Objective: Ensure the API handles special characters in the pet name correctly.
Preconditions: A pet name with special characters (e.g., Pet@123!) is provided.
Steps:
1.	Send a POST request with a pet name containing special characters.
2.	Verify that the pet is created successfully with the name as provided.
Expected Result: The pet should be created with the special characters correctly displayed in the response.

Test Case #10: Check that the pet creation fails when status is invalid
Objective: Ensure that providing an invalid status results in an error.
Preconditions: A pet status outside the acceptable values ("available", "pending", "sold") is provided.
Steps:
1.	Send a POST request with an invalid status (e.g., "unknown").
2.	Verify that the response returns a validation error indicating that the status is invalid.
Expected Result: The response should return a 400 Bad Request error indicating that the status is invalid.

