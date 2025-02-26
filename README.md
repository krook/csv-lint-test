# CSV lint Docker action test

This tests the [`krook/csv-lint`](https://github.com/krook/csv-lint) action.

## Inputs

## `CSV_FILE`

**Required** The path of the file to validate.

## Example usage

```yaml
on: 
  pull_request:
    paths:
      - 'file.csv'

jobs:
  verify-cvs-validation:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Validate CSV
        uses: krook/csv-lint@main
        env:
          CSV_FILE: "file.csv"
```
