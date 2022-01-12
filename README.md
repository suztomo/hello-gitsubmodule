Testing Git submodules to track a set of Google Cloud libraries
that were released as part of an SDK release.

# Submodules tracking release tags 

Each directory is a submodule ([git-submodule](https://git-scm.com/docs/git-submodule))
that corresponds to the release tag of the SDK release.

For example for January 2022 SDK release the references of the submodules are
the following:

| Repository  | Tag (commit) |
| ------------- | ------------- |
| google-auth-library-java  | v1.2.1 (4ae533b) |
| java-core  | v2.2.0 (834d228) |
| java-shared-dependencies  | v2.4.0 (ffc3cf1) |
| java-iam-admin  | v1.0.0 (48424a4) |
| java-iamcredentials  | v2.0.6 (12e1ff5) |
| java-bigquery  | v2.3.3 (f88665b) |

(I omit many other repositories for the sake of simplicity.)

A tag in this repository track these repository release tags. For example:
`2022-01-sdk` (https://github.com/suztomo/hello-gitsubmodule/releases/tag/2022-01-sdk)
represents the January 2022 SDK release, and `2022-06-sdk`, when it's created,
will have different set of release tags of the libraries.

# CI

Creating a pull request runs CI to run the tests in the submodules.

An example to validate an incompatible change in java-core:
https://github.com/suztomo/hello-gitsubmodule/pull/2