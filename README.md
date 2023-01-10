# docker-build

A GitHub Action for building docker images.

## Usage

To use the GitHub Action, add the following to your job:

```yaml
- uses: conventional-actions/docker-build@v1
```

### Inputs

| Name               | Default                                     | Description                                               |
|--------------------|---------------------------------------------|-----------------------------------------------------------|
| name               |                                             | name of container                                         |
| artifact           |                                             | name of the artifact if different from the container name |
| platforms          | `linux/amd64,linux/arm64`                   | comma-separated list of platforms to build                |
| buildkitd-flags    | `--allow-insecure-entitlement network.host` | buildkitd flags to use                                    |
| build-args         |                                             | list of build-time variables                              |
| target             |                                             | sets the target stage to build                            |
| snyk-token         |                                             | SNYK auth token                                           |
| scan               | `true`                                      | set to false to disable scan (default is true)            |
| download-artifacts | `true`                                      | set to false to disable downloading artifacts             |
| version-major      |                                             | major version number                                      |
| version-minor      |                                             | minor version number                                      |
| version-patch      |                                             | full path version number                                  |

### Outputs

| Name          | Type     | Description      |
|---------------|----------|------------------|

### Example

```yaml
on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: conventional-actions/docker-build@v1
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).
