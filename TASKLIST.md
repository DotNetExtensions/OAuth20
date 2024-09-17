# DotNetExtensions.OAuth20 Task List

This document provides a structured task list for the **DotNetExtensions.OAuth20** project, organized by milestones and sprints. Each task is categorized with a sprint-wide number (No.), milestone-wide number, project-wide number, title, priority, size, estimate, and risk level.

For a high-level overview of the project's key goals and timeline, please refer to the [ROADMAP.md](./ROADMAP.md) file.

### Repository Structure
Tasks in this project are distributed across different repositories depending on their focus:
- **Project Documentation** and related files: [DotNetExtensions/OAuth20](https://github.com/DotNetExtensions/OAuth20)
- **Core Libraries** and OAuth 2.0 components: [DotNetExtensions/OAuth20.Server](https://github.com/DotNetExtensions/OAuth20.Server)
- **Hosted Authorization Server** and related infrastructure: [DotNetExtensions/OAuth20.Server.Host](https://github.com/DotNetExtensions/OAuth20.Server.Host)

Please explore the full set of project repositories here: [DotNetExtensions GitHub Repositories](https://github.com/orgs/DotNetExtensions/repositories).

### Task Management and Progress Tracking
You can track the ongoing progress of tasks and sprints in the GitHub project board for **DotNetExtensions.OAuth20**:
- **Project Board:** [DotNetExtensions/OAuth20 Project](https://github.com/orgs/DotNetExtensions/projects/17)

Each task will be addressed within the appropriate repository, ensuring clear separation of responsibilities across different components of the project.

## Milestone 1: Project Setup (08/26/2024 - 09/22/2024)

### Sprint 1 (08/26/2024 - 09/08/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 1.1           | 1           | Create Git Repositories and Initialize Structure | P0       | XS   | 2                | Low        |
| 2   | 1.2           | 2           | Create Project Description (README.md)           | P0       | S    | 4                | Low        |
| 3   | 1.3           | 3           | Create Repository Descriptions                   | P1       | S    | 4                | Low        |
| 4   | 1.4           | 4           | Add LICENSE File                                 | P0       | XS   | 2                | Low        |
| 5   | 1.5           | 5           | Add CONTRIBUTING.md File                         | P1       | S    | 4                | Low        |
| 6   | 1.6           | 6           | Add CHANGELOG.md File                            | P2       | S    | 3                | None       |
| 7   | 1.7           | 7           | Add TASKLIST.md File                             | P2       | S    | 3                | None       |
| 8   | 1.8           | 8           | Add ROADMAP.md File                              | P1       | S    | 4                | Low        |

### Sprint 2 (09/09/2024 - 09/22/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 1.9           | 9           | Add GITFLOW.md File                              | P1       | S    | 4                | Low        |
| 2   | 1.10          | 10          | Add CONVENTIONS.md File                          | P1       | S    | 4                | Low        |
| 3   | 1.11          | 11          | Create SECURITY.md File                          | P0       | S    | 3                | Low        |
| 4   | 1.12          | 12          | Add CODE_OF_CONDUCT.md File                      | P1       | XS   | 2                | Low        |
| 5   | 1.13          | 13          | Add ISSUE_TEMPLATE.md File                       | P1       | XS   | 2                | Low        |
| 6   | 1.14          | 14          | Add PULL_REQUEST_TEMPLATE.md File                | P1       | XS   | 2                | Low        |
| 7   | 1.15          | 15          | Add Repository Settings JSON File                | P2       | XS   | 2                | Low        |
| 8   | 1.16          | 16          | Create and Initialize DotNetExtensions Repository| P0       | S    | 4                | Medium     |
| 9   | 1.17          | 17          | Synchronize Data Across Repositories             | P1       | S    | 3                | Low        |
| 10  | 1.18          | 18          | Retrospective (Sprint 1)                         | P0       | S    | 4                | None       |

---

## Milestone 2: Create Initial Project Structure (09/23/2024 - 10/06/2024)

### Sprint 3 (09/23/2024 - 10/06/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 2.1           | 23          | Create Visual Studio Solution (.sln)             | P0       | XS   | 2                | None       |
| 2   | 2.2           | 24          | Create Solution and System Directories           | P1       | S    | 3                | None       |
| 3   | 2.3           | 25          | Create Empty C# Projects (.csproj)               | P1       | M    | 6                | None       |
| 4   | 2.4           | 26          | Sprint Synchronization (Sprint 3)                | P0       | XS   | 1                | None       |
| 5   | 2.5           | 27          | Retrospective (Sprint 3)                         | P0       | S    | 4                | None       |
| 6   | 2.6           | 28          | Retrospective (Milestone 2)                      | P0       | S    | 4                | None       |

---

## Milestone 3: Setup CI/CD Workflows (10/07/2024 - 10/20/2024)

### Sprint 4 (10/07/2024 - 10/20/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 3.1           | 29          | Define Required CI/CD Workflows                  | P0       | M    | 6                | Medium     |
| 2   | 3.2           | 30          | Create CI/CD Workflow for Build and Test         | P1       | M    | 8                | Medium     |
| 3   | 3.3           | 31          | Create CI/CD Workflow for Publishing Releases    | P1       | M    | 8                | Medium     |
| 4   | 3.4           | 32          | Create CI/CD Workflow for Dependency Checks      | P2       | S    | 4                | Low        |
| 5   | 3.5           | 33          | Create CI/CD Workflow for Code Quality Checks    | P1       | M    | 8                | Medium     |
| 6   | 3.6           | 34          | Create CI/CD Workflow for Documentation Checks   | P2       | S    | 4                | Low        |
| 7   | 3.7           | 35          | Sprint Synchronization (Sprint 4)                | P0       | XS   | 1                | None       |
| 8   | 3.8           | 36          | Retrospective (Sprint 4)                         | P0       | S    | 4                | None       |
| 9   | 3.9           | 37          | Retrospective (Milestone 3)                      | P0       | S    | 4                | None       |

---

## Milestone 4: Develop Core OAuth 2.0 Authorization Flow (10/21/2024 - 12/15/2024)

### Sprint 5 (10/21/2024 - 11/03/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 4.1           | 38          | Implement Domain Models                          | P0       | L    | 12               | Medium     |
| 2   | 4.2           | 39          | Implement Flow Models                            | P1       | L    | 12               | Medium     |
| 3   | 4.3           | 40          | Implement ClientSecretReaders Abstractions       | P2       | M    | 6                | Low        |
| 4   | 4.4           | 41          | Sprint Synchronization (Sprint 5)                | P0       | XS   | 1                | None       |
| 5   | 4.5           | 42          | Retrospective (Sprint 5)                         | P0       | S    | 4                | None       |

### Sprint 6 (11/04/2024 - 11/17/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 4.6           | 43          | Implement Data Sources and Storages Abstractions | P0       | L    | 12               | Medium     |
| 2   | 4.7           | 44          | Implement EndpointArgumentReaders and Endpoints Abstractions | P1    | M    | 8                | Medium     |
| 3   | 4.8           | 45          | Implement Errors and Flows Abstractions          | P2       | M    | 10               | Medium     |
| 4   | 4.9           | 46          | Sprint Synchronization (Sprint 6)                | P0       | XS   | 1                | None       |
| 5   | 4.10          | 47          | Retrospective (Sprint 6)                         | P0       | S    | 4                | None       |

### Sprint 7 (11/18/2024 - 12/01/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 4.11          | 48          | Implement Interceptors, Providers, and Server Information Abstractions | P0 | L    | 12               | Medium     |
| 2   | 4.12          | 49          | Implement ServerSigningCredentials and Services Abstractions | P1   | L    | 12               | Medium     |
| 3   | 4.13          | 50          | Implement TokenBuilders Abstractions             | P2       | M    | 8                | Medium     |
| 4   | 4.14          | 51          | Sprint Synchronization (Sprint 7)                | P0       | XS   | 1                | None       |
| 5   | 4.15          | 52          | Implement Validations/Validators Abstractions    | P1       | M    | 8                | Medium     |
| 6   | 4.16          | 53          | Retrospective (Sprint 7)                         | P0       | S    | 4                | None       |

### Sprint 8 (12/02/2024 - 12/15/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 4.17          | 54          | Implement Utilities (EncryptionUtilities, HashingUtilities, etc.) | P0  | M    | 8                | Low        |
| 2   | 4.18          | 55          | Implement Options (37 Classes and Enums)         | P1       | L    | 12               | Medium     |
| 3   | 4.19          | 56          | Implement Extensions                             | P2       | M    | 8                | Medium     |
| 4   | 4.20          | 57          | Sprint Synchronization (Sprint 8)                | P0       | XS   | 1                | None       |
| 5   | 4.21          | 58          | Implement Errors and Validators                  | P1       | M    | 8                | Medium     |
| 6   | 4.22          | 59          | Retrospective (Sprint 8)                         | P0       | S    | 4                | None       |

---

## Milestone 5: Create Integration Tests (12/16/2024 - 12/29/2024)

### Sprint 9 (12/16/2024 - 12/29/2024)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 5.1           | 60          | Design Integration Test Cases                    | P0       | M    | 6                | Medium     |
| 2   | 5.2           | 61          | Implement Integration Tests for Authorization Code Flow | P1   | L    | 12               | Medium     |
| 3   | 5.3           | 62          | Implement Integration Tests for Client Credentials Flow | P2  | M    | 10               | Medium     |
| 4   | 5.4           | 63          | Sprint Synchronization (Sprint 9)                | P0       | XS   | 1                | None       |
| 5   | 5.5           | 64          | Implement Integration Tests for Refresh Token Flow | P1     | M    | 8                | Medium     |
| 6   | 5.6           | 65          | Retrospective (Sprint 9)                         | P0       | S    | 4                | None       |

---

## Milestone 6: Create Personal Account UI Using Blazor (12/30/2024 - 01/12/2025)

### Sprint 10 (12/30/2024 - 01/12/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 6.1           | 66          | Design Personal Account UI                       | P0       | M    | 8                | Medium     |
| 2   | 6.2           | 67          | Implement User Profile Management                | P1       | L    | 12               | Medium     |
| 3   | 6.3           | 68          | Implement OAuth Consents Management              | P2       | L    | 12               | Medium     |
| 4   | 6.4           | 69          | Sprint Synchronization (Sprint 10)               | P0       | XS   | 1                | None       |
| 5   | 6.5           | 70          | Implement Account Security Settings              | P1       | M    | 10               | Medium     |
| 6   | 6.6           | 71          | Retrospective (Sprint 10)                        | P0       | S    | 4                | None       |

---

## Milestone 7: Create Admin Panel UI Using Blazor (01/13/2025 - 01/26/2025)

### Sprint 11 (01/13/2025 - 01/26/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 7.1           | 72          | Design Admin Panel UI                            | P0       | M    | 8                | Medium     |
| 2   | 7.2           | 73          | Implement User Management Features               | P1       | L    | 12               | Medium     |
| 3   | 7.3           | 74          | Implement OAuth Client Management                | P2       | L    | 12               | Medium     |
| 4   | 7.4           | 75          | Sprint Synchronization (Sprint 11)               | P0       | XS   | 1                | None       |
| 5   | 7.5           | 76          | Implement System Settings Management             | P1       | M    | 10               | Medium     |
| 6   | 7.6           | 77          | Retrospective (Sprint 11)                        | P0       | S    | 4                | None       |

---

## Milestone 8: Create Demo (Quickstart) Projects (01/27/2025 - 02/09/2025)

### Sprint 12 (01/27/2025 - 02/09/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 8.1           | 78          | Design Demo Project for Basic OAuth 2.0 Flow     | P0       | M    | 8                | Low        |
| 2   | 8.2           | 79          | Implement Demo Project for Authorization Code Flow | P1     | M    | 10               | Low        |
| 3   | 8.3           | 80          | Implement Demo Project for Client Credentials Flow | P2    | M    | 10               | Low        |
| 4   | 8.4           | 81          | Sprint Synchronization (Sprint 12)               | P0       | XS   | 1                | None       |
| 5   | 8.5           | 82          | Implement Demo Project for Refresh Token Flow    | P1       | M    | 8                | Low        |
| 6   | 8.6           | 83          | Retrospective (Sprint 12)                        | P0       | S    | 4                | None       |

---

## Milestone 9: Create Libraries for Different Data Sources and Providers (02/10/2025 - 02/23/2025)

### Sprint 13 (02/10/2025 - 02/23/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 9.1           | 84          | Implement Library for SQL Server Data Source     | P0       | M    | 10               | Low        |
| 2   | 9.2           | 85          | Implement Library for PostgreSQL Data Source     | P1       | M    | 10               | Low        |
| 3   | 9.3           | 86          | Implement Library for MySQL Data Source          | P2       | M    | 10               | Low        |
| 4   | 9.4           | 87          | Sprint Synchronization (Sprint 13)               | P0       | XS   | 1                | None       |
| 5   | 9.5           | 88          | Implement Library for In-Memory Data Source      | P1       | M    | 8                | Low        |
| 6   | 9.6           | 89          | Retrospective (Sprint 13)                        | P0       | S    | 4                | None       |

---

## Milestone 10: Carry Out a Security Audit, Tests, and Vulnerability Investigations (02/24/2025 - 03/09/2025)

### Sprint 14 (02/24/2025 - 03/09/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 10.1          | 90          | Perform Initial Security Audit                   | P0       | L    | 12               | High       |
| 2   | 10.2          | 91          | Conduct Penetration Testing                      | P1       | L    | 12               | High       |
| 3   | 10.3          | 92          | Investigate and Document Vulnerabilities          | P2       | M    | 10               | High       |
| 4   | 10.4          | 93          | Sprint Synchronization (Sprint 14)               | P0       | XS   | 1                | None       |
| 5   | 10.5          | 94          | Retrospective (Sprint 14)                        | P0       | S    | 4                | None       |

---

## Milestone 11: Adjust the Solution Based on Tests and Security Audit (03/10/2025 - 03/23/2025)

### Sprint 15 (03/10/2025 - 03/23/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 11.1          | 95          | Implement Adjustments for Security Vulnerabilities (Part 1) | P0 | M    | 10               | High       |
| 2   | 11.2          | 96          | Implement Adjustments for Security Vulnerabilities (Part 2) | P1 | M    | 10               | High       |
| 3   | 11.3          | 97          | Implement Adjustments Based on Integration Tests  | P2       | M    | 8                | Medium     |
| 4   | 11.4          | 98          | Sprint Synchronization (Sprint 15)               | P0       | XS   | 1                | None       |
| 5   | 11.5          | 99          | Retrospective (Sprint 15)                        | P0       | S    | 4                | None       |

---

## Milestone 12: Prepare ASP.NET Core Hosted Authorization Server (03/24/2025 - 04/06/2025)

### Sprint 16 (03/24/2025 - 04/06/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 12.1          | 100         | Implement ASP.NET Core Hosted Server             | P0       | L    | 12               | Medium     |
| 2   | 12.2          | 101         | Implement Tests and Benchmarks for Hosted Server | P1       | M    | 10               | Medium     |
| 3   | 12.3          | 102         | Develop Docker Image for Hosted Server           | P2       | M    | 10               | Medium     |
| 4   | 12.4          | 103         | Sprint Synchronization (Sprint 16)               | P0       | XS   | 1                | None       |
| 5   | 12.5          | 104         | Develop Kubernetes Manifests and Helm Charts     | P1       | M    | 8                | Medium     |
| 6   | 12.6          | 105         | Retrospective (Sprint 16)                        | P0       | S    | 4                | None       |

---

## Milestone 13: Develop the Website Dedicated to the Project (04/07/2025 - 04/20/2025)

### Sprint 17 (04/07/2025 - 04/20/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 13.1          | 106         | Design Project Website                           | P0       | M    | 8                | Medium     |
| 2   | 13.2          | 107         | Implement Documentation Pages                    | P1       | M    | 12               | Low        |
| 3   | 13.3          | 108         | Implement Community Board                        | P2       | M    | 10               | Medium     |
| 4   | 13.4          | 109         | Sprint Synchronization (Sprint 17)               | P0       | XS   | 1                | Low        |
| 5   | 13.5          | 110         | Implement Project Guidelines and Contribution Pages | P1     | M    | 8                | Low        |
| 6   | 13.6          | 111         | Retrospective (Sprint 17)                        | P0       | S    | 4                | Low        |

---

## Milestone 14: Preparing for the First Release (04/21/2025 - 05/04/2025)

### Sprint 18 (04/21/2025 - 05/04/2025)

| No. | Milestone No. | Project No. | Title                                            | Priority | Size | Estimate (hours) | Risk Level |
| --- | ------------- | ----------- | ------------------------------------------------ | -------- | ---- | ---------------- | ---------- |
| 1   | 14.1          | 112         | Conduct Final Review of the Solution             | P0       | M    | 12               | Medium     |
| 2   | 14.2          | 113         | Prepare Release Notes                            | P1       | S    | 6                | Low        |
| 3   | 14.3          | 114         | Implement Automatic Deployment to NuGet Gallery  | P1       | M    | 8                | Medium     |
| 4   | 14.4          | 115         | Implement Automatic Deployment to DockerHub      | P2       | M    | 8                | Medium     |
| 5   | 14.5          | 116         | Implement Automatic Deployment to GitHub Releases | P1      | M    | 8                | Medium     |
| 6   | 14.6          | 117         | Sprint Synchronization (Sprint 18)               | P0       | XS   | 1                | Low        |
| 7   | 14.7          | 118         | Retrospective (Sprint 18)                        | P0       | S    | 4                | Low        |
