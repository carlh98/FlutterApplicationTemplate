﻿# Uno Platform Application Template

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?style=flat-square)](LICENSE) ![Version](https://img.shields.io/nuget/v/NV.Templates.Mobile?style=flat-square) ![Downloads](https://img.shields.io/nuget/dt/NV.Templates.Mobile?style=flat-square)

This is a mobile app project template using [Flutter](https://github.com/flutter) and the latest Flutter/Dart practices.

- It uses the MVVM pattern.
- Code is organized by [application layer](doc/Architecture.md#Solution-Structure).
- It comes with [dependency injection](doc/DependencyInjection.md).
- There are built-in [logs](doc/Logging.md) and [diagnostic tools](doc/Diagnostics.md).
- There is scaffolding code showing sample features.
  When you run as-is, you get a _Dad Jokes_ application.

## Preview
From left to right: WinUI, iOS, and Android.
![Platform-Comparison-Preview](https://user-images.githubusercontent.com/39710855/264705525-d070952c-04c7-4f4a-b6af-957f8415fb3e.png)
> Note that scaling was adjusted to better fit this preview and therefore this image isn't representative of the actual device sizes.

### Diagnostic Tools
![Diagnostics-Overlay-Preview](https://user-images.githubusercontent.com/39710855/264691340-dbc9d137-a199-4969-94d7-7dd430e08da7.gif)

## Requirements

Visual Studio Code with Flutter are required.

This template largely relies on Flutter, if you want to make sure you got everything installed correctly on your machine, we encourage you to use `flutter doctor -v`, the documentation is available [here](https://docs.flutter.dev/)

## Getting Started

We use a custom PowerShell script and a Dart package to easily create new projects. It simplifies the **project renaming**.

### Generate a new project

1. Make sure you cloned the latest version of this repository.

2. Make sure you have PowerShell installed.

   > 💡 For Windows, you can run `powershell` to verify. You can install it with the command `winget install --id Microsoft.Powershell --source winget`.
   > 💡 For Mac, you can run `pwsh` to verify. You can install it with Homebrew `brew install powershell/tap/powershell`.

3. To run the script and create a new project, run the following command in the cloned `FlutterApplicationTemplate` repository.

   `powershell -File ".\tools\copyApplicationTemplate.ps1" -sourceProjectDir C:\P\FlutterApplicationTemplate -destDir C:\P -projectName TODO -appName TODO -packageName TODO -organization Org`

   > 💡 The organization parameter is optional (Only used for the Windows platform).

   The following options are available when running the command.

   - To get help: `Get-Help .\tools\copyApplicationTemplate.ps1`

### Next Steps

1. Open the `README.md` and complete the documentation TODOs.
2. Open the directory with Visual Studio Code.
3. In Visual Studio Code, go to the **VIEW** menu and open the **Problems** to get hints on next steps.
   
   This template comes with several pointers on what you're most likely to change next.
   
   ![](doc/images/VisualStudioTaskListForNextSteps.PNG)

## Architecture and Recipes
This repository provides documentation on different topics under the [doc](doc/) folder.

### Architecture

The software architecture of the application is documented in the [Architecture](doc/Architecture.md) document.

### Summary of Recipes
| Topic | Recipe/Implementation |
|-|-|
UI Framework | [WinUI](https://learn.microsoft.com/en-us/windows/apps/winui/)<br/>[Uno Platform](https://platform.uno/)
[MVVM](doc/Architecture.md#mvvm---viewmodels) | [Chinook.DynamicMvvm](https://github.com/nventive/Chinook.DynamicMvvm)
[Dependency Injection](doc/DependencyInjection.md) | [Microsoft.Extensions.Hosting](https://www.nuget.org/packages/Microsoft.Extensions.Hosting)<br/>[Microsoft.Extensions.DependencyInjection](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.dependencyinjection)
[Configuration](doc/Configuration.md) | [Microsoft.Extensions.Configuration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration)
[Runtime Environments](doc/Environments.md) | [Microsoft.Extensions.Configuration](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.configuration)
Design System | [Uno.Material](https://platform.uno/docs/articles/external/uno.themes/doc/material-getting-started.html)<br/>[Material Design](https://m3.material.io/)
[HTTP](doc/HTTP.md) | [Refit](https://github.com/reactiveui/refit)<br/>[Microsoft.Extensions.Http](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.http)
[Async Data Loading](doc/DataLoading.md) | [Chinook.DataLoader](https://github.com/nventive/Chinook.DataLoader)
[Logging](doc/Logging.md) | [Serilog](https://serilog.net/)<br/>[Microsoft.Extensions.Logging](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.logging)
[Testing](doc/Testing.md) | [xUnit](https://github.com/xunit/xunit)
[Serialization](doc/Serialization.md) | [System.Text.Json](https://docs.microsoft.com/en-us/dotnet/api/system.text.json)
[Localization](doc/Localization.md) | [Microsoft.Extensions.Localization](https://learn.microsoft.com/en-us/dotnet/api/microsoft.extensions.localization)
[Navigation](doc/Architecture.md#navigation) | [Chinook.Navigation](https://github.com/nventive/Chinook.Navigation)<br/>[Chinook.BackButtonManager](https://github.com/nventive/Chinook.BackButtonManager)
[Validation](doc/Validation.md) | [FluentValidation](https://fluentvalidation.net/)
[App Reviews](doc/Reviews.md) | [ReviewService](https://github.com/nventive/ReviewService)

## Debugging or Testing the Template
Here's how to install the template directly from the code, in the case that you want to modify it and would like to test your changes.

## Changelog

Please consult the [CHANGELOG](CHANGELOG.md) for more information about the version history.

## License

This project is licensed under the Apache 2.0 license. See the [LICENSE](LICENSE) for details.

## Contributing

Please read [CONTRIBUTING](CONTRIBUTING.md) for details on the process for contributing to this project.

Be mindful of our [Code of Conduct](CODE_OF_CONDUCT.md).
