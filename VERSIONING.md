﻿Versioning scheme for .NET Compiler Platform ("Roslyn") Analyzers
=================================================================

Current version of all analyzer packages that are built out of this repo are tracked in [Analyzers.Versions.targets](.//build//Targets//Analyzers.Versions.targets)

Following is the versioning scheme that is being used for analyzer packages:

1. The major and minor version numbers of the packages track the major and minor version numbers of Microsoft.CodeAnalysis package that the analyzer is dependent upon. For example, version 1.0.0, 1.0.1, ..., 1.0.X of the analyzer packages depend upon version 1.0.0 of Microsoft.CodeAnalysis package.

2. When we move the repo to a newer version of Microsoft.CodeAnalysis, say 1.X.0, then the version number of all the analyzer packages will be bumped to be >= 1.X.0.

**NOTE**: An exception was applied to the above versioning scheme when we moved the analyzer packages to version 1.1.0, while still depending on version 1.0.0 of Microsoft.CodeAnalysis. This was done as we had mistakenly published 1.1.0-beta1 pre-release packages for some analyzer packages on nuget.org.