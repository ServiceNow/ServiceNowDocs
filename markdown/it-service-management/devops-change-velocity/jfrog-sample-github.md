---
title: Sample pipeline to upload and download artifacts for GitHub
description: Pipeline samples for GitHub containing steps to upload and download artifacts for GitHub.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Sample pipeline to upload and download artifacts for GitHub

Pipeline samples for GitHub containing steps to upload and download artifacts for GitHub.

## Upload artifacts from GitHub to JFrog

```

name: JFrogUploadArtifact

on:
  push:
    branches:
      - main
jobs:
  upload_to_jfrog:
    runs-on: ubuntu-latest

    defaults:
      run:
        working-directory: "${{ github.workspace }}"

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up JFrog CLI
        uses: jfrog/setup-jfrog-cli@v3
        with:
          version: latest
        env:
          JF_URL: ${{ secrets.JFROG_URL }}
          JF_USER: ${{ secrets.JFROG_USER }}
          JF_PASSWORD: ${{ secrets.JFROG_PASSWORD }}
    
      - name: Upload Artifact to Jfrog
        run: |
          export JFROG_CLI_HOME="${{ github.workspace }}"
          #upload artifacts
          jf rt u "servicenow-app-devops.zip" "local_repo"
          # Publish build info
          jf rt bp
```

## Download artifacts from JFrog to GitHub

```

name: JFrogDownloadArtifact

on:
  push:
    branches:
      - main

jobs:
  download_from_jfrog:
    runs-on: ubuntu-latest

    defaults:
      run:
        working-directory: "${{ github.workspace }}"

    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Set up JFrog CLI
        uses: jfrog/setup-jfrog-cli@v3
        with:
          version: latest
        env:
          JF_URL: ${{ secrets.JFROG_URL }}
          JF_USER: ${{ secrets.JFROG_USER }}
          JF_PASSWORD: ${{ secrets.JFROG_PASSWORD }}
          
      - name: download artifacts from jfrog
        run: |
          export JFROG_CLI_HOME="${{ github.workspace }}"
          # download artifact from jfrog
          jf rt dl "local_repo/servicenow-app-devops.zip" ./
          # Publish build info
          jf rt bp
```

**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

