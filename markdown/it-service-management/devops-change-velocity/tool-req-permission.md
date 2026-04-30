---
title: Permissions required for DevOps tools
description: Permissions required in your third-party tool to connect to DevOps Change Velocity.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Check permissions and update credentials, Manage, DevOps Change Velocity, IT Service Management]
---

# Permissions required for DevOps tools

Permissions required in your third-party tool to connect to DevOps Change Velocity.

## Azure DevOps permissions

**Important:** With the access level permissions specified in the following table in Azure DevOps, and the ServiceNow DevOps extension, you can connect to Azure DevOps from ServiceNow. Your Azure DevOps admin does not have to manually configure webhooks and service connections in Azure DevOps.

**Important:**

-   When onboarding a Project, the **Project Administrators** privilege requires the owner of the PAT to be a member of the project's **Project Administrators** group.
-   When onboarding an Organization, the **Project Administrators** privilege requires the owner of the PAT to be a member of the organization's **Project Collection Administrators** group.

<table id="table_of5_fy5_txb"><thead><tr><th>

Object

</th><th>

Permissions required

</th><th>

Impact

</th></tr></thead><tbody><tr><td>

Work Items

</td><td>

Read

</td><td>

Required to discover the boards and receive the work items either through import, polling, or real time with a configured webhook.

</td></tr><tr><td>

Code

</td><td>

Read

</td><td>

Required to discover repositories and receive branches, commits, and tags either through import, polling, or real time with a configured webhook.

</td></tr><tr><td>

Build

</td><td>

Read and execute

</td><td>

Read: Required to discover the build pipelines and receive pipeline execution details like stages, artifacts, test results, code security results, and so on, either through import, polling, or real time with a configured webhook.

 Execute: Required to pause or resume the pipelines based on the change control step.

</td></tr><tr><td>

Release

</td><td>

Read, write, and execute

</td><td>

Read: Required to discover the release pipelines and receive pipeline execution details like stages, artifacts, test results, code security results, and so on, either through import, polling, or real time with a configured webhook.

 Write and Execute: Required to pause or resume the pipelines based on change control step.

</td></tr><tr><td>

Test Management

</td><td>

Read

</td><td>

Required to receive test results for pipeline execution.

</td></tr><tr><td>

Service Connections

</td><td>

Read, query, and manage

</td><td>

Required to create Service connection automatically which is used to configure ServiceNow tasks like change acceleration, artifact, and package registration, and so on.

</td></tr><tr><td>

Packaging

</td><td>

Read

</td><td>

Required to discover the artifact repositories and receive the feeds and packages either through import, polling, or real-time with a configured webhook.

</td></tr><tr><td>

Permissions

</td><td>

Project Administrators

</td><td>

Required to create webhooks automatically to receive data in real-time and to create Service connections automatically which is used to configure ServiceNow tasks like change acceleration, artifact and package registration, and so on.

</td></tr></tbody>
</table>-   **Limitation of Azure DevOps**

    If you create an Azure tool with custom defined access level, and you reconfigure such a tool because of change in your Integration user credentials, then the existing service hooks for release created and release deployment are not updated. Instead, two new service hooks are created with new configuration details. To avoid the duplication of these service hooks, you must create the tool with full access level.


## Bitbucket

|Object|Permissions required|Impact|
|------|--------------------|------|
|Account|Read|Required to discover repos and fetch branches, commit, pull requests, and tags either through import, polling, or configured webhook.|
|Projects|Read|Required to discover repos and fetch branches, commit, pull requests, and tags either through import, polling, or configured webhook.|
|Webhooks|Read and write|Required to discover repos and fetch branches, commit, pull requests, and tags either through import, polling, or configured webhook.|
|Pull requests|Read|Required to discover repos and fetch branches, commit, pull requests, and tags either through import, polling, or configured webhook.|

## GitHub permissions

The following table lists the GitHub permissions for basic authentication.

|Object|Permissions required|Impact|
|------|--------------------|------|
|repo|repo|Required to discover repositories and their respective workflows and receive branches, commits, pull requests, and tags either through import, polling, or real-time with a configured webhook.|
|admin:repo\_hook|write:repo\_hook|Required to create webhooks automatically to receive repo data in real time.|
|admin:repo\_hook|read:repo\_hook|Required to lookup already existing webhooks before any new webhook is automatically created to receive repo data in real time.|
|user|user:email|Required to discover pull requests actors like approvers, raised by, merged by, reviewers, and assignees either through import, polling, or real time with a configured webhook.|

The following table lists the GitHub permissions required for OAuth 2.0 authentication.

<table id="table_pzz_pvr_szb"><thead><tr><th>

Object

</th><th>

Permissions required

</th><th>

Impact

</th></tr></thead><tbody><tr><td>

Actions

</td><td>

Read-only

</td><td>

Required to receive workflows associated to the respective repos real time with a configured webhook.

</td></tr><tr><td>

Contents

</td><td>

Read-only

</td><td>

Required to discover repositories and its respective workflows and receive branches, commits, and tags either through import/polling or real time with a configured webhook.

</td></tr><tr><td>

Deployments

</td><td>

Read and write

</td><td>

Required to resume the workflow which has environment with ServiceNow change as an environment secret.

</td></tr><tr><td>

Environments

</td><td>

Read-only

</td><td>

Required to lookup for existing environment secrets for change creation.

</td></tr><tr><td>

Metadata

</td><td>

Read-only

</td><td>

Required to discover repositories and its respective workflows.

</td></tr><tr><td>

Secrets

</td><td>

Read-only

</td><td>

Required to get access to environment secrets \(to create change\).

</td></tr><tr><td>

Webhooks

</td><td>

Read and write**Note:** Read and write permissions are required to configure webhooks from ServiceNow.

</td><td>

Required to create webhook automatically to receive repo data in real time.

</td></tr><tr><td>

Pull requests

</td><td>

Read-only

</td><td>

Required to discover pull requests and receive related details like pull request ID, commits, raised by, approvers, comments, reviewers, etc., either through import/polling or real time with a configured webhook.

</td></tr><tr><td>

Checks

</td><td>

Read-only

</td><td>

Required to process workflow events associated with private repositories.

</td></tr></tbody>
</table>## GitLab permissions

|Object|Permissions required|Impact|
|------|--------------------|------|
|api|Read and write|Required to discover plans, repos, and pipelines and receive branches, commit, and tags, and pipeline execution details \(like stages, artifacts, test results, code security results\), work items, tags, branches, and commits either through import, polling, or real time with a configured webhook. Also, to pause or resume the pipelines based on change control step.|

## Jenkins permissions

|Object|Permissions required|Impact|
|------|--------------------|------|
|Overall|Read|Required to discover the pipelines and receive pipeline execution details like jobs or stages, artifacts, test results, code security results, and so on, either through import, polling, or real time with ServiceNow DevOps Jenkins plugin.|
|Job|Read|Required to discover the pipelines and receive pipeline execution details like jobs or stages, artifacts, test results, code security results, and so on, either through import, polling, or real time with ServiceNow DevOps Jenkins plugin.|

## JFrog permissions

|Object|Permissions required|Impact|
|------|--------------------|------|
|Roles|Administer Platform|Required to access artifact details like artifact name, artifact repo, and artifact version.|

## Jira permissions

|Object|Permissions required|Impact|
|------|--------------------|------|
|Groups|jira-software-users|Required to discover plans and fetch features, stories, and so on, either through import, polling, or configured webhook.|
|Permissions|Jira Administrators|Required to create webhooks automatically for fetching features and stories in real time.|

**Parent Topic:**[Check permissions and update credentials for tools — Workspace](update-credentials-check-permissions.md)

