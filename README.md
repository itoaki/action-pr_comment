![build-test](https://github.com/itoaki/action-pr_comment/workflows/build-test/badge.svg)

# PR Comment Action

This action comments a message on PR.

## Inputs

### `repo-token`

**Required** The GitHub Token for comment on PR.

### `message`

**Required** The message to comment on PR.

## Outputs

### `commentUrl`

The PR comment URL.

## Example Usage

```yaml
jobs:
  prComment:
    if: github.event_name == 'pull_request'
    runs-on: ubuntu-latest
    steps:
      - name: PR Comment test
        uses: itoaki/action-pr_comment@v1.0.0
        with:
          repo-token: ${{ secrets.GITHUB_TOKEN }}
          message: Nice PR!👍
```
