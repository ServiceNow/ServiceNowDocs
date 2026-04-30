---
title: GitHub Actions configurations
description: Configuration information on GitHub Actions, such as, secrets, workflows, and limitations.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# GitHub Actions configurations

Configuration information on GitHub Actions, such as, secrets, workflows, and limitations.

## Secrets in GitHub Actions

Create secrets \(credentials\) in GitHub repository or GitHub organization. Secrets are environment variables \(encrypted\) that you create in an organization or repository. These secrets are available to use in GitHub Actions workflows. For more information, see [Encrypted secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets).

|Secret|Description|
|------|-----------|
|SN\_INSTANCE\_URL|ServiceNow instance URL. For example, https://&lt;instance\_name&gt;.service-now.com.|
|SN\_ORCHESTRATION\_TOOL\_ID|Sys\_id for the GitHub tool created in ServiceNow instance.|
|SN\_DEVOPS\_INTEGRATION\_TOKEN|Secret token for the GitHub tool created in DevOps \(`devops-integration-token` parameter\). To access your secret token navigate to your GitHub tool record in ServiceNow \(**All &gt; Tools &gt; Orchestration Tools**\), and select **Copy token** in the Classic UI.|

## Workflows in the GitHub repository

Create a YAML file to define workflow configuration in your GitHub repository.

The following points must be considered while defining the workflow:

-   All workflows of your repository must have either a .yml or .yaml file extension. All workflows must be under `.github/workflows` directory and follow the syntax defined in the [Workflow syntax for GitHub Actions](https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions).

    ![Workflows in the GitHub Actions tab](../image/integration-with-github-actions-2.jpg)

-   The name of the workflow must match with the workflow file name.

    ![Name of the worflow must match with the file name](../image/integration-with-github-actions-3.jpg)

-   The names of the workflows under **All workflows** on the **Actions** tab must match with the workflows saved under the `.github/workflows` directory of your repository.

    ![Placement of workflow files in the Actions tab](../image/integration-with-github-actions-4.jpg)

-   A display name must be given for every job and must be unique for every job in the workflow. The job name must match with the stage name in the custom action.

    ![Job name in custom action](../image/github-actions-jobname.png)

-   Use the `workflow_dispatch` event to trigger a workflow manually.

    ![Manually triggering a workflow using an event](../image/integration-with-github-actions-5.jpg)


## GitHub Actions workflow run details in DevOps

After you configure the webhooks, the notifications from GitHub Actions are sent to ServiceNow DevOps whenever a workflow is executed or triggered.

The following details are sent to the ServiceNow instance when a workflow is manually executed or triggered automatically on a GitHub repository.

-   The workflow\_job webhook notifies the ServiceNow instance with status of the job \(queued, in\_progress, completed\) when the workflow is manually run or automatically triggered on a GitHub Repository.
-   Inbound Events are created in the ServiceNow instance for status of the job \(queued, in\_progress, and completed\) and in\_progress events are ignored.
-   Queued and completed inbound events are processed and ServiceNow DevOps Pipeline Steps and Orchestration Tasks are created for jobs configured in the workflow.
-   Pipeline Execution is created for every workflow run with Task Executions and Step Executions records created for each job executed in the workflow run.
-   You can use the Pipeline UI to visualize interactions and results across a pipeline execution.

## GitHub re-runs

Change requests created for GitHub jobs are re-used if the change requests are in the implement and post-implement stages. For example, for a pipeline execution:

-   If a job fails before the change request is in the implement stage, the change request created will not be re-used when the failed jobs are re-run.
-   If the failed jobs or all jobs are re-run, a new change request will be created.
-   Now if a job fails when the change request is in the implement or post-implement stages, the change request will be re-used when the failed jobs or all jobs are re-run.

    **Note:** If the change request is already implemented in a previous step before the job failed, then the during re-runs, the pipeline execution will not be stopped. The change request is considered as already approved and implemented.


**Composite workflows**

For composite workflows where one workflow calls another workflow and the change step is in the child workflow, the **job-name** parameter for the change step must be of the format `job-name: '<parent-job-name> / <child-job-name>'`. Here the space before and after the forward slash \(/\) is mandatory.

![Sample job-name parameter.](../image/gh-actions-rerun-eg.png "Example of a job-name parameter in the child workflow")

## GitHub Actions limitations for DevOps Change Velocity integration

-   GitHub Actions and GitHub Environments are supported in GitHub Enterprise Server starting from version 3.3.
    -   For detailed information about GitHub environments, see [Using environments for deployment](https://docs.github.com/en/actions/deployment/targeting-different-environments/using-environments-for-deployment).
    -   GitHub environments are available to private repositories only in GitHub Enterprise Cloud.
-   For GitHub Organizations, use a specific account \(with access to the required organizations\) with personal access token for integrating with ServiceNow DevOps or you can also use GitHub Apps through Authorization Code 2.0 or JWT.

    For tool creation using GitHub Apps - JWT, you must create separate tool for separate organization.

-   Only the latest GitHub Actions scan results can be pulled from an instance for a workflow run.
-   ServiceNow DevOps Change Automation using custom action or environment is not supported for parallel jobs. For parallel jobs, the webhook notification payload does not contain information on the jobs executed in parallel with a sequence number. Due to this limitation, the sequence of jobs depends on the execution order returned by the response of the \(/repos/\{owner\}/\{repo\}/actions/runs/\{run\_id\}/jobs\) API.
-   Callback URL to pause and resume workflow run from the ServiceNow instance is supported only with GitHub Actions Deployment Gates feature. However, change creation is possible through both deployment gates and GitHub Custom Action.
-   User who creates GitHub tool in the ServiceNow instance must be a reviewer to approve the workflow for GitHub Environments.

**Parent Topic:**[GitHub integration with DevOps Change Velocity](github-integration-dev-ops.md)

**Related topics**  


[Configure webhooks in GitHub manually](../task/config-webhooks-github-manually.md)

