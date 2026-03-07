# HTLogin Test Suite

This directory contains unit tests for the HTLogin project.

## Installation

To run the tests, first install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running Tests

To run all tests:

```bash
pytest
```

or

```bash
python -m pytest
```

To run a specific test file:

```bash
pytest tests/test_config.py
```

To run a specific test function:

```bash
pytest tests/test_config.py::TestConfig::test_config_default_values
```

## Test Coverage

To run tests with coverage report:

```bash
pytest --cov=. --cov-report=html
```

This command generates an HTML coverage report (`htmlcov/index.html`).

## Test Files

- `test_config.py`: Tests for Config class and configuration management
- `test_form_parser.py`: Tests for FormParser class and HTML form parsing (including CAPTCHA detection)
- `test_detection.py`: Tests for LoginSuccessDetector and confidence score calculation
- `test_credentials.py`: Tests for CredentialProvider and credential management
- `test_api_discovery.py`: Tests for APIDiscovery class and API endpoint discovery
- `test_api_tester.py`: Tests for APITester class and JSON API/GraphQL login testing

## Test Structure

Tests are written using the pytest framework. Each test file contains test classes for the related module.

Tests are categorized as follows:
- **Unit Tests**: Individual function and class tests
- **Integration Tests**: Inter-module interaction tests
