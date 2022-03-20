# Easily Add record support to a .NET Standard library

How to add C# `record` support or `init` support in a .NET Standard 2.0 library.

Just change your project to use the latest C# language version and add this nuget package.

## Use latest C# version:

In .NET Standard 2.0, change your .csproj to use the latest lang version by adding the `LangVersion` element:

```xml
<PropertyGroup>
  <TargetFramework>netstandard2.0</TargetFramework>
  <LangVersion>latest</LangVersion>
</PropertyGroup>
```

## Install the nuget package: 

> As a Project Reference:
> 
> ```xml
> <PackageReference Include="dotnetKyle.IsExternalInit" version="1.0.0" />
> ```
> 
> Using the CLI:
> 
> ```sh
> dotnet add package dotnetKyle.IsExternalInit
> ```
> 
> Using the Package Manager Console:
> 
> ```pwsh
> Install-Package dotnetKyle.IsExternalInit
> ```

## Testing:

To test, rebuild your project to get your `record` or `init` setter to start working.

Alternatively, you can create a test record:

```csharp
public record MyRecord(string MyString);
```

Then build your project.
