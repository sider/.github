# Sider organization-wide files and settings

See the [document](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) about the `.github` repository.

## Syncing labels

You can add or edit labels in [`labels.json`](labels.json) (in alphabetical order).

Use [github-label-sync](https://github.com/Financial-Times/github-label-sync) and follow the steps:

1. [Get a new access token](https://github.com/settings/tokens/new?description=Sider+labels+sync&scopes=repo) in GitHub
2. Set the new token on your terminal, e.g. `export GITHUB_ACCESS_TOKEN=xxxxxx`
3. Try to sync with dry-run mode: `npx github-label-sync sider/.github --allow-added-labels --dry-run`
4. Sync actually: `npx github-label-sync sider/.github --allow-added-labels`
5. Check the synced labels on the [labels](https://github.com/sider/.github/labels) page
6. Try to sync for other repositories: `npx github-label-sync sider/<repo> --allow-added-labels [--dry-run]`
7. Unset the token on your terminal, e.g. `unset GITHUB_ACCESS_TOKEN`
8. [Delete the generated token](https://github.com/settings/tokens) on GitHub

Note that we should **always set `--allow-added-labels`** because existing labels would be deleted without it.
