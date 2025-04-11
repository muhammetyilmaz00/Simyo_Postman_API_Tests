# Simyo API Tests

This repository contains API tests for the Simyo API using Postman and Newman. The tests are designed to validate the functionality of purchasing extra MB bundel from Simyo.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running Tests Locally](#running-tests-locally)
- [Running Tests with GitHub Actions](#running-tests-with-github-actions)
- [Viewing Test Results](#viewing-test-results)

## Prerequisites

To run these tests, you need to have the following installed:

- [Node.js](https://nodejs.org/) (which includes npm)
- [Newman](https://github.com/postmanlabs/newman)
- Postman (for editing and exporting collections)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/muhammetyilmaz00/Simyo_Postman_API_Tests
cd Simyo_Postman_API_Tests
```

### 2. Install Newman and the HTMLEXTRA Reporter

```bash
npm install -g newman
npm install -g newman-reporter-htmlextra
```

## Running Tests Locally

### 1. Run Postman Collection

```bash
newman run Simyo_MB_Bundle_Flow.postman_collection.json -e Simyo_Environment_Variables.postman_environment.json -r cli,htmlextra --reporter-htmlextra-export Simyo_Postman_API_Tests.html
```

## Running Tests with GitHub Actions

This repository is configured to run the Postman tests automatically using GitHub Actions. The workflow is triggered on:

Push events to the `main` branch.
Pull requests targeting the `main` branch.
Manual triggers via the GitHub Actions interface.

### Manually Triggering the Workflow
To manually run the tests:

1. Navigate to the "Actions" tab in your GitHub repository.
2. Select the "Run Postman Tests with Newman" workflow.
3. Click the "Run workflow" button.

## Viewing Test Results

### Locally
After running the tests locally, open the `Simyo_Postman_API_Tests.html` file in a web browser to view the detailed test report.

### GitHub Actions
When the tests are run via GitHub Actions:

1. Go to the "Actions" tab in your GitHub repository.
2. Select the latest workflow run.
3. Download the `Simyo_Postman_API_Tests.html` file from the "Artifacts" section to view the results.

