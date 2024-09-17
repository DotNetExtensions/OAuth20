# Coding and Formatting Conventions for DotNetExtensions.OAuth20

Consistency in code style and formatting enhances readability and maintainability of the project. This document outlines the conventions to be followed when contributing to the DotNetExtensions.OAuth20 project.

## Table of Contents

- [General Guidelines](#general-guidelines)
- [Naming Conventions](#naming-conventions)
  - [Quick Reference Table](#quick-reference-table)
  - [Namespaces](#namespaces)
  - [Classes, Abstract Classes and Interfaces](#classes-abstract-classes-and-interfaces)
  - [Methods and Asynchronous Methods](#methods-and-asynchronous-methods)
  - [Variables and Fields](#variables-and-fields)
  - [Constants](#constants)
- [Formatting Rules](#formatting-rules)
  - [Indentation](#indentation)
  - [Newlines](#newlines)
  - [Braces](#braces)
  - [Spacing](#spacing)
- [Comments and Documentation](#comments-and-documentation)
- [Example Code](#example-code)
- [Future Automation](#future-automation)
- [Use of Linters and Tools](#use-of-linters-and-tools)

---

## General Guidelines

- Adhere to the conventions outlined in this document to maintain consistency across the codebase.
- Until automation is in place, adherence relies on individual contributors to follow these guidelines.

## Naming Conventions

### Quick Reference Table

| Item                  | Convention                    | Example                    |
|-----------------------|-------------------------------|----------------------------|
| Namespace             | PascalCase                    | `DotNetExtensions.OAuth20` |
| Class                 | PascalCase                    | `AuthorizationServer`      |
| Abstract Class        | PascalCase + Base             | `AuthorizationServerBase`  |
| Interface             | I + PascalCase                | `IAuthorizationProvider`   |
| Method                | PascalCase                    | `ValidateToken()`          |
| Asynchronous Method   | PascalCase + Async            | `ValidateTokenAsync()`     |
| Public Property       | PascalCase                    | `AccessToken`              |
| Private Field         | _camelCase                    | `_tokenService`            |
| Local Variable        | camelCase                     | `tokenResponse`            |
| Constant              | PascalCase                    | `DefaultTimeout`           |
| Enum                  | PascalCase                    | `TokenType`                |
| Enum Members          | PascalCase                    | `Bearer`, `Mac`            |

### Namespaces

- Use **PascalCase** for namespaces.
- Namespaces should reflect the project structure.

**Correct:**

```csharp
namespace DotNetExtensions.OAuth20.Services
{
    // Code here
}
```

**Incorrect:**

```csharp
namespace dotnetextensions.oauth20.services
{
    // Code here
}
```

### Classes, Abstract Classes and Interfaces

- **Classes**: Use **PascalCase**.
- **Abstract Classes**: Postfix `Base` following **PascalCase**.
- **Interfaces**: Prefix with `I` followed by **PascalCase**.

**Correct:**

```csharp
public class TokenValidator
{
    // Code here
}

public abstract class TokenBuilderBase
{
    // Code here
}

public interface ITokenProvider
{
    // Code here
}
```

**Incorrect:**

```csharp
public class tokenvalidator
{
    // Code here
}

public abstract class TokenBuilder
{
    // Code here
}

public interface Tokenprovider
{
    // Code here
}
```

### Methods and Asynchronous Methods

- Use **PascalCase** for method names.
- Method names should be descriptive and use verb-noun phrases.
- Postfix `Async` following a method name for asynchronous methods.

**Correct:**

```csharp
public void GenerateAccessToken()
{
    // Code here
}

public async Task GenerateAccessTokenAsync()
{
    // Code here
}
```

**Incorrect:**

```csharp
public void generateaccesstoken()
{
    // Code here
}

public async Task GenerateAccessToken()
{
    // Code here
}
```

### Variables and Fields

- **Private Fields**: Use `_camelCase` with an underscore prefix.
- **Local Variables and Parameters**: Use **camelCase**.

**Correct:**

```csharp
private readonly ITokenService _tokenService;

public void AuthenticateUser(string username)
{
    var accessToken = _tokenService.GetToken(username);
}
```

**Incorrect:**

```csharp
private readonly ITokenService TokenService;

public void AuthenticateUser(String Username)
{
    var AccessToken = TokenService.GetToken(Username);
}
```

### Constants

- Use **PascalCase** for constants.

**Correct:**

```csharp
public const int DefaultTimeout = 30;
```

**Incorrect:**

```csharp
public const int DEFAULT_TIMEOUT = 30;
```

## Formatting Rules

### Indentation

- Use **4 spaces** for indentation.
- Do not use tabs.

**Correct:**

```csharp
if (isValid)
{
    ProcessRequest();
}
```

**Incorrect:**

```csharp
if (isValid)
  {
  ProcessRequest();
  }
```

### Newlines

- Use a newline between stereotype members and logical blocks of code.
- Use CRLF (Carriage Return + Line Feed) as the line ending format.

**Correct:**

```csharp
private readonly ICredentialsService _credentialsService;

public JwtTokenBuilder(ICredentialsService credentialsService)
{
    _credentialsService = credentialsService;
}
```

**Incorrect:**

```csharp
private readonly ICredentialsService _credentialsService;
public JwtTokenBuilder(ICredentialsService credentialsService)
{
    _credentialsService = credentialsService;
}
```

### Braces

- Use **Allman style** braces (braces on a new line).

**Correct:**

```csharp
public void Validate()
{
    // Code here
}
```

**Incorrect:**

```csharp
public void Validate() {
    // Code here
}
```

### Spacing

- Place a single space after keywords and before parentheses.
- Do not place spaces inside parentheses.

**Correct:**

```csharp
if (condition)
{
    // Code here
}
```

**Incorrect:**

```csharp
if(condition){
    // Code here
}
```

## Comments and Documentation

- Use XML documentation comments for public members.
- Write comments in clear and concise English.

**Example:**

```csharp
/// <summary>
/// Generates a new access token for the specified user.
/// </summary>
/// <param name="username">The username of the user.</param>
/// <returns>A new access token.</returns>
public string GenerateAccessToken(string username)
{
    // Code here
}
```

## Example Code

Below is an example that incorporates the conventions:

**Correct:**

```csharp
namespace DotNetExtensions.OAuth20.Server.TokenBuilders
{
    public class JwtTokenBuilder : TokenBuilderBase
    {
        private readonly ICredentialsService _credentialsService;

        public JwtTokenBuilder(ICredentialsService credentialsService)
        {
            _credentialsService = credentialsService;
        }

        public override async Task<string> GenerateAccessTokenAsync(TokenContext context)
        {
            if (condition)
            {
                // Code here
            }
        }
    }
}
```

**Incorrect:**

```csharp
namespace dotnetextensions.oauth20.server.tokenbuilders{
  public class JWT_TokenBuilder : TokenBuilder{
    private readonly ICredentialsService credentialsService;

    public JWT_TokenBuilder(ICredentialsService CredentialsService){
      credentialsService = CredentialsService;
    }

    public override async Task<string> generateAccessToken(TokenContext _context){
      if(condition){
        // Code here
      }
    }
  }
}
```

## Future Automation

We plan to automate code style enforcement by introducing IDE configuration files such as `.editorconfig` and incorporating code analysis tools into our CI/CD pipelines.

## Use of Linters and Tools

To help enforce these conventions, we recommend using the following tools:

- **EditorConfig**: Place an `.editorconfig` file at the root of the repository to define coding styles.
- **StyleCop Analyzers**: Integrate StyleCop into the project to provide real-time feedback on code style violations.
- **ReSharper**: Use ReSharper for additional code analysis and refactoring support.

---

By following these conventions, we ensure that our codebase remains clean, consistent, and maintainable.
