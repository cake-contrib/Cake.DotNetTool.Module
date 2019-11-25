The folllowing URI parameters are supported by the Cake.DotNetTool.Module.

# Source

This is not a named parameter, but it is permitted as per the URI definition.  By default, the dotnet CLI will attempt to install applications from NuGet.org.  If your package is actually hosted on another feed, for example, on a MyGet feed, the installation source can be overridden.

## Example

```
#tool dotnet:https://www.myget.org/F/gep13/api/v2?package=Octopus.DotNet.Cli
```

# Package

This is the name of the Global Tool that you would like to install.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli
```

# Version

The specific version of the Global Tool that is being installed.  If not provided, the dotnet CLI will install the latest package version that is available.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli&version=4.41.0
```

# Global

By default, a tool will be installed to the configured Cake Tools folder.  If you want to install the tool globally on your machine, you can pass the global parameter.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli&version=4.41.0&global
```

# Config File

If you need to specify a NuGet config file, for example you need to authenticate to a particular feed, you can specify the location of this file using the configfile parameter.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli&version=4.41.0&configfile="../../NuGet.config"
```

# Ignore failed sources

There might be cases where you want to ignore failed NuGet sources as long as the package could be restored.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli&version=4.41.0&ignore-failed-sources"
```

# Framework

Specifies the [target framework](https://docs.microsoft.com/en-us/dotnet/standard/frameworks) to install the tool for. By default, the .NET Core SDK tries to choose the most appropriate target framework.

## Example

```
#tool dotnet:?package=Octopus.DotNet.Cli&version=4.41.0&framework="net472"
```

# Verbosity

While not a named parameter, you can control the logging verbosity of the underlying dotnet tool command by altering the overall verbosity of the Cake Script execution. i.e. running:

```
./build.sh --verbosity=diagnostic
```
