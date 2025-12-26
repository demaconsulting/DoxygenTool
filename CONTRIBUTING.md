# Contributing to DoxygenTool

Thank you for your interest in contributing to DoxygenTool! This document provides guidelines and instructions for contributing to this project.

## Code of Conduct

This project adheres to a [Code of Conduct][code-of-conduct]. By participating, you are expected to uphold this code.

## How to Contribute

### Reporting Bugs

If you find a bug, please create an issue using the bug report template. Include:

* A clear and descriptive title
* Steps to reproduce the issue
* Expected behavior
* Actual behavior
* Your environment (OS, .NET version, DoxygenTool version)

### Suggesting Features

Feature requests are welcome! Please create an issue using the feature request template. Include:

* A clear and descriptive title
* The problem you're trying to solve
* Your proposed solution
* Any alternatives you've considered

### Pull Requests

1. Fork the repository and create your branch from `main`
2. Make your changes following the guidelines below
3. Test your changes thoroughly
4. Ensure all quality checks pass (spelling and markdown linting)
5. Submit a pull request

## Development Guidelines

### Documentation

* All Markdown files must pass spelling and linting checks
* The README.md file should only contain absolute URL links as it is distributed in the NuGet package
* Use Markdown link reference format for all links

### Quality Checks

Before submitting a pull request, ensure your changes pass quality checks:

```bash
# Check spelling
npx cspell "**/*.md" "**/*.yaml" "**/*.yml" "**/*.json"

# Lint markdown files
npx markdownlint-cli "**/*.md"
```

### Testing

When making changes to the tool wrapper or build process:

1. Test the build process locally
2. Verify the generated NuGet package
3. Test the tool installation and execution

#### Automated CI Testing

All pull requests and pushes trigger automated testing via GitHub Actions:

* **Quality Checks**: Spelling and markdown linting
* **Build**: Creates the NuGet package on ubuntu-latest
* **Package Testing**: Matrix tests across:
  * Operating Systems: ubuntu-latest, windows-latest
  * .NET Versions: 8.x, 9.x, 10.x

The package tests verify the tool can be installed and executed by running `doxygen --help` and `doxygen --version`.

### Commit Messages

* Use clear and descriptive commit messages
* Reference relevant issues in commit messages

## Project Structure

* `.github/` - GitHub workflows and issue templates
* `pack/` - Package source files and build configuration
* `.cspell.json` - Spelling configuration
* `.markdownlint.json` - Markdown linting configuration

## Questions?

If you have questions, please open a discussion on GitHub.

[code-of-conduct]: https://github.com/demaconsulting/DoxygenTool/blob/main/CODE_OF_CONDUCT.md
