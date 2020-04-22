# Sider organization-wide files and settings

See the [document](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) about the `.github` repository.

## Syncing labels

Use [github-label-sync](https://github.com/Financial-Times/github-label-sync) and follow the steps:

1. Get a new access token and set it: `export GITHUB_ACCESS_TOKEN=xxxxxx`
2. Try to sync with dry-run mode: `npx github-label-sync sider/<repo_name> --allow-added-labels --dry-run`
3. Sync actually: `npx github-label-sync sider/<repo_name> --allow-added-labels`

Note that we should **always set `--allow-added-labels`** because existing labels would be deleted without it.
