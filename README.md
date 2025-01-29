# My Payrails Assignment

## Overview
This repository contains a comprehensive test suite focusing on the TIME_SERIES_DAILY and GLOBAL_QUOTE endpoints. The tests are implemented using Postman and can be run to verify the API's functionality and reliability.

## Test Cases

### 1. Time Series Daily Endpoint

#### 1.1 Successful Daily Time Series Retrieval
**Test ID**: `TIME_SERIES_DAILY_SUCCESS`  
**Endpoint**: `GET /query?function=TIME_SERIES_DAILY`  
**Description**: Verifies successful retrieval of daily time series data for a valid stock symbol.

**Test Assertions**:
- Response status code should be 200
- Response should contain "Time Series (Daily)" data
- Response time should be less than 2000ms

**Required Parameters**:
- function: TIME_SERIES_DAILY
- symbol: Valid stock symbol (e.g., IBM)
- apikey: Valid API key

#### 1.2 Invalid Symbol Handling
**Test ID**: `TIME_SERIES_DAILY_INVALID_SYMBOL`  
**Endpoint**: `GET /query?function=TIME_SERIES_DAILY`  
**Description**: Verifies API's error handling when an invalid stock symbol is provided.

**Test Assertions**:
- Response status code should be 200
- Response should contain an error message
- Error message should indicate invalid symbol

**Test Parameters**:
- function: TIME_SERIES_DAILY
- symbol: "INVALID"
- apikey: Valid API key

### 2. Global Quote Endpoint

#### 2.1 Successful Global Quote Retrieval
**Test ID**: `GLOBAL_QUOTE_SUCCESS`  
**Endpoint**: `GET /query?function=GLOBAL_QUOTE`  
**Description**: Verifies successful retrieval of global quote data for a valid stock symbol.

**Test Assertions**:
- Response status code should be 200
- Response should contain "Global Quote" data
- Response should include required fields:
  - Symbol
  - Price

**Required Parameters**:
- function: GLOBAL_QUOTE
- symbol: Valid stock symbol (e.g., IBM)
- apikey: Valid API key

## Setup and Running Tests

### Prerequisites
- Install **Postman**.
- Set up **GitHub Actions** for CI/CD.

### Running Tests in Postman
1. Clone the repository:
   ```bash
   git clone https://github.com/Hozhalan/myPayrails-Assignment.git
   cd myPayrails-Assignment
2. Import myPayrails_API_Assignment.postman_collection.json into Postman.
3. Run the collection via Postman.

### Running Tests in GitHub Actions
1. The action will run tests on every push or pull request made to the repository. To trigger it manually:
   - Navigate to the Actions tab in your GitHub repository.
   - Select the latest workflow and click on Run workflow.
2. To modify or add additional workflows, edit the YAML files located in the .github/workflows directory.

### Conclusion
This repository contains the necessary API test cases for verifying key functionalities. Follow the steps above to run the tests in Postman and GitHub Actions for ensuring that the application works as expected.
