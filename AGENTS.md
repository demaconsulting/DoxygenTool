# Instructions for AI Agents

This document provides guidance for AI agents contributing to the DoxygenTool project.

## Project Overview

DoxygenTool is a .NET tool wrapper for the Doxygen documentation generator. The project repackages Doxygen binaries for multiple platforms as a .NET global/local tool, allowing version control through .NET tool manifests.

## Important Guidelines

### README.md Special Requirements

**CRITICAL**: The README.md file is distributed in the NuGet package and must only contain absolute URLs. This is because:

* The README.md is included in the NuGet package
* Relative links will not work when viewed from NuGet.org
* Relative links will not work when the package is installed locally

When editing README.md:

* Use only absolute URLs (e.g., `https://github.com/demaconsulting/DoxygenTool/blob/main/...`)
* Do not use relative paths (e.g., `./file.md` or `../file.md`)
* Use Markdown link reference format for better maintainability
* All links should point to stable references (main branch or specific tags)

### Quality Standards

All contributions must pass quality checks:

1. **Spelling**: Run `npx cspell "**/*.md" "**/*.yaml" "**/*.yml" "**/*.json"`
2. **Markdown Linting**: Run `npx markdownlint-cli "**/*.md"`

These checks are enforced in CI/CD through the Quality Checks job in `.github/workflows/build_on_push.yaml`.

### Testing Changes

When making changes:

1. Follow the spelling and markdown linting rules
2. Test changes locally before committing
3. Verify quality checks pass as part of testing
4. For build-related changes, test the full build process
5. For documentation changes, verify all links are absolute URLs (especially in README.md)

## Build Process

The project uses a multi-stage build process:

1. Downloads DotnetToolWrapper binaries
2. Downloads Doxygen binaries for Windows and Linux
3. Generates SBOM (Software Bill of Materials)
4. Creates the NuGet package

## File Structure

* `.github/` - CI/CD workflows, issue templates, and dependabot config
* `pack/` - NuGet package source and build files
* `.cspell.json` - Spelling dictionary and configuration
* `.markdownlint.json` - Markdown linting rules
* `README.md` - Project documentation (must use absolute URLs only)
* `CONTRIBUTING.md` - Contribution guidelines
* `SECURITY.md` - Security policy
* `CODE_OF_CONDUCT.md` - Community code of conduct

## Common Tasks

### Adding Dependencies

Dependencies are managed through:

* `.github/dependabot.yml` - Automated dependency updates
* `.config/dotnet-tools.json` - .NET tool dependencies

### Updating Documentation

1. Edit the relevant Markdown file
2. Ensure README.md uses absolute URLs only
3. Run spelling and linting checks
4. Verify all links work correctly

### Modifying Build Process

1. Edit the appropriate workflow file in `.github/workflows/`
2. Test changes in a feature branch
3. Monitor the CI/CD pipeline for issues

## References

* [Doxygen Official Site][doxygen]
* [.NET Tools Documentation][dotnet-tools]
* [NuGet Package Documentation][nuget]

[doxygen]: https://www.doxygen.nl/
[dotnet-tools]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[nuget]: https://learn.microsoft.com/en-us/nuget/
