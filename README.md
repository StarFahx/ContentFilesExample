# ContentFiles Generated Inconsistently When Using TargetFramework vs TargetFrameworks

Recreation steps:
1. Run `dotnet pack -o artifacts` to build the nuget package
2. Open the created .nupkg file (I do this by renaming to .zip, don't know if there's an easier way?)
3. Verify that the archive contains `contentFiles/any/any/ExampleFile.txt`
4. Edit `/ContentFilesExample/ContentFilesExample.csproj` to replace TargetFramework with TargetFrameworks (I have left this in as a commented line for ease)
5. Repeat steps 1-2
6. Verify that the archive does not contain `contentFiles`