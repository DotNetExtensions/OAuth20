# GitFlow Workflow for DotNetExtensions.OAuth20

This document outlines the GitFlow branching strategy used in the DotNetExtensions.OAuth20 project. Adhering to this workflow ensures consistent and organized code management across the project.

## Table of Contents

- [Overview](#overview)
- [Visual Diagram](#visual-diagram)
- [Branch Types](#branch-types)
  - [Main Branch](#main-branch)
  - [Develop Branch](#develop-branch)
  - [Feature Branches](#feature-branches)
  - [Bugfix Branches](#bugfix-branches)
  - [Hotfix Branches](#hotfix-branches)
  - [Release Branches](#release-branches)
- [Quick Reference Guide](#quick-reference-guide)
- [Branch Naming Conventions](#branch-naming-conventions)
- [Protected Branch Policies](#protected-branch-policies)
- [Workflow Steps](#workflow-steps)
  - [Creating a Feature Branch](#creating-a-feature-branch)
  - [Merging a Feature Branch](#merging-a-feature-branch)
  - [Creating a Hotfix Branch](#creating-a-hotfix-branch)
  - [Merging a Hotfix Branch](#merging-a-hotfix-branch)
- [Common Pitfalls and How to Avoid Them](#common-pitfalls-and-how-to-avoid-them)
- [References](#references)

---

## Overview

GitFlow is a branching model that provides a robust framework for managing larger projects. It defines a strict branching model designed around the project release. This document explains how we implement GitFlow in the DotNetExtensions.OAuth20 project.

## Visual Diagram

<img src="./assets/atlassian-gitflow-diagram.svg" width="768">

<!-- ![GitFlow Diagram](./assets/atlassian-gitflow-diagram.svg) -->

*Figure 1: GitFlow Branching Model (taken from [Atlassian GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow))*

## Branch Types

### Main Branch

- **Branch Name:** `main`
- **Purpose:** Contains production-ready code.
- **Protected:** Yes

### Develop Branch

- **Branch Name:** `develop`
- **Purpose:** Integrates features for the upcoming release.
- **Protected:** Yes

### Feature Branches

- **Prefix:** `feature/`
- **Purpose:** Used to develop new features for the upcoming release.
- **Base Branch:** `develop`

### Bugfix Branches

- **Prefix:** `bugfix/`
- **Purpose:** Used to fix non-critical bugs identified during the current release cycle.
- **Base Branch:** `develop`

### Hotfix Branches

- **Prefix:** `hotfix/`
- **Purpose:** Used to fix critical issues in the production code.
- **Base Branch:** `main`

### Release Branches

- **Prefix:** `release/`
- **Purpose:** Prepare for a new production release.
- **Base Branch:** `develop`

## Quick Reference Guide

| Branch Type     | Prefix       | Base Branch | Merge Into     | Purpose                          |
|-----------------|--------------|-------------|----------------|----------------------------------|
| Main            | `main`       | N/A         | N/A            | Production-ready code            |
| Develop         | `develop`    | `main`      | N/A            | Integration of features          |
| Feature         | `feature/`   | `develop`   | `develop`      | New feature development          |
| Bugfix          | `bugfix/`    | `develop`   | `develop`      | Non-critical bug fixes           |
| Hotfix          | `hotfix/`    | `main`      | `main`, `develop` | Critical fixes in production     |
| Release         | `release/`   | `develop`   | `develop`, `main` | Release preparation             |

## Branch Naming Conventions

- **Feature Branches:**

  ```bash
  git checkout -b feature/feature-name develop
  ```

- **Bugfix Branches:**

  ```bash
  git checkout -b bugfix/bugfix-name develop
  ```

- **Hotfix Branches:**

  ```bash
  git checkout -b hotfix/hotfix-name main
  ```

- **Release Branches:**

  ```bash
  git checkout -b release/version-number develop
  ```

Branch names should be descriptive and use lowercase letters with hyphens to separate words.

## Protected Branch Policies

The following branches are protected to prevent direct pushes and require pull requests for merging:

- `main`
- `develop`

**Protection Rules:**

- **Pull Request Reviews:** At least one approval is required.
- **Status Checks:** All CI checks must pass before merging.
- **No Force Pushes:** Force pushes are not allowed.
- **No Deletions:** Deleting these branches is prohibited.

Exceptions to these policies can only be made by project maintainers in exceptional circumstances.

## Workflow Steps

### Creating a Feature Branch

1. **Update `develop` Branch:**

   ```bash
   git checkout develop
   git pull origin develop
   ```

2. **Create Feature Branch:**

   ```bash
   git checkout -b feature/your-feature-name develop
   ```

3. **Develop Your Feature:**

   - Commit changes following the commit message conventions.

4. **Push Feature Branch to Remote:**

   ```bash
   git push origin feature/your-feature-name
   ```

### Merging a Feature Branch

1. **Create a Pull Request:**

   - Target Branch: `develop`
   - Ensure all CI checks pass.
   - Get at least one approval.

2. **Merge the Pull Request:**

   - Use "Squash and Merge" to maintain a clean history.

3. **Delete the Feature Branch:**

   - After merging, delete the feature branch from remote.

### Creating a Hotfix Branch

1. **Update `main` Branch:**

   ```bash
   git checkout main
   git pull origin main
   ```

2. **Create Hotfix Branch:**

   ```bash
   git checkout -b hotfix/your-hotfix-name main
   ```

3. **Fix the Issue:**

   - Commit changes with appropriate messages.

4. **Push Hotfix Branch to Remote:**

   ```bash
   git push origin hotfix/your-hotfix-name
   ```

### Merging a Hotfix Branch

1. **Create Pull Requests:**

   - Target Branches: `main` and `develop`
   - Ensure all CI checks pass.
   - Get necessary approvals.

2. **Merge the Pull Requests:**

   - Merge into `main` first, then into `develop`.

3. **Tag the Release (if applicable):**

   ```bash
   git checkout main
   git pull origin main
   git tag -a vX.X.X -m "Release version X.X.X"
   git push origin vX.X.X
   ```

## Common Pitfalls and How to Avoid Them

- **Forgetting to Pull Latest Changes:**

  - *Issue:* Conflicts may occur if you don't have the latest code.
  - *Solution:* Always pull the latest changes before creating a new branch.

- **Incorrect Base Branch:**

  - *Issue:* Branching from the wrong base can cause integration issues.
  - *Solution:* Verify you're on the correct base branch (`develop` or `main`) before creating a new branch.

- **Not Following Naming Conventions:**

  - *Issue:* Inconsistent branch names make tracking difficult.
  - *Solution:* Adhere strictly to the naming conventions outlined above.

- **Directly Pushing to Protected Branches:**

  - *Issue:* This action is blocked and may cause delays.
  - *Solution:* Always create a pull request for merging into protected branches.

## References

- [Atlassian GitFlow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
- [Semantic Versioning](https://semver.org/)
- [Contributing Guidelines](./CONTRIBUTING.md)
- [Conventions](./CONVENTIONS.md)

---

By following this GitFlow workflow, we maintain a clean and organized codebase that facilitates collaboration and efficient development.

