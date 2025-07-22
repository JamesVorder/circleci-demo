# CircleCI Demo Project

A simple Python project demonstrating basic CircleCI workflow functionality with automated testing.

## Project Structure

```
circleci-demo/
├── .circleci/
│   └── config.yml      # CircleCI configuration
├── src/
│   └── circleci_demo/
│       ├── __init__.py
│       └── calculator.py  # Calculator module
├── tests/
│   └── test_calculator.py # Test cases
├── pyproject.toml      # Project configuration and dependencies
└── README.md          # This file
```

## Features

- Basic calculator functions (add, subtract, multiply, divide)
- Unit tests using pytest
- Code coverage reporting
- Continuous Integration with CircleCI
- Proper Python package structure with `src/` layout

## Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd circleci-demo
   ```

2. Install the project with test dependencies:
   ```bash
   uv sync
   ```

## Running Tests

To run the tests locally:

```bash
uv run pytest -v
```

To run tests with coverage report:

```bash
uv run pytest --cov=src --cov-report=term-missing
```

## CircleCI Integration

This project includes a `.circleci/config.yml` file that configures the following workflow:

1. Checks out the code
2. Sets up Python environment using CircleCI's Python orb
3. Installs dependencies using pip
4. Runs tests with coverage
5. Stores test results and coverage reports as artifacts

## Viewing Results

After pushing to your repository, CircleCI will automatically run the test workflow. You can view the results:

1. In the CircleCI dashboard
2. In the "Artifacts" tab of the build for test results and coverage reports

## Development

This project uses:
- Python 3.10+
- pytest for testing
- pytest-cov for coverage reporting
- setuptools for packaging
