---
title: Azure DevOps PAT scopes for DevOps
description: Scope access levels are required when using a personal access token \(PAT\) to access Azure DevOps during setup.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Azure DevOps PAT scopes for DevOps

Scope access levels are required when using a personal access token \(PAT\) to access Azure DevOps during setup.

Scope access level settings are based on the capability you have configured. Set the corresponding access level for seamless functionality. For information on creating a PAT, see [Personal access token \(PAT\)](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page).

**Important:** With the access level permissions specified in the following table in Azure DevOps, and the ServiceNow DevOps extension, you can connect to Azure DevOps from ServiceNow. Your Azure DevOps admin does not have to manually configure webhooks and service connections in Azure DevOps.

**Important:**

-   When onboarding a Project, the **Project Administrators** privilege requires the owner of the PAT to be a member of the project's **Project Administrators** group.
-   When onboarding an Organization, the **Project Administrators** privilege requires the owner of the PAT to be a member of the organization's **Project Collection Administrators** group.

<table id="table_pat_ado"><thead><tr><th>

Capability

</th><th>

Scope

</th><th>

Access level

</th><th>

Impact

</th></tr></thead><tbody><tr><td>

Boards

</td><td>

Work item

</td><td>

Read

</td><td>

Required to discover the boards and receive the work items either through import/polling or real time with a configured webhook.

</td></tr><tr><td>

Repos

</td><td>

Code

</td><td>

Read

</td><td>

Required to discover repositories and receive branches, commits, and tags either through import/polling or real time with a configured webhook.

</td></tr><tr><td>

Build pipelines

</td><td>

Build

</td><td>

Read &amp; Execute

</td><td>

-   Read: Required to discover the build pipelines and receive pipeline execution details like stages, artifacts, test results, code security results, etc., either through import/polling or real time with a configured webhook.
-   Execute: Required to pause/resume the pipelines based on the change control step.

</td></tr><tr><td>

Release pipelines and gates

</td><td>

Release

</td><td>

Read, write and execute

</td><td>

-   Read: Required to discover the release pipelines and receive pipeline execution details like stages, artifacts, test results, code security results, etc, either through import/polling or real time with a configured webhook.
-   Write and Execute: Required to pause/resume the pipelines based on change control step.

</td></tr><tr><td>

Test build and release pipelines

</td><td>

Test management

</td><td>

Read

</td><td>

Required to receive test results for pipeline execution.

</td></tr><tr><td>

Service Connections

</td><td>

Service connection

</td><td>

Read, query, and manage

</td><td>

Required to create Service connection automatically which is used to configure ServiceNow tasks like change acceleration, artifact and package registration, etc.

</td></tr><tr><td>

Packaging

</td><td>

Packaging

</td><td>

Read

</td><td>

Required to discover the artifact repositories and receive the feeds and packages either through import/polling or real-time with a configured webhook.

</td></tr></tbody>
</table>**Note:** You must have the Update build information permission on your pipeline for all pipeline features to work seamlessly. Contact your ADO Project Administrator if you don't have this permission.

## Limitation of Azure DevOps

If you create an Azure tool with custom defined access level, and you reconfigure such a tool because of change in your Integration user credentials, then the existing service hooks for release created and release deployment are not updated. Instead, two new service hooks are created with new configuration details. To avoid the duplication of these service hooks, you must create the tool with full access level.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

