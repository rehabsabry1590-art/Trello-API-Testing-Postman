# Trello API Automation Testing Project – Postman

## Project Overview

This is a hands-on API Testing training project using the Trello REST API and Postman.

The project focuses on testing Trello Boards, Lists, and Cards by creating, retrieving, updating, and deleting resources through API requests.

## Tools & Technologies

* Postman
* Trello REST API
* REST APIs
* JSON
* HTTP Methods

## APIs Tested

The following Trello resources were tested:

* Boards
* Lists
* Cards

## HTTP Methods

The project covers the following HTTP methods:

* **GET** – Retrieve resources
* **POST** – Create resources
* **PUT** – Update resources
* **DELETE** – Delete resources

## Testing Activities

* Created and executed API requests using Postman.
* Tested CRUD operations for Boards, Lists, and Cards.
* Used Postman Environment Variables to manage API configuration.
* Used dynamic IDs such as Board ID, List ID, and Card ID between requests.
* Used API Key and Token for authentication.
* Validated HTTP status codes and API responses.
* Created Postman test scripts and assertions to validate response data.
* Validated response properties such as `id`, `name`, and `url`.
* Validated response time.
* Used Trello API documentation to understand endpoints and required parameters.

## Environment Variables

The project uses a Postman environment to manage API configuration and dynamic values, including:

* Base URL
* API Key
* Token
* Board ID
* List ID
* Card ID

Sensitive credentials such as API Keys and Tokens are not included in this repository.

## Testing Flow

The project follows the relationship between Trello resources:

**Board → List → Card**

A Board is created first, followed by creating and managing a List using the Board ID. A Card can then be created and managed using the List ID.

Resource IDs are stored in Postman environment variables and reused in subsequent requests.

A separate diagram (`Trello API Execution Flow.png`) documents the full request order and dependencies between all Board, List, and Card operations.

## Postman Test Scripts

Postman test scripts were used to validate API responses automatically.

Examples of validations include:

* Status code is `200`
* Response time is less than `1000 ms`
* Response contains an `id`
* Response contains a `name`
* Response contains a `url`
* Status code is `404` after a resource is deleted, confirming successful deletion

## Collection Run Results

The Postman collection was executed using the configured Trello API environment.

| Metric                | Result |
| --------------------- | -----: |
| Total Tests           |     47 |
| Passed                |     45 |
| Failed                |      2 |
| Errors                |      0 |
| Average Response Time | 300 ms |

The collection run demonstrates the execution of API requests and automated response validations across the project.

## Screenshots

The `screenshots/` folder contains supporting evidence of the testing process:

* **Run-Results.png** – Full collection run summary (47 tests, 45 passed, 2 failed). Sensitive values (API Key) are redacted.
* **postman-test-assertions.png** – Test script assertions for the *Create Board* request, validating that the response contains `id` and `name`.
* **postman-test-assertions..png** – Test script assertion for the *Get Deleted Board* request, validating a `404` status code after deletion.

## Project Structure

```text
Trello-API-Testing-Postman
│
├── README.md
├── Trello APIs.postman_collection.json
├── Trello API Execution Flow.png
└── screenshots/
    ├── Run-Results.png
    ├── postman-test-assertions.png
    └── postman-test-assertions..png
```

## Project Type

Training / Portfolio Project

## Author

**Rehab Sabry**
