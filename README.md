# Git Push Action

A Github Action to push code to git, like [`gitpage`](https://pages.github.com/).

## Environment Variables

- GITHUB_EMAIL: git user email
- GITHUB_USERNAME: git user username
- PUBLISH_REPO: repo url, `https://${{ secrets.GitHub_PAT }}@github.com/owner/repo.git`
- PUBLISH_BRANCH: git branch
- PUBLISH_DIR: dir to publish

## Secrets

- DEPLOY_PRIVATE_KEY: Required your deploy key which has Write access[not use]

## How to Use

```
    - name: Push to Github
      uses: cnxyz/git-push@v1.0.0
      env:
        GITHUB_EMAIL: "admin@china.cn"
        GITHUB_USERNAME: "admin"
        PUBLISH_REPO: https://${{ secrets.GitHub_PAT }}@github.com/owner/repo.git
        PUBLISH_BRANCH: main
        PUBLISH_DIR: ./public
        # DEPLOY_PRIVATE_KEY: ${{ secrets.DEPLOY_PRIVATE_KEY }}
```
