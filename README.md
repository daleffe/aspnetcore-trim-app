# ASP.NET Core Trim App

C# ASP.NET Core app standalone/trimmed sample

## How to
Edit your prject file (**.csproj**) and add follow lines at *PropertyGroup*:
```csharp
<PublishSingleFile>true</PublishSingleFile>
<RuntimeIdentifier>linux-arm64</RuntimeIdentifier>
<PublishReadyToRun>true</PublishReadyToRun>
<PublishTrimmed>true</PublishTrimmed>
```
Then run:
```console
dotnet publish --runtime linux-arm64 --self-contained -p:PublishTrimmed=true
```
With this sample, the binary will be available at **bin/Release/net8.0/linux-arm64/publish/**.

## Notes
* Change *RuntimeIdentifier* according to your target arch;
* Trimming is fully supported in .NET 6 and later versions. In .NET Core 3.1 and .NET 5, trimming was an experimental feature;
* Trimming is only available to apps that are published self-contained.
