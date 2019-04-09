Due to the fact that Cake Modules are extending and altering the internals of the Cake, the Module Assembly needs to be loaded prior to the main Cake execution. As documented in the Module section of this page, you simply have to do the following:

```
./build.sh --bootstrap
./build.sh
```

This means that the first execution of Cake will inspect your Cake script for any module inclusions in your script, and if there are any, download and install them. And the second execution will then be able to use those modules, and complete the usage of the module.

An example of a Cake script which both includes the module definition for the DotNet Tool Module, and which also uses it, is shown below:

```
#module nuget:?package=Cake.DotNetTool.Module&version=0.1.0
#tool "dotnet:?package=Octopus.DotNet.Cli&version=4.41.0"
```
