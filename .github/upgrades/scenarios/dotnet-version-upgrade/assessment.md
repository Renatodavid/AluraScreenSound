# Projects and dependencies analysis

This document provides a comprehensive overview of the projects and their dependencies in the context of upgrading to .NETCoreApp,Version=v8.0.

## Table of Contents

- [Executive Summary](#executive-Summary)
  - [Highlevel Metrics](#highlevel-metrics)
  - [Projects Compatibility](#projects-compatibility)
  - [Package Compatibility](#package-compatibility)
  - [API Compatibility](#api-compatibility)
- [Aggregate NuGet packages details](#aggregate-nuget-packages-details)
- [Top API Migration Challenges](#top-api-migration-challenges)
  - [Technologies and Features](#technologies-and-features)
  - [Most Frequent API Issues](#most-frequent-api-issues)
- [Projects Relationship Graph](#projects-relationship-graph)
- [Project Details](#project-details)

  - [ScreenSound.API\ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj)
  - [ScreenSound.Shared.Dados\ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj)
  - [ScreenSound.Shared.Modelos\ScreenSound.Shared.Modelos.csproj](#screensoundsharedmodelosscreensoundsharedmodeloscsproj)
  - [ScreenSound.Web\ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj)
  - [ScreenSound\ScreenSound.csproj](#screensoundscreensoundcsproj)


## Executive Summary

### Highlevel Metrics

| Metric | Count | Status |
| :--- | :---: | :--- |
| Total Projects | 5 | 0 require upgrade |
| Total NuGet Packages | 13 | All compatible |
| Total Code Files | 51 |  |
| Total Code Files with Incidents | 0 |  |
| Total Lines of Code | 1926 |  |
| Total Number of Issues | 0 |  |
| Estimated LOC to modify | 0+ | at least 0,0% of codebase |

### Projects Compatibility

| Project | Target Framework | Difficulty | Package Issues | API Issues | Est. LOC Impact | Description |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| [ScreenSound.API\ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj) | net8.0 | ✅ None | 0 | 0 |  | AspNetCore, Sdk Style = True |
| [ScreenSound.Shared.Dados\ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj) | net8.0 | ✅ None | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [ScreenSound.Shared.Modelos\ScreenSound.Shared.Modelos.csproj](#screensoundsharedmodelosscreensoundsharedmodeloscsproj) | net8.0 | ✅ None | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [ScreenSound.Web\ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj) | net8.0 | ✅ None | 0 | 0 |  | AspNetCore, Sdk Style = True |
| [ScreenSound\ScreenSound.csproj](#screensoundscreensoundcsproj) | net8.0 | ✅ None | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |

### Package Compatibility

| Status | Count | Percentage |
| :--- | :---: | :---: |
| ✅ Compatible | 13 | 100,0% |
| ⚠️ Incompatible | 0 | 0,0% |
| 🔄 Upgrade Recommended | 0 | 0,0% |
| ***Total NuGet Packages*** | ***13*** | ***100%*** |

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

## Aggregate NuGet packages details

| Package | Current Version | Suggested Version | Projects | Description |
| :--- | :---: | :---: | :--- | :--- |
| Microsoft.AspNetCore.Components.WebAssembly | 8.0.0 |  | [ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj) | ✅Compatible |
| Microsoft.AspNetCore.Components.WebAssembly.DevServer | 8.0.0 |  | [ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj) | ✅Compatible |
| Microsoft.AspNetCore.OpenApi | 8.0.0 |  | [ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj) | ✅Compatible |
| Microsoft.Data.SqlClient | 5.1.2 |  | [ScreenSound.csproj](#screensoundscreensoundcsproj)<br/>[ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj) | ✅Compatible |
| Microsoft.EntityFrameworkCore.Design | 7.0.13 |  | [ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj)<br/>[ScreenSound.csproj](#screensoundscreensoundcsproj) | ✅Compatible |
| Microsoft.EntityFrameworkCore.Proxies | 7.0.14 |  | [ScreenSound.csproj](#screensoundscreensoundcsproj)<br/>[ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj) | ✅Compatible |
| Microsoft.EntityFrameworkCore.SqlServer | 7.0.13 |  | [ScreenSound.csproj](#screensoundscreensoundcsproj)<br/>[ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj) | ✅Compatible |
| Microsoft.EntityFrameworkCore.Tools | 7.0.13 |  | [ScreenSound.csproj](#screensoundscreensoundcsproj)<br/>[ScreenSound.Shared.Dados.csproj](#screensoundshareddadosscreensoundshareddadoscsproj) | ✅Compatible |
| Microsoft.Extensions.Http | 8.0.0 |  | [ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj) | ✅Compatible |
| MudBlazor | 6.11.1 |  | [ScreenSound.Web.csproj](#screensoundwebscreensoundwebcsproj) | ✅Compatible |
| Swashbuckle.AspNetCore | 6.5.0 |  | [ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj) | ✅Compatible |
| Swashbuckle.AspNetCore.Swagger | 6.5.0 |  | [ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj) | ✅Compatible |
| Swashbuckle.AspNetCore.SwaggerUI | 6.5.0 |  | [ScreenSound.API.csproj](#screensoundapiscreensoundapicsproj) | ✅Compatible |

## Top API Migration Challenges

### Technologies and Features

| Technology | Issues | Percentage | Migration Path |
| :--- | :---: | :---: | :--- |

### Most Frequent API Issues

| API | Count | Percentage | Category |
| :--- | :---: | :---: | :--- |

## Projects Relationship Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart LR
    P1["<b>📦&nbsp;ScreenSound.csproj</b><br/><small>net8.0</small>"]
    P2["<b>📦&nbsp;ScreenSound.API.csproj</b><br/><small>net8.0</small>"]
    P3["<b>📦&nbsp;ScreenSound.Shared.Modelos.csproj</b><br/><small>net8.0</small>"]
    P4["<b>📦&nbsp;ScreenSound.Shared.Dados.csproj</b><br/><small>net8.0</small>"]
    P5["<b>📦&nbsp;ScreenSound.Web.csproj</b><br/><small>net8.0</small>"]
    P1 --> P3
    P1 --> P4
    P2 --> P3
    P2 --> P4
    P4 --> P3
    click P1 "#screensoundscreensoundcsproj"
    click P2 "#screensoundapiscreensoundapicsproj"
    click P3 "#screensoundsharedmodelosscreensoundsharedmodeloscsproj"
    click P4 "#screensoundshareddadosscreensoundshareddadoscsproj"
    click P5 "#screensoundwebscreensoundwebcsproj"

```

## Project Details

<a id="screensoundapiscreensoundapicsproj"></a>
### ScreenSound.API\ScreenSound.API.csproj

#### Project Info

- **Current Target Framework:** net8.0✅
- **SDK-style**: True
- **Project Kind:** AspNetCore
- **Dependencies**: 2
- **Dependants**: 0
- **Number of Files**: 29
- **Lines of Code**: 347
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

#### Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["ScreenSound.API.csproj"]
        MAIN["<b>📦&nbsp;ScreenSound.API.csproj</b><br/><small>net8.0</small>"]
        click MAIN "#screensoundapiscreensoundapicsproj"
    end
    subgraph downstream["Dependencies (2"]
        P3["<b>📦&nbsp;ScreenSound.Shared.Modelos.csproj</b><br/><small>net8.0</small>"]
        P4["<b>📦&nbsp;ScreenSound.Shared.Dados.csproj</b><br/><small>net8.0</small>"]
        click P3 "#screensoundsharedmodelosscreensoundsharedmodeloscsproj"
        click P4 "#screensoundshareddadosscreensoundshareddadoscsproj"
    end
    MAIN --> P3
    MAIN --> P4

```

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

<a id="screensoundshareddadosscreensoundshareddadoscsproj"></a>
### ScreenSound.Shared.Dados\ScreenSound.Shared.Dados.csproj

#### Project Info

- **Current Target Framework:** net8.0✅
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 1
- **Dependants**: 2
- **Number of Files**: 17
- **Lines of Code**: 1159
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

#### Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (2)"]
        P1["<b>📦&nbsp;ScreenSound.csproj</b><br/><small>net8.0</small>"]
        P2["<b>📦&nbsp;ScreenSound.API.csproj</b><br/><small>net8.0</small>"]
        click P1 "#screensoundscreensoundcsproj"
        click P2 "#screensoundapiscreensoundapicsproj"
    end
    subgraph current["ScreenSound.Shared.Dados.csproj"]
        MAIN["<b>📦&nbsp;ScreenSound.Shared.Dados.csproj</b><br/><small>net8.0</small>"]
        click MAIN "#screensoundshareddadosscreensoundshareddadoscsproj"
    end
    subgraph downstream["Dependencies (1"]
        P3["<b>📦&nbsp;ScreenSound.Shared.Modelos.csproj</b><br/><small>net8.0</small>"]
        click P3 "#screensoundsharedmodelosscreensoundsharedmodeloscsproj"
    end
    P1 --> MAIN
    P2 --> MAIN
    MAIN --> P3

```

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

<a id="screensoundsharedmodelosscreensoundsharedmodeloscsproj"></a>
### ScreenSound.Shared.Modelos\ScreenSound.Shared.Modelos.csproj

#### Project Info

- **Current Target Framework:** net8.0✅
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 0
- **Dependants**: 3
- **Number of Files**: 3
- **Lines of Code**: 99
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

#### Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (3)"]
        P1["<b>📦&nbsp;ScreenSound.csproj</b><br/><small>net8.0</small>"]
        P2["<b>📦&nbsp;ScreenSound.API.csproj</b><br/><small>net8.0</small>"]
        P4["<b>📦&nbsp;ScreenSound.Shared.Dados.csproj</b><br/><small>net8.0</small>"]
        click P1 "#screensoundscreensoundcsproj"
        click P2 "#screensoundapiscreensoundapicsproj"
        click P4 "#screensoundshareddadosscreensoundshareddadoscsproj"
    end
    subgraph current["ScreenSound.Shared.Modelos.csproj"]
        MAIN["<b>📦&nbsp;ScreenSound.Shared.Modelos.csproj</b><br/><small>net8.0</small>"]
        click MAIN "#screensoundsharedmodelosscreensoundsharedmodeloscsproj"
    end
    P1 --> MAIN
    P2 --> MAIN
    P4 --> MAIN

```

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

<a id="screensoundwebscreensoundwebcsproj"></a>
### ScreenSound.Web\ScreenSound.Web.csproj

#### Project Info

- **Current Target Framework:** net8.0✅
- **SDK-style**: True
- **Project Kind:** AspNetCore
- **Dependencies**: 0
- **Dependants**: 0
- **Number of Files**: 38
- **Lines of Code**: 124
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

#### Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["ScreenSound.Web.csproj"]
        MAIN["<b>📦&nbsp;ScreenSound.Web.csproj</b><br/><small>net8.0</small>"]
        click MAIN "#screensoundwebscreensoundwebcsproj"
    end

```

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

<a id="screensoundscreensoundcsproj"></a>
### ScreenSound\ScreenSound.csproj

#### Project Info

- **Current Target Framework:** net8.0✅
- **SDK-style**: True
- **Project Kind:** DotNetCoreApp
- **Dependencies**: 2
- **Dependants**: 0
- **Number of Files**: 7
- **Lines of Code**: 197
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

#### Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["ScreenSound.csproj"]
        MAIN["<b>📦&nbsp;ScreenSound.csproj</b><br/><small>net8.0</small>"]
        click MAIN "#screensoundscreensoundcsproj"
    end
    subgraph downstream["Dependencies (2"]
        P3["<b>📦&nbsp;ScreenSound.Shared.Modelos.csproj</b><br/><small>net8.0</small>"]
        P4["<b>📦&nbsp;ScreenSound.Shared.Dados.csproj</b><br/><small>net8.0</small>"]
        click P3 "#screensoundsharedmodelosscreensoundsharedmodeloscsproj"
        click P4 "#screensoundshareddadosscreensoundshareddadoscsproj"
    end
    MAIN --> P3
    MAIN --> P4

```

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 0 |  |
| ***Total APIs Analyzed*** | ***0*** |  |

