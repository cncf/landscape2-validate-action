# Landscape2 validate action

This GitHub action checks if the provided landscape data file (`landscape.yml`) is valid.

## Usage

```yaml
name: Validate

on:
  push:
    branches:
      - main

jobs:
  validate-landscape:
    runs-on: ubuntu-latest
    name: "Validate landscape.yml file"
    steps:
      - uses: actions/checkout@v3
      - uses: cncf/landscape2-validate-action@v1
        with:
          data_file: ./landscape.yml
```

## Contributing

Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.

## Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/master/code-of-conduct.md).

## License

Landscape2 is an Open Source project licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
