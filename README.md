# sample-documentation

# How to deploy

Do the changes to the documents

```bash
cd website
yarn run build
GIT_USER=<GIT_USER> CURRENT_BRANCH=master USE_SSH=false yarn run publish-gh-pages
```