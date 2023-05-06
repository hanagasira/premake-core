Add any property to your visual studio project
This allows you to set properties that premake does not support without extending it

Values set at one time are sorted alphabetically

```lua
	props {
		Name1 = "value1",
		Name2 = "value2",
	}
```

### Parameters ###

Name and value is string

### Availability ###

Premake 5.0-beta3 or later.

### Applies To ###

The `config` scope.

### Examples ###

```lua
	language "C#"
	props {
		-- https://devblogs.microsoft.com/visualstudio/vs-toolbox-accelerate-your-builds-of-sdk-style-net-projects/
		AccelerateBuildsInVisualStudio = "true",
		-- https://learn.microsoft.com/en-us/visualstudio/ide/how-to-change-the-build-output-directory?view=vs-2022
		AppendTargetFrameworkToOutputPath = "false",
		-- https://learn.microsoft.com/en-us/dotnet/csharp/tutorials/nullable-reference-types
		Nullable = "enable",
	}
```
```lua
	language "C++"
	nuget {
		"Microsoft.Direct3D.D3D12:1.608.2"
	}
	props {
		-- https://devblogs.microsoft.com/directx/gettingstarted-dx12agility/#2-set-agility-sdk-parameters
		Microsoft_Direct3D_D3D12_D3D12SDKPath = "custom_path",
	}
```
