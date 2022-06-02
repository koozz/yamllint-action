# yamllint-action

> **Deprecated: This action is no longer needed**
> 
> usage of `ubuntu-latest` with a step that defines `run: yamllint --config-file .yamllint --format github .` will suffice.


To prevent each build from building a yamllint container over-and-over-again,
this action will use a hosted prebuilt container.

## Usage

```yaml
---
name: yamllint

on:
  pull_request:
    branches:
      - main

jobs:
  yamllint:
    runs-on: ubuntu-latest
    steps:
      - name: Code checkout
        uses: actions/checkout@v2
      - name: Lint YAML
        uses: koozz/yamllint-action@latest
```

If your satisfied, follow best practices and pin the action to a specific
version.

## License

MIT
