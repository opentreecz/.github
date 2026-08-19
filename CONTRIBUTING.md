<p align="center">
  <img src="https://raw.githubusercontent.com/opentreecz/.github/master/profile/img/opentreeczlogo.jpeg" alt="opentree.cz" width="200"/>
</p>

# Contributing to opentree.cz Projects

Thank you for your interest in contributing to opentree.cz! We welcome
contributions from everyone, whether you are fixing a typo, reporting a bug, or
building a new feature.

For a complete list of our projects, visit our
[project website](https://opentreecz.github.io/repositories) or browse the
[organization page](https://github.com/orgs/opentreecz/repositories).

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Features](#suggesting-features)
  - [Submitting Pull Requests](#submitting-pull-requests)
- [Forking and Branching Workflow](#forking-and-branching-workflow)
- [Commit Message Guidelines](#commit-message-guidelines)
- [Code Review Process](#code-review-process)
- [Development Setup](#development-setup)
- [CI and Quality Checks](#ci-and-quality-checks)

## Code of Conduct

All participants are expected to follow our
[Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

## How to Contribute

### Reporting Bugs

If you find a bug, please open an issue using the
[Bug Report template](https://github.com/opentreecz/.github/issues/new?template=bug_report.yml).
Include as much detail as possible:

- Steps to reproduce the issue
- Expected vs. actual behavior
- Environment details (OS, tool versions)
- Relevant logs or screenshots

### Suggesting Features

Have an idea for an improvement? Open an issue using the
[Feature Request template](https://github.com/opentreecz/.github/issues/new?template=feature_request.yml).
Describe the problem you are solving and your proposed solution.

### Submitting Pull Requests

1. Check existing issues and PRs to avoid duplicating effort.
2. For significant changes, open an issue first to discuss the approach.
3. Follow the [forking workflow](#forking-and-branching-workflow) below.
4. Fill out the [PR template](.github/PULL_REQUEST_TEMPLATE.md) when submitting.

## Forking and Branching Workflow

1. **Fork the repository** -- Click the "Fork" button on the repository page to
   create your own copy.

2. **Clone your fork locally:**

   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

3. **Add the upstream remote:**

   ```bash
   git remote add upstream https://github.com/opentreecz/<repo-name>.git
   ```

4. **Create a feature branch:**

   ```bash
   git checkout -b feature/your-feature-name
   ```

   Use descriptive branch names:
   - `feature/add-helm-chart` -- for new features
   - `fix/broken-proxy-config` -- for bug fixes
   - `docs/update-readme` -- for documentation changes

5. **Keep your fork up to date:**

   ```bash
   git fetch upstream
   git rebase upstream/master
   ```

6. **Make your changes**, then commit following the
   [commit guidelines](#commit-message-guidelines).

7. **Push your branch:**

   ```bash
   git push origin feature/your-feature-name
   ```

8. **Open a Pull Request** from your fork's branch to the upstream `master`
   branch.

## Commit Message Guidelines

We follow the [Conventional Commits](https://www.conventionalcommits.org/)
specification:

```text
<type>(<scope>): <short summary>

<optional body>

<optional footer>
```

### Types

| Type | Description |
|------|-------------|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation changes only |
| `style` | Formatting, whitespace (no code change) |
| `refactor` | Code change that neither fixes a bug nor adds a feature |
| `test` | Adding or correcting tests |
| `chore` | Build process, CI, or auxiliary tool changes |

### Examples

```text
feat(helm): add ingress configuration for openrepo

fix(k3s): correct node labeling script for multi-node clusters

docs(readme): update installation instructions
```

## Code Review Process

1. All PRs require at least one approving review before merging.
2. Maintainers may request changes -- please address feedback promptly.
3. Keep PRs focused and small. Large PRs are harder to review and more likely to
   have merge conflicts.
4. CI checks must pass before merging. See
   [CI and Quality Checks](#ci-and-quality-checks).

## Development Setup

Each repository may have its own setup instructions in its README. Generally:

1. Fork and clone the repository (see [above](#forking-and-branching-workflow)).
2. Follow the README in the specific project for build/run instructions.
3. Run any available tests before submitting your PR.

## CI and Quality Checks

Our repositories use GitHub Actions for continuous integration. The following
checks run on every push and pull request:

- **Markdown Lint** -- Enforces consistent Markdown formatting
- **YAML Lint** -- Validates YAML syntax and style
- **Link Check** -- Detects broken links in documentation
- **Spell Check** -- Catches typos in documentation

All CI checks must pass before a PR can be merged.

### Branch Protection

We recommend enabling branch protection on `master` with the following settings:

- Require status checks to pass before merging
- Require pull request reviews before merging
- Require branches to be up to date before merging

---

Thank you for contributing to opentree.cz!
