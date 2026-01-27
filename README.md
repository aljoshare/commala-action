![Logo for commala](assets/logo.png)

# commala - A commit linter with a lot of rice

![GitHub Release](https://img.shields.io/github/v/release/aljoshare/commala-action?style=flat&logo=github&label=release&color=eca13d)
![GitHub Release Date](https://img.shields.io/github/release-date/aljoshare/commala-action?display_date=published_at&style=flat&logo=github&label=release%20date&color=eca13d)

![Static Badge](https://img.shields.io/badge/language-grey?logo=yaml)
![Static Badge](https://img.shields.io/badge/github-action-eca13d?logo=github)

> “Dad-a-chum? Dum-a-chum? Ded-a-chek? Did-a-chick?”  
> — Lobstrosities

commala is a commit linting tool that ensures that certain standards are met before you merge to keep your git history clean and consistent. Commala is part of your Ka-tet, when you walk through the Wastelands of software development.

## Requirements

This action requires a `.commala.yml` configuration file to be present in the root of your repository. The action will look for this file at `/github/workspace/.commala.yml` inside the Docker container.

For configuration options and examples, see the [commala documentation](https://github.com/aljoshare/commala).

## Usage

```yaml
- uses: actions/checkout@v5
  with:
    fetch-depth: 0 # Required to fetch commit history
- uses: aljoshare/commala-action@v0.7.0
  with:
    number-of-commits: 5 # Check last 5 commits
```

<!-- action-docs-inputs source="action.yml" -->

## Inputs

| name                | description                                 | required | default |
| ------------------- | ------------------------------------------- | -------- | ------- |
| `number-of-commits` | <p>Limit the number of commits to check</p> | `false`  | `""`    |

<!-- action-docs-inputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-outputs source="action.yml" -->

<!-- action-docs-runs source="action.yml" -->

## Runs

This action is a `docker` action.

<!-- action-docs-runs source="action.yml" -->
