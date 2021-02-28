# Cake.DotNetTool.Module

The Cake.DotNetTool.Module started out as an experiment to see how it would be possible to install .NET Tools using the Cake pre-processor directive.  This experiment turned out to be a success, and as a result, this module has now been integrated into the [main Cake repository](https://github.com/cake-build/cake/pull/3207).

Starting with Cake [v1.1.0](https://github.com/cake-build/cake/milestone/77?closed=1) this module will be released as part of the Cake release, as an official NuGet package under the same ID: [`Cake.DotNetTool.Module`](https://www.nuget.org/packages/Cake.DotNetTool.Module/).

Moving forward issues about this module will be tracked on the [main Cake repo](https://github.com/cake-build/cake/issues).

As such, it will no longer be necessary to include the following:

```
#module nuget:?package=Cake.DotNetTool.Module&version=0.4.0
```

In your cake scripts, as this will be done automatically.  If you do still have this in your cake script, Cake will ignore it, and emit a warning, indicating that you should remove it going forward.
