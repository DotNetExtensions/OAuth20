# DotNetExtensions.OAuth20 - Comprehensive OAuth 2.0 Authorization Server Project

<!-- [![Build Status](https://github.com/DotNetExtensions/OAuth20.Server/actions/workflows/build.yml/badge.svg)](https://github.com/DotNetExtensions/OAuth20.Server/actions/workflows/build.yml) -->
<!-- [![NuGet Version](https://img.shields.io/nuget/v/DotNetExtensions.OAuth20.Server)](https://www.nuget.org/packages/DotNetExtensions.OAuth20.Server) -->
[![License](https://img.shields.io/github/license/DotNetExtensions/OAuth20)](./LICENSE)
[![Contributors](https://img.shields.io/github/contributors/DotNetExtensions/OAuth20)](https://github.com/DotNetExtensions/OAuth20/graphs/contributors)

DotNetExtensions.OAuth20 is a modular, cross-platform solution designed to implement OAuth 2.0 authorization flows in .NET applications. This project offers reusable libraries for core OAuth 2.0 functionalities and a fully hosted ASP.NET Core web application, making it easy to deploy and integrate secure authorization services across various environments.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Installation](#installation)
  - [Library Installation](#library-installation)
    - [Using NuGet Packages](#using-nuget-packages)
    - [Direct Download](#direct-download)
    - [Adding Services and Middleware](#adding-services-and-middleware)
  - [Hosted Application Installation](#hosted-application-installation)
    - [Docker Installation](#docker-installation)
    - [Kubernetes Installation](#kubernetes-installation)
    - [Helm Installation](#helm-installation)
    - [Windows Service or IIS Installation](#windows-service-or-iis-installation)
- [Running Tests and Benchmarks](#running-tests-and-benchmarks)
- [Demo Projects](#demo-projects)
- [Project Structure](#project-structure)
- [Development Workflow](#development-workflow)
- [Roadmap](#roadmap)
- [Task List](#task-list)
- [Community and Support](#community-and-support)
- [Contributing](#contributing)
- [Security](#security)
- [License](#license)
- [References](#references)

## Project Overview

Welcome to the DotNetExtensions.OAuth20 project, a comprehensive solution for implementing OAuth 2.0 authorization flows in .NET applications. This project is divided into two main repositories, each serving a distinct purpose:

1. **Library Repository:**

   - Contains the core OAuth 2.0 authorization libraries, data source integration libraries, and Blazor-based UI components (Admin Panel and Personal Account).
   - Distributed via NuGet packages for easy integration into .NET projects.

2. **Hosted Application Repository:**

   - Contains an ASP.NET Core hosted web application that provides a fully functional OAuth 2.0 Authorization Server.
   - Utilizes the libraries from the Library Repository to deliver OAuth 2.0 endpoints, UI components, and data storage options.
   - Supports deployment via Docker, Kubernetes, Helm, and as a Windows Service or IIS application.

## Key Features

- **Modular Architecture:** Separates core functionality into reusable libraries and a hosted application, allowing for flexible deployment and integration.
- **Cross-Platform Compatibility:** Supports .NET 8, .NET Standard 2.0/2.1, and .NET Framework 4.8.1.
- **Flexible Data Storage:** Libraries support in-memory, SQLite, MS SQL Server, PostgreSQL, MySQL, and more.
- **User Interfaces:** Includes Blazor-based user-friendly Admin Panel and Personal Account UI for managing OAuth 2.0 consents and configurations.
- **Security Compliance:** Adheres to the OAuth 2.0 [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749) specification with additional enhancements.
- **CI/CD Integration:** Automated workflows using GitHub Actions for building, testing, and release uploading.
- **Comprehensive Testing:** Includes unit, integration, and load tests, benchmarks, demo projects, and configuration samples.
- **Container and Cloud Support:** Ready-to-use Docker images with Kubernetes and Helm deployment configurations.
- **Windows Installation:** Install on Windows OS as a Hosted Service or an IIS application.

## Getting Started

To get started with DotNetExtensions.OAuth20, follow the installation instructions below for either integrating the library into your project or deploying the hosted application.

## Installation

### Library Installation

**Prerequisites:**

- .NET SDK (version 8.0 or later)

#### Using NuGet Packages

The libraries are available as NuGet packages. To install, use the following command in your package manager console:

```bash
dotnet add package DotNetExtensions.OAuth20.Server --version x.x.x
```

Replace `x.x.x` with the latest version number from the [NuGet Gallery](https://www.nuget.org/packages/DotNetExtensions.OAuth20.Server).

#### Direct Download

You can also download the compiled library assemblies directly from the [GitHub Releases](https://github.com/DotNetExtensions/OAuth20.Server/releases) page and add them to your project manually.

#### Adding Services and Middleware

Add the library services in your `Startup.cs` or `Program.cs` file:

```csharp
services.AddOAuth20Server();
```

And use its middleware:

```csharp
app.UseOAuth20Server();
```

### Hosted Application Installation

**Prerequisites:**

- Docker (if using containerized deployments)
- Kubernetes (for cluster-based deployments)
- IIS (for IIS installations)

#### Docker Installation

To run the OAuth 2.0 Server using Docker, execute:

```bash
docker pull dotnetextensions/oauth20serverhost:latest
docker run -d -p 5000:80 dotnetextensions/oauth20serverhost:latest
```

#### Kubernetes Installation

To deploy the server on a Kubernetes cluster, use the following command:

```bash
kubectl apply -f https://github.com/DotNetExtensions/OAuth20.Server.Host/kubernetes-manifest.yaml
```

#### Helm Installation

To install using Helm, use the following command:

```bash
helm repo add dotnetextensions https://dotnetextensions.com/oauth20/helm
helm install your-release-name dotnetextensions/oauth20serverhost --version x.x.x
```

Replace `x.x.x` with the desired version number.

#### Windows Service or IIS Installation

You can install your OAuth 2.0 Server as a Windows Service or IIS website by following the instructions in the [Hosted Application Repository](https://github.com/DotNetExtensions/OAuth20.Server.Host).

## Running Tests and Benchmarks

To run the unit tests included in the Library Repository, use the following command:

```bash
dotnet test
```

To run benchmarks, navigate to the benchmarks directory and use:

```bash
dotnet run -c Release
```

## Demo Projects

This project includes several demo projects within the Library Repository to help you get started with different OAuth 2.0 flows. You can find these in the `Demos` directory. Follow the README files within each demo project for setup and usage instructions.

## Project Structure

This project is divided into the following repositories:

- **Project Repository:** [DotNetExtensions/OAuth20](https://github.com/DotNetExtensions/OAuth20)
  - Essential Project Documentation

- **Library Repository:** [DotNetExtensions/OAuth20.Server](https://github.com/DotNetExtensions/OAuth20.Server)
  - Core Libraries
  - Data Source Libraries
  - UI Libraries
  - Infrastructure (tests, benchmarks, demos)
  - Available via NuGet and direct download.

- **Hosted Application Repository:** [DotNetExtensions/OAuth20.Server.Host](https://github.com/DotNetExtensions/OAuth20.Server.Host)
  - ASP.NET Core Application
  - Integration with core and UI libraries
  - Infrastructure (tests, demos)
  - Deployment support via Docker, Kubernetes, Helm, Windows Service, IIS.

## Development Workflow

We follow the GitFlow branching strategy for managing our development and release processes. For detailed information, please refer to our [GitFlow Guide](./GITFLOW.md).

## Roadmap

To understand our future plans and milestones, please refer to our [Roadmap](./ROADMAP.md).

## Task List

For a detailed breakdown of ongoing and upcoming tasks, please refer to our [Task List](./TASKLIST.md).

## Community and Support

For discussions, support, and feedback, please visit:

- [GitHub Project Page](https://github.com/orgs/DotNetExtensions/projects/17)
- [Project Website](https://dotnetextensions.com/oauth20)
- [Community Board](https://dotnetextensions.com/oauth20/community)
- [Support Page](https://dotnetextensions.com/oauth20/support)

## Contributing

We welcome contributions! Please read our [Contributing Guidelines](./CONTRIBUTING.md) to get started.

For detailed information on coding, formatting, and contribution conventions, please refer to our [Conventions](./CONVENTIONS.md) file.

Please note that all contributions are expected to adhere to our [Code of Conduct](./CODE_OF_CONDUCT.md).

## Security

We take the security of our project seriously. If you discover any security vulnerabilities, please report them by following the instructions in our [Security Policy](./SECURITY.md).

## License

This project is licensed under the [MIT License](./LICENSE).

## References

This project is based on the OAuth 2.0 Authorization Framework, specifically following the guidelines set forth in [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749).
