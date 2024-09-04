---
title: "Running Dagger in a GitHub Actions workflow"
---

## Embedding is easy

Embedding Dagger in a GitHub Actions workflow is straightforward as the Dagger team provides a GitHub Action that you can use to run Dagger pipelines.

Alternatively, the proces is the same as what we just did, if you do not want to use the provided GitHub Action.

</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

## GitHub Action Workflow

Create a new file in the `.github/workflows` directory called `dagger.yml` and add the following content:

</br>

```yaml
name: Run Dagger pipeline

on:
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  dagger:
    name: Run Dagger pipeline
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Go
        uses: actions/setup-go@v5
        with:
          go-version: 1.23.0
          cache: false

      - name: Run Dagger pipeline
        uses: dagger/dagger-for-github@v5
        with:
          verb: run
          args: go run pipeline.go
          version: "0.12.5"
```

</br>

This workflow runs on every push to the `main` branch and when manually triggered.

It uses the `dagger/dagger-for-github` action to run the pipeline.

Push the changes to your repository and navigate to the Actions tab in GitHub to see the workflow running.

</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

![Finish smile](https://media1.tenor.com/m/rPOqhxQBOz0AAAAC/all-might-my-hero-academia.gif)

</br>
</br>
