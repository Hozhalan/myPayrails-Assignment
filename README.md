# My Payrails Assignment

## Overview
This repository contains a comprehensive test suite for the Alpha Vantage API, focusing on the TIME_SERIES_DAILY and GLOBAL_QUOTE endpoints. The tests are implemented using Postman and can be run to verify the API's functionality and reliability.

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
