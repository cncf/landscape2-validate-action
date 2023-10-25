# Landscape2 validate action

This GitHub action checks if the provided landscape datasource file is valid.

## Usage

### Validate data file

```yaml
name: Validate

on:
  push:
    branches:
      - main

jobs:
  validate-landscape-data:
    runs-on: ubuntu-latest
    name: "Validate landscape data file"
    steps:
      - uses: actions/checkout@v3
      - uses: cncf/landscape2-validate-action@v2
        with:
          target_kind: data
          target_path: ./landscape.yml
```

### Validate settings file

```yaml
name: Validate

on:
  push:
    branches:
      - main

jobs:

  validate-landscape-settings:
    runs-on: ubuntu-latest
    name: "Validate landscape settings file"
    steps:
      - uses: actions/checkout@v3
      - uses: cncf/landscape2-validate-action@v2
        with:
          target_kind: settings
          target_path: ./settings.yml
```

### Validate guide file

```yaml
name: Validate

on:
  push:
    branches:
      - main

jobs:
  validate-landscape-guide:
    runs-on: ubuntu-latest
    name: "Validate landscape guide file"
    steps:
      - uses: actions/checkout@v3
      - uses: cncf/landscape2-validate-action@v2
        with:
          target_kind: guide
          target_path: ./guide.yml
```

## Contributing

Please see [CONTRIBUTING.md](./CONTRIBUTING.md) for more details.

## Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/master/code-of-conduct.md).

## License

Landscape2 is an Open Source project licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).
