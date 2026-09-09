# Calculator – GitHub Actions CI Demo

A simple Python calculator project created to demonstrate **Git, GitHub, GitHub Actions, automated testing, branching, pull requests, and code review** as part of a Software Engineering practical demonstration.

##  Project Objective

The objective of this project is to demonstrate how automated testing can be integrated into a GitHub development workflow.

Whenever code is pushed to the repository or a Pull Request is created, **GitHub Actions automatically runs the unit tests** to verify that the code works correctly.

## Technologies Used

* Python
* Git
* GitHub
* GitHub Actions
* Pytest

## Project Structure

```text
calculator-github-actions/
│
├── calculator.py
├── test_calculator.py
├── requirements.txt
│
└── .github/
    └── workflows/
        └── test.yml
```

## Calculator Functions

The calculator currently supports:

* Addition
* Subtraction
* Multiplication


Example:

```python
add(2, 3)
subtract(5, 3)
multiply(4, 3)
```

## Automated Testing

The project uses **pytest** for unit testing.

Run the tests locally using:

```bash
pytest -v
```

A successful test run looks like:

```text
3 passed
```

## GitHub Actions

The workflow is stored in:

```text
.github/workflows/test.yml
```

The workflow automatically:

1. Checks out the repository.
2. Sets up Python.
3. Installs the required dependencies.
4. Runs the pytest test suite.

The workflow runs whenever:

* Code is pushed to `main`.
* A Pull Request is opened against `main`.

## Failure Demonstration

As part of the practical demonstration, an intentional error is introduced into the calculator code.

For example:

```python
def multiply(a, b):
    return a + b
```

The automated test detects the incorrect result and the GitHub Actions workflow fails.

After correcting the implementation:

```python
def multiply(a, b):
    return a * b
```

the tests pass successfully.

This demonstrates how **Continuous Integration (CI)** can detect errors before code is merged.

## Git Branching Workflow

The project uses feature branches for development.

Example:

```text
main
 │
 └── feature/division
          │
          ├── Add feature
          ├── Add tests
          └── Pull Request
                   │
                   ↓
             GitHub Actions
                   │
                Tests
                   │
                   ↓
                Review
                   │
                   ↓
                Merge
```

## Pull Request & Code Review

New features are developed on separate branches and submitted through Pull Requests.

Before merging:

* GitHub Actions runs the automated tests.
* Code can be reviewed through GitHub's **Files changed** interface.
* Review comments can be added.
* The Pull Request can be approved and merged after successful checks.

## Learning Outcomes

This project demonstrates practical understanding of:

* Git version control
* Git branching
* Git commits
* GitHub repositories
* Pull Requests
* Code reviews
* Automated unit testing
* GitHub Actions
* Continuous Integration
* Detecting and fixing failed tests

## Author

**Huma**,
**Dhruv Jagadeesh**,
**Ashmitha Sri Anand**,
**Niraj Kumar**.
