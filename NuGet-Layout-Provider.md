Our support for NuGet is handled via the Nuget Layout provider.

We currently only support NuGet protocol version 2.0.

# Notes

## Custom Features

This layout provider has feeds.

## NuGet 2 Search Provider

The NuGet layout provider supports uses the [OrientDB (default)](https://github.com/strongbox/strongbox/wiki/Searching#orientdbsearchprovider).

# Information For Developers

The code for the NuGet layout provider is located under the [strongbox-storage-nuget-layout-provider](https://github.com/strongbox/strongbox/tree/master/strongbox-storage/strongbox-storage-layout-providers/strongbox-storage-nuget-layout-provider) module.

## Classes of Interest

The following are some of the most important classes you will need to be familiar with in order to work on this layout provider:

* [NugetArtifactCoordinates](https://github.com/strongbox/strongbox/blob/master/strongbox-storage/strongbox-storage-layout-providers/strongbox-storage-nuget-layout-provider/src/main/java/org/carlspring/strongbox/artifact/coordinates/NugetArtifactCoordinates.java) : This is an implementation of `ArtifactCoordinates` for NuGet.
* [NugetLayoutProvider](https://github.com/strongbox/strongbox/blob/master/strongbox-storage/strongbox-storage-layout-providers/strongbox-storage-nuget-layout-provider/src/main/java/org/carlspring/strongbox/providers/layout/NugetLayoutProvider.java) : This is the actual implementation of the NuGet layout provider.
* [NugetRepositoryFeatures](https://github.com/strongbox/strongbox/blob/master/strongbox-storage/strongbox-storage-layout-providers/strongbox-storage-nuget-layout-provider/src/main/java/org/carlspring/strongbox/repository/NugetRepositoryFeatures.java) : This defines the custom layout provider features for NuGet (like, for example, feeds).
* [NugetRepositoryManagementStrategy](https://github.com/strongbox/strongbox/blob/master/strongbox-storage/strongbox-storage-layout-providers/strongbox-storage-nuget-layout-provider/src/main/java/org/carlspring/strongbox/repository/NugetRepositoryManagementStrategy.java) : This class is used to handle the initialization of NuGet repositories.
* [NugetArtifactController](https://github.com/strongbox/strongbox/blob/master/strongbox-web-core/src/main/java/org/carlspring/strongbox/controllers/nuget/NugetArtifactController.java) : This is the NuGet-specific implementation of the `BaseArtifactController`.

# See Also
* [[How To Implement Your Own Repository Format]]