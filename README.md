# RoslynScriptRunner
<img src="https://www.nuget.org/Content/gallery/img/logo-header.svg?sanitize=true" height="30px">
  
RoslynScriptRunner is a versatile C# script execution library based on the Roslyn compiler, enabling dynamic runtime execution of C# code snippets without the need for pre-compilation.

### Download
RoslynScriptRunner is available as [Nuget Package](https://www.nuget.org/packages/ZjzMisaka.RoslynScriptRunner/) now.
### Getting started
**Hello World**
``` csharp
string codeHelloWorld = @"
using System;
class Run
{
    public void Main()
    {
        Console.WriteLine(""Hello World"");
    }
}
";
RoslynScriptRunner.ScriptRunner.Run(codeHelloWorld);
```
#### API
``` csharp
object Run(string code, RunOption runOption = null)
```
``` csharp
Task<object> RunAsync(string code, RunOption runOption = null)
```
``` csharp
object Run(ICollection<string> codeList, RunOption runOption = null)
```
``` csharp
Task<object> RunAsync(ICollection<string> codeList, RunOption runOption = null)
```
``` csharp
object Run(RunOption runOption)
```
``` csharp
Task<object> RunAsync(RunOption runOption)
```
``` csharp
InstanceObject GetInstanceObject(string code, RunOption runOption = null)
```
``` csharp
InstanceObject GetInstanceObject(ICollection<string> codeList, RunOption runOption = null)
```
#### Options
**RoslynScriptRunner.RunOption**
``` csharp
object[] paramList;
ICollection<string> extraDllFolderList;
ICollection<string> extraDllFileList;
string methodName;
string className;
InstanceObject instanceObject;
```
**Useage**
``` csharp
RoslynScriptRunner.RunOption runOption = new RoslynScriptRunner.RunOption(...);
RoslynScriptRunner.ScriptRunner.Run(code, runOption);
```
