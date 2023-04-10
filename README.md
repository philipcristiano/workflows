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

## docker-build(-push).yml

Docker building and build/push actions.

Push requires secrets for:

* `DOCKER_USERNAME`
* `DOCKER_PASSWORD`

These can optionally include multi-platform options

* `qemu_platforms`
* `docker_platforms`

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
