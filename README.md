# MyWebApp

A simple ASP.NET Core web application used to learn framework-dependent deployment.
See [Exercise - Publish for framework-dependent deployment - Training | Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/publish-aspnetcore-app/3-exercise-framework-dependent) for more details.

## Quick Start

1. **Run the application:**

   ```powershell
   dotnet run --project MyWebApp
   ```

2. **Build for release:**

   ```powershell
   dotnet build -c Release
   ```

3. **Publish (framework-dependent):**
Run this in the root directory of specific project folder.
See [Microsoft Learn documentation](https://learn.microsoft.com/en-us/training/modules/publish-aspnetcore-app/3-exercise-framework-dependent)

   ```powershell
   dotnet publish -c Release -o publish-fd   
   ```

## What's Framework-Dependent Deployment?

- Requires .NET runtime to be installed on the target machine
- Smaller deployment size
- Automatic security updates through runtime updates
- Cross-platform compatible

## Project Info

- **Framework:** .NET 9.0
- **Type:** ASP.NET Core Web Application
- **Default URL:** https://localhost:5001
