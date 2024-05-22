# Introduction 
---
Creating cloud-native applications demands thorough configuration to ensure they operate consistently and securely in various environments. .NET Aspire offers numerous helper methods and tools that simplify the management of settings for OpenTelemetry, health checks, environment variables, and other aspects, making the process more efficien.

# Service Defaults
---
 This project is intented to be used for .NET Aspire based development. This is a shared project and will be referenced by many other projects to provide a common set of services to all projects. For example, when building an API, you call the AddServiceDefaults method in the Program.cs file of your WebApi project. Similary, when building a WebApplication using MVC/Razor pages etc, you call the AddServiceDefaults method in the program.cs file of your WebApplication.

 ```charp
 builder.AddServiceDefaults();
 ```

 The AddServiceDefaults method handles the following concerns:

- Configures OpenTelemetry metrics and tracing.
- Add default health check endpoints.
- Add service discovery functionality.
- Configures HttpClient to work with service discovery.

You can customise the `Extensions.cs` file to add more capabiliteis as needed. For example Serilog functionality has been added to it, so it will be available to all projects that need it by referencing the project and calling the above method.

For more details, please refer to [.NET Aspire service defaults](https://learn.microsoft.com/en-us/dotnet/aspire/fundamentals/service-defaults#custom-service-defaults) documentation.