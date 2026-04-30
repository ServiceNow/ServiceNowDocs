---
title: GitLab pipelines with parallel jobs
description: GitLab Docker Image supports change creation in GitLab pipelines containing parallel jobs.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Change acceleration in GitLab, GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# GitLab pipelines with parallel jobs

GitLab Docker Image supports change creation in GitLab pipelines containing parallel jobs.

**Note:** If your GitLab pipeline has parallel jobs, it is better to use the GitLab Docker Image, rather than **when:manual**. For detailed information about GitLab Docker Image, see [Implement custom actions for pipelines using generic Docker container image](servicenow-custom-actions-for-gitlab.md).

Sample yaml pipeline demonstrating parallel jobs:

```

image: servicenowdocker/sndevops:3.1.0  # Update docker version per your current version.
stages:
  - pre-build
  - build
  - test
  - pre-prod
  - prod


Scan PreProd:
  stage: pre-build
  script:
    - echo $CI_JOB_NAME

Check policies in PreProd:
  stage: build
  needs: 
    - job: "Scan PreProd"
  script:
    - exit 1  # Simulating a failed test job
  allow_failure: true  # Allow this job to fail without stopping the pipeline

Check policies in Prod:
  stage: build
  needs: 
    - job: "Scan PreProd"
  script:
    - echo $CI_JOB_NAME

Deploy App in Test:
  stage: test
  needs: 
    - job: "Scan PreProd"
  script: 
    - echo $CI_JOB_NAME

Deploy App in PreProd:
  stage: pre-prod
  needs:
    - job: "Deploy App in Test"
    - job: "Check policies in PreProd"
  allow_failure: false
  script:
    - echo $CI_JOB_NAME
    - sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":100},\"autoCloseChange\":true}"



Deploy App in Prod:
  stage: prod
  needs:
    - job: "Deploy App in PreProd"
    - job: "Check policies in Prod"
  allow_failure: false
  script:
    - echo $CI_JOB_NAME
    - sndevopscli create change -p "{\"changeStepDetails\":{\"timeout\":3600,\"interval\":100},\"autoCloseChange\":true}"
```

**Parent Topic:**[GitLab integration with DevOps Change Velocity](gitlab-integration-dev-ops.md)

