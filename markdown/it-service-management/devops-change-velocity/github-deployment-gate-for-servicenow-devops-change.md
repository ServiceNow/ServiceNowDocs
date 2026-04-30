---
title: GitHub Deployment Gates for ServiceNow DevOps Change
description: Use the GitHub Deployment Gate capability to decide on whether a new deployment should proceed or halt.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# GitHub Deployment Gates for ServiceNow DevOps Change

Use the GitHub Deployment Gate capability to decide on whether a new deployment should proceed or halt.

## Before you begin

GitHub deployment gates are supported only if you have connected your GitHub instance with Oauth 2.0 credentials for GitHub Apps using the JWT bearer token. For more information, see [OAuth 2.0 credentials for GitHub Apps - JWT](dev-ops-github-apps-oath-jwt.md#).

By default, the Deployment protection rules section is available for environments in all the repositories selected in the installed GitHub App.

Role required: Permission to create environments in GitHub

## Procedure

1.  Navigate to **Settings &gt; Environments** from a repository and click **New environment** to create an environment. ![Add new environment for GitHub App](../image/github-app-deployment-gate-02.png)

2.  In the Deployment protection rules section, select the installed GitHub App name, and select **Save protection rules**. ![Configure deployment gate in GitHub App environment](../image/github-app-deployment-gate-01.png)

3.  Add the ServiceNow DevOps Change Automation custom action at the step level \(for example, changeRequest job in workflow/yaml file\) in a pipeline job to create the change for deployment gates.

    The **deployment-gate** parameter must be added in the following JSON format.

    ```
    '{"environment":"deployment_gate","jobName":"Deploy"}'
    ```

    Here **environment** key value is the environment created with deployment protection rules, and **jobName** key value is the deployment job created in the workflow/yaml file with dependency on the change request job configured with the ServiceNow DevOps Change Automation custom action. ![Deployment gate parameter](../image/deploymentgate-environmentkey.png)

    When the deployment gate specific workflow/yaml file is run in GitHub Actions, the details like change number, change url, and status will be displayed once the change request is created in ServiceNow. ![Change details for deployment gate](../image/github-app-deployment-gate-03.png)

    The details like change comments, approved by, approved on, and status are logged in the GitHub tool after the workflow run is resumed from ServiceNow, i.e. when change request is approved and the change request state is updated to Implement in ServiceNow. ![Change logs for deployment gate](../image/github-app-deployment-gate-04.png)


**Parent Topic:**[GitHub integration with DevOps Change Velocity](github-integration-dev-ops.md)

