# API_Automation_with_Newman
API Automation with Newman report

## Overview
This repository contains a Postman test collection and environment for the Notes API available at [Expand Testing Practice API](https://practice.expandtesting.com/notes/api). It includes a complete suite of API automation tests for features like user registration, login, profile management, note creation, updates, and deletion.

## Files Included
- `anirudha.postman_collection.json`: The main Postman collection with all test cases.
- `tonmoy.postman_environment.json`: The environment file with variables like `base_url`, `token`, `email`, etc.

## Base URL
```
https://practice.expandtesting.com/notes/api
```

## Features Covered
1. **Health Check**
2. **User Registration**
3. **User Login & Logout**
4. **Profile Retrieval & Update**
5. **Note Creation, Retrieval (all & by ID), Update (PUT/PATCH), and Deletion**
6. **Account Deletion**

## How to Use

### 1. Import into Postman
- Open Postman
- Import `anirudha.postman_collection.json`
- Import `tonmoy.postman_environment.json` as environment

### 2. Run the Tests
- Select the `tonmoy` environment
- Go to the **Collection Runner**
- Choose the `Anirudha` collection and run all requests in sequence

### 3. Dynamic Variables
Some values like name, email, password, and others are generated dynamically using Postman’s built-in variables (e.g., `{{$randomFullName}}`, `{{$randomEmail}}`). These are stored in environment variables for chained usage across requests.

## Test Validations
Each request includes comprehensive `pm.test` validations, including:
- Status code validation (e.g., 200, 201, 400, 401, 500)
- Response message validation
- Data field validation (e.g., name, email, id, token, notes fields)

## Notes API Workflow
```text
Register -> Login -> Get Profile -> Update Profile -> Create Note -> Get Notes -> Get Note by ID -> Update Note -> Patch Note -> Delete Note -> Delete Account
```

## Author
Anirudha (using Postman automation suite)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
Feel free to contribute or discuss issues if you want to extend the test suite!


