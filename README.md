# Sider organization-wide files and settings

See the [document](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) about the `.github` repository.

## Syncing labels

Use [github-label-sync](https://github.com/Financial-Times/github-label-sync):

```console
$ npx github-label-sync --access-token xxxx sider/<repo_name> [--dry-run] [--allow-added-labels]
```
