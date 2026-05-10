---
title: Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity
description: Create OAuth 2.0 credentials for GitHub Apps or OAuth apps and use them to connect your GitHub instance.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity

Create OAuth 2.0 credentials for GitHub Apps or OAuth apps and use them to connect your GitHub instance.

If you want to use Basic Authentication credentials instead of OAuth 2.0, skip this section and proceed to onboard GitHub using one of the following options:

-   [Onboard GitHub to DevOps Change Velocity — Workspace](../task/playbook-enter-github-instance-details.md).
-   [Onboard GitHub to DevOps Change Velocity — Classic](../task/create-github-tool-dev-ops.md).

**Note:** The OAuth Authorization Code &amp; JWT grant types are supported for GitHub &amp; GitHub Enterprise with MID server.

**Note:** DevOps connection and credential aliases \(DevOpsAlias1 through DevOpsAlias10\) are used to connect automatically when you set up your GitHub instance using OAuth 2.0. To connect to more than 10 tools, or if you receive an error saying all DevOpsAlias connection and credential aliases are being used, an admin can create additional aliases in the sn\_devops application scope. For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md). If necessary, you can reuse a DevOpsAlias alias that is no longer in use by inactivating the HTTP connection.

-   **[OAuth 2.0 credentials for GitHub Apps - JWT](dev-ops-github-apps-oath-jwt.md#)**  
Perform the following steps to integrate your GitHub Apps using the JWT bearer token.
-   **[OAuth 2.0 credentials for GitHub Apps - Authorization Code](dev-ops-github-apps-oauth-auth.md#)**  
Perform the following steps to integrate your GitHub Apps using Authorization code.

**Parent Topic:**[GitHub integration with DevOps Change Velocity](github-integration-dev-ops.md)

