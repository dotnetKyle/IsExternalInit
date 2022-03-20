# IsExternalInit
The is external init class (for allowing .Net Standard 2.0 to work with the newest C# version).

In .NET Standard 2.0, change your .csproj to use the latest lang version:

```xml
  <PropertyGroup>
    <TargetFramework>netstandard2.0</TargetFramework>
	<LangVersion>latest</LangVersion>
	<Nullable>enable</Nullable>
	<ImplicitUsings>enable</ImplicitUsings>
  </PropertyGroup>
```

Install the nuget package: 

Project Reference:

```xml
<PackageReference Include="dotnetKyle.IsExternalInit" version="1.0.0" />
```

CLI:

```
dotnet add package dotnetKyle.IsExternalInit
```

Package Manager Console:

```
Install-Package dotnetKyle.IsExternalInit
```

To test, rebuild your project to get `init` to start working or create a new record:

```csharp 
public record MyRecord(string MyString);
```

Then build your project.