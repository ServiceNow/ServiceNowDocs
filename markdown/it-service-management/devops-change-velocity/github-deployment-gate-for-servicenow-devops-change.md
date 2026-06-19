---
title: GitHub Deployment Gates for ServiceNow DevOps Change
description: Use the GitHub Deployment Gate capability to decide on whether a new deployment should proceed or halt.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/github-deployment-gate-for-servicenow-devops-change.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# GitHub Deployment Gates for ServiceNow DevOps Change

Use the GitHub Deployment Gate capability to decide on whether a new deployment should proceed or halt.

## Before you begin

GitHub deployment gates are supported only if you have connected your GitHub instance with Oauth 2.0 credentials for GitHub Apps using the JWT bearer token. For more information, see [OAuth 2.0 credentials for GitHub Apps - JWT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/dev-ops-github-apps-oath-jwt.md).

By default, the Deployment protection rules section is available for environments in all the repositories selected in the installed GitHub App.

Role required: Permission to create environments in GitHub

## Procedure

1.  Navigate to **Settings &gt; Environments** from a repository and click **New environment** to create an environment. \[Omitted image "github-app-deployment-gate-02.png"\] Alt text: Add new environment for GitHub App

2.  In the Deployment protection rules section, select the installed GitHub App name, and select **Save protection rules**. \[Omitted image "github-app-deployment-gate-01.png"\] Alt text: Configure deployment gate in GitHub App environment

3.  Add the ServiceNow DevOps Change Automation custom action at the step level \(for example, changeRequest job in workflow/yaml file\) in a pipeline job to create the change for deployment gates.

    The **deployment-gate** parameter must be added in the following JSON format.

    ```
    '{"environment":"deployment_gate","jobName":"Deploy"}'
    ```

    Here **environment** key value is the environment created with deployment protection rules, and **jobName** key value is the deployment job created in the workflow/yaml file with dependency on the change request job configured with the ServiceNow DevOps Change Automation custom action. \[Omitted image "deploymentgate-environmentkey.png"\] Alt text: Deployment gate parameter

    When the deployment gate specific workflow/yaml file is run in GitHub Actions, the details like change number, change url, and status will be displayed once the change request is created in ServiceNow. \[Omitted image "github-app-deployment-gate-03.png"\] Alt text: Change details for deployment gate

    The details like change comments, approved by, approved on, and status are logged in the GitHub tool after the workflow run is resumed from ServiceNow, i.e. when change request is approved and the change request state is updated to Implement in ServiceNow. \[Omitted image "github-app-deployment-gate-04.png"\] Alt text: Change logs for deployment gate


**Parent Topic:**[GitHub integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/github-integration-dev-ops.md)

