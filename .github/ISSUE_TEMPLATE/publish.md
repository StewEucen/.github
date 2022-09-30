---
name: '🚀 Publish'
about: Publish Issue
title: '🚀 Publish `vvvvvv`'
labels: ''
assignees: ''

---
## Overview

* Publish version as `vvvvvv`.

## Tasks

- [ ] ⚙️ Update package version to `vvvvvv`
- [ ] Publish.
- [ ] Merge to `main` as `vvvvvv`.

## npm login before publishing

* npm login to GitHub Packages

    - [ ] get login password from your GitHub settings
Go to → https://github.com/settings/tokens
    - [ ] copy your `personal access token` created
    - [ ] run in terminal
        ```
        % npm login --registry=https://npm.pkg.github.com/

        Username: your-github-account-in-lower-case-only
        Password:
        Email: your.mail.account@gmail.com
        Logged in as [your-name] on https://npm.pkg.github.com/.
        ```

## Procedure to Publish

1. Check Commit Hash to Publish

    - [ ] git log --graph --oneline --decorate --all
    - [ ] target commit as: `xxxxxxxx`

2. Confirm Work to Publish

    - [ ] package.json
    - [ ] package-lock.json

3. Publish

    - [ ] `npm publish --dry-run`

        ```
        % npm publish --dry-run
        npm notice
        npm notice 📦  your-package-name
        ```

    - [ ] Check log of `--dry-run` by other member before actual publishing.
    - [ ] `npm publish`
