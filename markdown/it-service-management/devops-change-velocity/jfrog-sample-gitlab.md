---
title: Sample pipeline to upload and download artifacts for GitLab
description: Pipeline samples for GitLab containing steps to upload and download artifacts for GitHub.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Sample pipeline to upload and download artifacts for GitLab

Pipeline samples for GitLab containing steps to upload and download artifacts for GitHub.

To upload and download artifacts from GitLab to JFrog, the parameters **JFROG\_URL**, **JFROG\_USER**, and **JFROG\_PASSWORD** must be set as CI/CD variables in your GitLab instance.

1.  Navigate to your project, then go to **Settings** &gt; **CI/CD** &gt; **Variables**.
2.  Select **Add variable**.
3.  Enter the parameter in the **Key** field and enter the value for the parameter in the **Value** field.
4.  Select **Add variable** to save.

Create a CI/CD variable for the following 3 parameters:

-   **JFROG\_URL**
-   **JFROG\_USER**
-   **JFROG\_PASSWORD**

![Set the parameters.](../image/jfrog-sample-gitlab-01.png)

## Sample pipeline to upload artifacts from GitLab to JFrog

```

stages:
  - upload

variables:
  JFROG_CLI_HOME: ${CI_PROJECT_DIR}
  JFROG_ARTIFACTORY_URL: ${JFROG_URL}
  JFROG_ARTIFACTORY_REPO: "local_repo/gitlab"
  JFROG_ARTIFACTORY_USERNAME: ${JFROG_USER}
  JFROG_ARTIFACTORY_PASSWORD: ${JFROG_PASSWORD}
  ARTIFACT_PATH: "/"
  ARTIFACT_NAME: "servicenow-app-devops.zip"
  BUILD_NAME: "${CI_PROJECT_NAME}"
  BUILD_NUMBER: "${CI_PIPELINE_ID}"
  JFROG_CLI_BUILD_URL: ${CI_SERVER_URL}/$CI_PROJECT_PATH/-/pipelines/$CI_PIPELINE_ID

upload:
  stage: upload
  script:
    - export BUILD_URL=${CI_SERVER_URL}/$CI_PROJECT_PATH/pipelines/$CI_PIPELINE_ID
    # upload artifact
    - jfrog rt u "servicenow-app-devops.zip"  "${JFROG_ARTIFACTORY_REPO}" --build-name=$CI_PROJECT_NAME --build-number=$CI_PIPELINE_ID
    # publish build-info
    - jfrog rt bp "${CI_PROJECT_NAME}" "${CI_PIPELINE_ID}"
  before_script:
  - mkdir -p ${JFROG_CLI_HOME}
  - export PATH=$PATH:${JFROG_CLI_HOME}
  - curl -fL https://getcli.jfrog.io | sh
  - jfrog config add artifactory-server --artifactory-url=${JFROG_ARTIFACTORY_URL} --user=${JFROG_ARTIFACTORY_USERNAME} --password=${JFROG_ARTIFACTORY_PASSWORD}
```

## Sample pipeline to download artifacts from JFrog to GitLab

```

stages:
  - download

variables:
  JFROG_CLI_HOME: ${CI_PROJECT_DIR}
  JFROG_ARTIFACTORY_URL: ${JFROG_URL}
  JFROG_ARTIFACTORY_REPO: "local_repo/gitlab"
  JFROG_ARTIFACTORY_USERNAME: ${JFROG_USER}
  JFROG_ARTIFACTORY_PASSWORD: ${JFROG_PASSWORD}
  ARTIFACT_PATH: "/"
  ARTIFACT_NAME: "servicenow-app-devops.zip"
  BUILD_NAME: "${CI_PROJECT_NAME}"
  BUILD_NUMBER: "${CI_PIPELINE_ID}"
  JFROG_CLI_BUILD_URL: ${CI_SERVER_URL}/$CI_PROJECT_PATH/-/pipelines/$CI_PIPELINE_ID

download:
  stage: download
  script:
    # download artifact 
     - jfrog rt dl ${JFROG_ARTIFACTORY_REPO}/servicenow-app-devops.zip --include-dirs --build-name=$CI_PROJECT_NAME --build-number=$CI_PIPELINE_ID
    # publish build-info 
     - jfrog rt bp ${CI_PROJECT_NAME} ${CI_PIPELINE_ID}
  before_script:
  - mkdir -p ${JFROG_CLI_HOME}
  - export PATH=$PATH:${JFROG_CLI_HOME}
  - curl -fL https://getcli.jfrog.io | sh
  - jfrog config add artifactory-server --artifactory-url=${JFROG_ARTIFACTORY_URL} --user=${JFROG_ARTIFACTORY_USERNAME} --password=${JFROG_ARTIFACTORY_PASSWORD}
```

**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

