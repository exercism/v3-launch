# File migration

1. Move the existing exercises in the `exercises` directory to the `exercises/practice` directory
1. Copy the v3 `languages/<slug>/concepts` directory to the `concepts` directory
1. Copy the v3 `languages/<slug>/exercises/concept` directory to the `exercises/concept` directory
1. Copy the v3 `languages/<slug>/reference` directory to the `reference` directory
1. Copy the v3 `languages/<slug>/docs` directory to the `docs` directory
1. Update the `fetch-configlet` and `fetch-configlet.ps1` files to the latest version
1. Convert relative links that point to v3 documents outside the track's directory to absolute links.

## Notes

1. The `_sidebar.md` files are not copied.
1. The `README.md` file is not copied.
1. The `maintainers.md` file is not copied.

The [git-filter-repo](https://github.com/newren/git-filter-repo) tool is used to retain the commit history.
