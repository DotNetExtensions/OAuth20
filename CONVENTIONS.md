# Conventions for DotNetExtensions.OAuth20 Project

This document outlines the coding, naming, and formatting conventions that all contributors must follow when contributing to the DotNetExtensions.OAuth20 project. Currently, these agreements must be followed manually. However, in the future (during the **Setup CI/CD Workflows** milestone), we will introduce configuration files for popular linters and IDEs (like Visual Studio 2022, Visual Studio Code, Rider) and automate validation for commits and pull requests via GitHub workflows.

## Table of Contents
- [Coding Standards](#coding-standards)
  - [Naming Conventions](#naming-conventions)
  - [General Coding Style](#general-coding-style)
  - [Formatting Rules](#formatting-rules)
- [Commit Messages](#commit-messages)
- [Branching Strategy](#branching-strategy)
- [Testing Guidelines](#testing-guidelines)
- [Documentation](#documentation)
- [Security Best Practices](#security-best-practices)
- [Future Automation](#future-automation)

---

## Coding Standards

The following conventions are to be followed manually until the setup of CI/CD workflows where automatic validation will be integrated.

### Naming Conventions

We follow the official [Microsoft Naming Guidelines](https://learn.microsoft.com/en-us/dotnet/standard/design-guidelines/general-naming-conventions) and [Style Rules](https://learn.microsoft.com/en-us/dotnet/fundamentals/code-analysis/style-rules/naming-rules). Here’s a summary of the naming conventions to be manually adhered to:

- **Classes & Interfaces**: Use `PascalCase`. Interfaces should start with an `I` (e.g., `ILogger`, `OAuthService`).
- **Methods & Properties**: Use `PascalCase` (e.g., `GetUserData`, `ValidateToken`).
- **Variables & Parameters**: Use `camelCase` (e.g., `userName`, `tokenValue`).
- **Fields**: Private fields should start with an underscore (e.g., `_cache`, `_logger`).
- **Abbreviations**: Abbreviations in identifiers should be written with only the first letter capitalized (e.g., `XmlParser`, `HttpClient`). If multiple abbreviations are used, each follows the same rule (e.g., `XmlHttpClient`).

### General Coding Style

We follow the **Allman style** for braces, where opening braces are placed on a new line. This applies to both code blocks (like methods) and declaration blocks (like classes). For now, this rule must be manually enforced by all contributors.

```csharp
if (condition) 
{
    // code block
}
```

For method definitions:

```csharp
public void SomeMethod()
{
    // method code
}
```

For class declarations:

```csharp
public class SomeClass
{
    public void SomeMethod()
    {
        // method code
    }
}
```

### Formatting Rules

- **Indentation**: Use 4 spaces for indentation (no tabs).
- **Max Line Length**: Limit lines to 120 characters.
- **Newlines**: Use a newline after method signatures and between logical blocks of code.
- **Error Handling**: Use `try-catch` blocks for error handling and always log meaningful messages when an exception occurs.
- **Line Endings (CRLF)**: Use `CRLF` (Carriage Return + Line Feed) as the line ending format, ensuring consistency across platforms. Configure your IDE to always use CRLF for this project.

```csharp
try 
{
    // code
} 
catch (Exception ex) 
{
    _logger.LogError(ex, "Error processing request.");
    throw;
}
```

---

## Commit Messages

Commit messages should follow the format below and will eventually be validated automatically, but for now, this process is manual.

- Format: `[scope] #issue_number Description`
- Ensure the commit messages are clear and concise.

```plaintext
[feature] #15 Implement OAuth token refresh mechanism
```

---

## Branching Strategy

We follow the [GitFlow](./GITFLOW.md) branching strategy for managing features, bug fixes, and releases. All merges into `main` and `develop` should be done through pull requests only that have been reviewed and approved. This will be manually enforced until CI/CD workflows are in place.

---

## Testing Guidelines

- Write unit tests for all new code.
- Use the format `MethodName_StateUnderTest_ExpectedBehavior` for test names.

```csharp
[Fact]
public void ValidateToken_ValidToken_ReturnsTrue()
{
    // Arrange
    // Act
    // Assert
}
```

---

## Documentation

- Use XML comments for all public methods, properties, and classes.
- Keep all documentation files up-to-date as features evolve.

---

## Security Best Practices

- Always validate input to prevent SQL injection, XSS, and other vulnerabilities.
- Use parameterized queries where applicable and encrypt sensitive data at rest and in transit.
- Always handle sensitive information, such as API keys and passwords, securely in configuration files.

---

## Future Automation

In the future, during the **Setup CI/CD Workflows** milestone, the following automation will be implemented:

1. **Linter Configurations**: 
    - We will add configuration files for linters (e.g., StyleCop, .NET Analyzers) and IDEs (Visual Studio 2022, Rider, Visual Studio Code).
    - Contributors will be able to install these configurations into their IDEs to automatically apply the conventions described here.

2. **GitHub Workflow Integration**:
    - Automated validation for commits and pull requests will be integrated, ensuring adherence to the naming, formatting, and style rules outlined here.
    - This will include:
        - Automated linting using StyleCop and .NET Analyzers.
        - Automatic validation of commit message formats.
        - Pull request validation to ensure all tests pass and the code meets the required conventions.

---

## Conclusion

This document outlines all current coding conventions to be followed manually. In the future, automatic linter configuration and GitHub workflows will be implemented to enforce these rules. For now, contributors must adhere to these conventions and best practices manually until the milestone is reached.
