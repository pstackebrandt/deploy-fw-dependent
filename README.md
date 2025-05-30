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

4. **Publish (self-contained):**
Run this in the root directory of specific project folder.

   ```powershell
   dotnet publish -c Release -r win-x64 -o publish-scd-win64 --self-contained
   ```

5. **Publish (self-contained for Linux):**
Run this in the root directory of specific project folder.

   ```powershell
   dotnet publish -c Release -r linux-x64 -o publish-scd-linux64 --self-contained
   ```

## Command Explanation

We get a folder with ca. 100 MB size.

In the previous command:

- **`-c Release`** - Specifies that the app should be built in release mode. This optimizes the app for performance.
- **`-r win-x64`** - Specifies that the app should be published for 64-bit Windows. `win-x64` is the runtime identifier (RID) for 64-bit Windows, so the app is published as a self-contained deployment for 64-bit Windows.
- **`-o publish-scd-win64`** - Specifies the output directory for the published app.
- **`--self-contained`** - Specifies that the app should be published as a self-contained deployment.

This command builds and publishes the app as a self-contained deployment for 64-bit Windows to the `MyWebApp/publish-scd-win64` directory.

For the Linux self-contained deployment command:

- **`-r linux-x64`** - Specifies that the app should be published for 64-bit Linux.
- **`-o publish-scd-linux64`** - Specifies the output directory for the published app.

This command builds and publishes the app as a self-contained deployment for 64-bit Linux to the `MyWebApp/publish-scd-linux64` directory.

The list of files in the publish-scd-linux64 directory is similar to the list of files in the publish-scd-win64 directory, but the executable file is named MyWebApp instead of MyWebApp.exe. This is because Linux doesn't use file extensions to determine file types. After you deploy the app to a Linux server, you'll need to grant execute permission to the MyWebApp file with the chmod +x command before it can run.

## What's Framework-Dependent Deployment?

- Requires .NET runtime to be installed on the target machine
- Smaller deployment size
- Automatic security updates through runtime updates
- Cross-platform compatible

## What's Self-Contained Deployment?

- Includes the .NET runtime with your application
- Larger deployment size but no runtime dependencies
- Target machine doesn't need .NET installed
- Platform-specific (e.g., win-x64, linux-x64, osx-x64)

## Project Info

- **Framework:** .NET 9.0
- **Type:** ASP.NET Core Web Application
- **Default URL:** [https://localhost:5001](https://localhost:5001)
