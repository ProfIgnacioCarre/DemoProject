# Demo Project

## Introduction

This demo project is designed to help you set up a Git repository with basic branching strategies.

## Table of Contents

- [Getting Started](#getting-started)
- [Branching Strategy](#branching-strategy)
- [Committing Guidelines](#committing-guidelines)
- [Issue Tracking](#issue-tracking)
- [Full Git Flow Reference](#full-git-flow-reference)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

To get a local copy of this project up and running, follow these steps:

### Prerequisites

Ensure you have the following installed:

- **Git**: [Download and install Git](https://git-scm.com/downloads)
- **GitHub Account**: [Create a GitHub account](https://github.com/join)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/demo-project.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd demo-project
   ```

3. **Initialize the `develop` branch:**

   ```bash
   git checkout -b develop
   ```

## Branching Strategy

This project utilizes a simplified Git flow to manage development:

- **`main` branch**: Contains the stable, production-ready code.
- **`develop` branch**: Serves as the integration branch for features and bug fixes.
- **Feature branches**: Created from `develop` for new features.
- **Bugfix branches**: Created from `develop` or `main` to address specific issues.

### Workflow Examples

- **Feature Development:**

    1. Create a feature branch from `develop`:

       ```bash
       git checkout -b feature/feature-name develop
       ```

    2. After implementing the feature, merge it back into `develop`:

       ```bash
       git checkout develop
       git merge feature/feature-name
       ```

    3. Delete the feature branch:

       ```bash
       git branch -d feature/feature-name
       ```

- **Bug Fixing:**

    1. Create a bugfix branch from `main`:

       ```bash
       git checkout -b bugfix/issue-id main
       ```

    2. After resolving the bug, merge it back into `main`:

       ```bash
       git checkout main
       git merge bugfix/issue-id
       ```

    3. Delete the bugfix branch:

       ```bash
       git branch -d bugfix/issue-id
       ```

## Committing Guidelines

- **Commit Messages**: Each commit message should reference the associated issue ID for traceability. Use the following format:

```
<type>[optional scope]: <description>
[optional body]
[optional footer(s)]
```

  *Example:*

```
feat(login): add Google authentication

Implemented OAuth2 integration to allow login with Google Added unit tests for the new flow.

Issue: #45
```

- **Atomic Commits**: Ensure each commit represents a single logical change to maintain a clear and concise project history. Keep the commit message description under 50 characters for clarity.
- **Track Issues**: Reference related issues or tickets using the optional footer (e.g., Issue: #123 or Refs: #45).

## Issue Tracking

All issues are managed within the project's GitHub repository under the [Issues](https://github.com/your-username/demo-project/issues) section. Each issue should:

- Clearly describe the problem or feature request.
- Be assigned a unique ID.
- Be referenced in corresponding commit messages.

## Full Git Flow Reference

For a comprehensive understanding of Git flow practices, refer to the following resources:

- [Git Flow Cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- [A successful Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)

## Contributing

We welcome contributions to enhance this demo project. To contribute:

1. Fork the repository.
2. Create a new branch (`feature/your-feature-name`).
3. Commit your changes with clear messages referencing issue IDs.
4. Push to your forked repository.
5. Open a pull request to the `develop` branch of this repository.

## License

This project is licensed under the [MIT License](LICENSE).

---

*Note: Replace placeholders like `your-username` and `demo-project` with your actual GitHub username and repository name, respectively.* 