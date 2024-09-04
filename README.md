# convcom-action
Action to create a changelog, next version and version bump type based on semantic versioning and conventional commits

Very opinionated. Expects a semantic version of the form `v__MAJOR__.__MINOR__.__PATCH__`, source and target SHA. The action will then calculate, based on the commit messages betwen source and target SHA, what kind of change the next update is and then return the bumped version.

The commits are expected to be conventional commits. The type of bump is decided by the following logic:

- `__noun__!:` - major
- `feat:` - minor
- everything else - patch
