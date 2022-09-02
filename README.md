# docker-build

A GitHub Action for building docker images.

## Usage

To use the GitHub Action, add the following to your job:

```yaml
- uses: conventional-actions/docker-build@v1
```

### Inputs

| Name          | Default        | Description                             |
|---------------|----------------|-----------------------------------------|

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

