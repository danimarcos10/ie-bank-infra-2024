# Contributing to IE Bank Infrastructure

This document outlines the process for contributing to the IE Bank Infrastructure project.

## GitHub Flow

We follow the GitHub Flow branching strategy. Here's how it works:

### Branches

- `main`: Production branch. Always deployable.
- `develop`: Development branch. Integration branch for features.
- Feature branches: Created from `develop` for new features/fixes.

### Branch Protection Rules

The `main` branch is protected with the following rules:
- Requires pull request reviews before merging
- Requires status checks to pass before merging
- Requires branches to be up to date before merging
- No direct pushes to main
- No force pushes
- No branch deletion

### Development Process

1. Create a new branch from `develop`:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/your-feature-name
   ```

2. Make your changes and commit them:
   ```bash
   git add .
   git commit -m "Description of your changes"
   ```

3. Push your branch and create a Pull Request:
   ```bash
   git push -u origin feature/your-feature-name
   ```

4. Create a Pull Request (PR) to merge into `develop`
   - Fill out the PR template
   - Request reviews from team members
   - Ensure all checks pass

5. After approval and passing checks, merge into `develop`

6. Once features are tested in `develop`, create a PR to merge into `main`

### Commit Messages

Follow these guidelines for commit messages:
- Use present tense ("Add feature" not "Added feature")
- Use imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally

### Pull Request Process

1. Update the README.md with details of changes if needed
2. Update the documentation if needed
3. The PR will be merged once you have:
   - At least one approval
   - All status checks passing
   - No merge conflicts

## Development Environment Setup

1. Install Azure CLI
2. Install Bicep CLI
3. Configure Azure credentials:
   ```bash
   az login
   ```

## Infrastructure Changes

- All infrastructure changes must be made through Bicep templates
- Test changes in development environment first
- Follow Azure naming conventions
- Document all new resources and their purposes

## Code Style

- Follow Bicep style guide
- Use consistent naming conventions
- Document all parameters and variables
- Include comments for complex logic 