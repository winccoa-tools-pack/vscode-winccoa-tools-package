# Contributing to WinCC OA Tools Package

Thank you for your interest in contributing to the WinCC OA Tools Package. This document provides guidelines to ensure a smooth collaboration process.

## 🤝 Code of Conduct

This project follows a Code of Conduct. By participating, you are expected to maintain professional and respectful communication.

## 🚀 Quick Start for Contributors

### 1. Fork & Clone

1. Fork the repository on GitHub.
2. Clone your fork:

```powershell
git clone https://github.com/YOUR_USERNAME/vscode-winccoa-tools-package.git
cd vscode-winccoa-tools-package
```

3. Add upstream remote (optional):

```powershell
git remote add upstream https://github.com/winccoa-tools-pack/vscode-winccoa-tools-package.git
```

### 2. Follow Git Flow

This repository uses a Git Flow branching model.

For new features:

```powershell
# Ensure you're on develop
git checkout develop
git pull upstream develop
# Create feature branch
git checkout -b feature/your-feature-name
```

For bug fixes (development):

```powershell
git checkout develop
git pull upstream develop
git checkout -b bugfix/issue-description
```

For hotfixes (production):

```powershell
git checkout main
git pull upstream main
git checkout -b hotfix/critical-fix
```

### 3. Development Workflow

```powershell
# Install dependencies (if any)
npm install

# Start development (extension development host)
npm run watch

# In another terminal, run tests
npm test

# Compile TypeScript (if applicable)
npm run compile
```

### 4. Commit and Push

```powershell
git add .
git commit -m "feat: descriptive message"
git push origin feature/your-feature-name
```

### 5. Create Pull Request

1. Open your fork on GitHub and click "Compare & pull request".
2. Base branch: `develop` for features/bugs; `main` for hotfixes/releases.
3. Provide a clear description and reference related issues.

## Development Setup

### Prerequisites

- Node.js 18.x or later
- Visual Studio Code 1.105.0 or later
- Git

### Installation

```powershell
git clone https://github.com/winccoa-tools-pack/vscode-winccoa-tools-package.git
cd vscode-winccoa-tools-package
npm install
```

### Running the Extension

1. Open the project in VS Code
2. Press `F5` to launch an Extension Development Host window

## Code Style

- Use TypeScript for new code where applicable.
- Follow existing code style and formatting.
- Run `npm run lint` to check style issues.

## Testing

- Write tests for new functionality.
- Ensure existing tests pass: `npm test`.

## 🔒 Mandatory CI/CD Checks

All pull requests must pass the automated CI/CD pipeline before merging. Required checks typically include:

- Linting: `npm run lint`
- TypeScript compilation: `npm run compile`
- Tests: `npm test`
- Package validation: `vsce package` (optional in CI)

Branch protection rules require pull requests, passing status checks, and at least one approving review.

## WinCC OA Specific Guidelines

- Maintain compatibility with WinCC OA configuration files.
- Test with actual WinCC OA projects when possible.
- Consider Windows-specific file paths and permissions.

## Submitting Changes

1. Create a descriptive branch name.
2. Make atomic commits with clear messages.
3. Update documentation if needed.
4. Ensure all tests pass.
5. Submit a PR with a clear description and link to related issues.

## Reporting Issues

- Use the issue templates when filing issues.
- Include VS Code and WinCC OA version information.
- Provide steps to reproduce and relevant logs.

## License

By contributing, you agree your contributions will be licensed under the MIT License.
