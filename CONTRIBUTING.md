# Contributing to DotNetExtensions.OAuth20

Thank you for your interest in contributing to DotNetExtensions.OAuth20! We appreciate all contributions, whether big or small, and we aim to make the process as clear and efficient as possible. Please review the following guidelines to ensure a smooth collaboration.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Contributing to Documentation and Project Files](#contributing-to-documentation-and-project-files)
    - [Branching Strategy](#branching-strategy)
    - [Commit Messages](#commit-messages)
    - [Pull Requests](#pull-requests)
- [Style Guides](#style-guides)
  - [Writing Standards](#writing-standards)
- [Security Vulnerabilities](#security-vulnerabilities)
- [Additional Notes](#additional-notes)

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](./CODE_OF_CONDUCT.md). Please familiarize yourself with this document to ensure a positive and inclusive community environment.

---

## How Can I Contribute?

### Reporting Bugs

1. [**Search for existing issues**](https://github.com/DotNetExtensions/OAuth20/issues) to avoid duplication.
2. If no issue exists, create a new one via the GitHub Issues section.
3. Provide as much detail as possible:
   - Description of the bug.
   - Steps to reproduce.
   - Expected vs. actual behavior.
   - Relevant screenshots or logs, if applicable.

### Suggesting Enhancements

To propose new features or improvements:

1. [**Create an issue**](https://github.com/DotNetExtensions/OAuth20/issues/new/choose) in GitHub with a detailed description of your idea, including:
   - The reasoning behind the enhancement.
   - How it benefits the project.
   - Any relevant details or examples.

### Contributing to Documentation and Project Files

We welcome contributions to our documentation and project files, including correcting typos, improving clarity, and adding new content.

#### Branching Strategy

1. **Fork the repository** and clone it to your local machine:

   ```bash
   git clone https://github.com/your-username/OAuth20.git
   ```

2. **Create a new branch** following our branching strategy:

   - For new features or significant updates (e.g., adding new documents or major revisions):

     ```bash
     git checkout -b feature/your-feature-name develop
     ```

   - For fixing non-critical issues (e.g., correcting formatting errors):

     ```bash
     git checkout -b bugfix/your-bugfix-name develop
     ```

   - For fixing critical issues that require immediate attention (e.g., fixing broken links):

     ```bash
     git checkout -b hotfix/your-hotfix-name main
     ```

3. **Make your changes** to the documentation or project files.

4. **Commit your changes** with clear and descriptive commit messages.

5. **Push your branch** to your forked repository:

   ```bash
   git push origin your-branch-name
   ```

6. **Submit a pull request** to the main repository. All changes made in `feature` and `bugfix` branches should be merged into the `develop` branch, while changes from `hotfix` branches should be merged into the `main` branch via pull requests.

For detailed information on branching strategies (e.g., `feature/`, `bugfix/`, `hotfix/`), please refer to the [GITFLOW.md](./GITFLOW.md).


#### Commit Messages

- Use **sentence case** for commit messages (start with a capital letter, avoid periods).
- **Format:** `[scope] #issue_number Description of the change`.
  - **Scopes:** Use scopes relevant to documentation, such as `[docs]`, `[config]`, `[workflow]`.
  - **Example:**

    - `[docs] #15 Update README with installation instructions`
    - `[config] #20 Add GitHub Actions workflow for linting`

- Place the issue number directly after the scope to quickly reference related issues.

#### Pull Requests

- Ensure your pull request is **linked to a GitHub issue** if applicable.
- Use clear, descriptive titles and provide a detailed summary of the changes in the pull request.
- Include the **issue number** in the pull request title and description if it's related to an existing issue.
- Our pull request template includes a checklist; please ensure you review and complete it before submitting.
- **Target the `develop` branch** when creating your pull request (unless it's a hotfix, which should target `main`).

---

## Style Guides

### Writing Standards

- **Clarity and Conciseness:** Ensure that your contributions are clear and concise.
- **Tone:** Use a professional and friendly tone.
- **Language:** All contributions should be in English.
- **Formatting:** Follow the existing formatting styles used in the documents.
- **Markdown Best Practices:** Use proper Markdown syntax for headings, lists, links, code blocks, etc.
- **Consistency:** Adhere to the guidelines outlined in our [CONVENTIONS.md](./CONVENTIONS.md) file.

---

## Security Vulnerabilities

If you discover a security vulnerability, please follow our [SECURITY.md](./SECURITY.md) guidelines for responsible disclosure. We take security seriously and will address issues promptly.

---

## Additional Notes

- We value all contributions—no matter the size—whether it's fixing a typo or adding new sections.
- If you have any questions or need clarification, feel free to reach out via GitHub issues or discussions.
- **Open Communication:** We're here to help. Don't hesitate to ask questions if you're unsure about any process.

Thank you for helping us improve DotNetExtensions.OAuth20!
