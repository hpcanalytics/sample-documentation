# sample-documentation

Documentation is built using [Docusaurus](https://docusaurus.io). Please refer its documentation on how to build.

# How to deploy

Do the changes to the documents

```bash
cd website
yarn run build
GIT_USER=<GIT_USER> CURRENT_BRANCH=master USE_SSH=false yarn run publish-gh-pages
```