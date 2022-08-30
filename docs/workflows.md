# Safe Settings Workflows

This workflow has been developed for use with the safe settings project.  However, it is general enough that it can be used with most node projects.

The following github workflows are available for this project:

|Workflow|Variables|Dependencies|Description|
|---|---|---|---|
|rp-safe-settings|- REGISTRY<br/>- REPOSITORY<br/>-GHCR_TOKEN<br/>- GH_TOKEN|- Semantic Release<br/>- Conventionl Commits|Generates a new safe settings release & publishes a corresponding image|


## rp-safe-settings

This will evaluate the triggeri

### Variables

#### REGISTRY
REGISTRY is the docker image registry to use for hosting the published images. It is defaulted to ghcr.io.

#### REPOSITORY
REPOSITORY is the location for the code that is to be avaluated by the workflow.  By default, it is configured to use the repo the workflow has been triggered from

#### GH_TOKEN
GH_TOKEN is the token to be used for interacting with the project.  This token needs to have the following permissions:

- Repository
    - Read
    - Write
- Workflow
    - Read
    - Write
- Package
    - Read
    - Write

#### GHCR_TOKEN
This is the token to be used for interacting with the image repository.  If GitHub is being used, then the GH_TOKEN can be used here as well.
