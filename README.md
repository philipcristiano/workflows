# workflows
Github Workflows for common patterns

## rebar3.yml

Example usage:


```
name: Pull Request

on:

  pull_request:
    branches:
      - main

jobs:

  erlang:
    uses: "philipcristiano/workflows/.github/workflows/rebar3.yml@main"
    secrets:
      CODECOV_TOKEN: ${{ secrets.CODECOV_TOKEN }}
```

## docker-build.yml

Example usage:


```
name: Pull Request

on:

  pull_request:
    branches:
      - main

jobs:

  docker-build:
    uses: "philipcristiano/workflows/.github/workflows/docker-build.yml@main"
```
