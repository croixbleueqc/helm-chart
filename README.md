# Public helm repositories

Purpose is to distribute public projets charts

```bash
helm repo index . --url https://croixbleueqc.github.io/helm-charts/
```

Tip, to generate the index.yaml before merging your chart in, you can push a
branch with the new release, and then use the URL of your branch to generate the
index.yaml. Eg:

```bash
helm repo index . --url https://github.com/croixbleueqc/helm-charts/tree/feature/add-axop-1.0.4
```

Then adjust index.yaml so that the URLs do not contain the repo URL & branch
name, add index.yaml to your branch in a new commit and update your branch which
now contains the chart + the updated index.yaml.

# Package new charts (ex: ots)
helm package ots
