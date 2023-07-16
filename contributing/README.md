# Contributing

## Work flow

All the repos in the **HiDRo** organization are governed by the following guidelines.

1. All the repos have only 2 branches: `master` and `devel`.
2. The HEAD of `master` is at the last stable release.
3. The HEAD of `devel` is at the last tested feature.
4. No one can commit directly neither to `master` nor `devel`.
5. The only way to contribute is via pull requests to `devel`.
6. Pull requests (PRs) must be approved by one allowed organization member.

## Guidelines

If you want to contribute, please follow these steps:

1. Fork the repository you want to contribute to. Commits to `devel` and `master` are only done via PR. Besides, no other branches are allowed in the repositories.
2. Pull the latest `hidro-iri:devel` changes to your fork.
3. Create a new branch with the name of the new feature.
4. Develop the new feature into this branch.
5. Format the code using the files in [this repository](https://github.com/hidro-iri/linters).
6. Submit the PR of the feature forked branch into the original repository.
7. This PR will be reviewed by an organization member and probably some changes will be suggested.
8. After the changes have been incorporated, the feature will be merged to merged to `devel`.

[Back to Home](../profile/README.md)
