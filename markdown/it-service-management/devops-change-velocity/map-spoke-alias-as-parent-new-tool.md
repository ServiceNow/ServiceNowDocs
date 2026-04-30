---
title: Map spoke alias as parent alias for new DevOps tool
description: Create Jira, GitHub or Jenkins tool with parent alias set to respective spoke alias instead of DevOps Basic authentication. Use a script include to reset parent alias to spoke alias for existing or onboarded tool.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Map spoke alias as parent alias for new DevOps tool

Create Jira, GitHub or Jenkins tool with parent alias set to respective spoke alias instead of DevOps Basic authentication. Use a script include to reset parent alias to spoke alias for existing or onboarded tool.

## Before you begin

**Important:** This feature is currently supported for Jira spoke v3.1, Jenkins spoke v2.1.1, and GitHub spoke v2.2.2, and later only.

-   Ensure that you have an Integration Hub subscription.
-   Ensure that you have set up the connection and credential alias using spoke for Jira, Jenkins and GitHub . For more information, see:
    -   [Jira spoke](https://www.servicenow.com/docs/access?context=jira-spoke-v3-0-2&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
    -   [Jenkins spoke](https://www.servicenow.com/docs/access?context=jenkins-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
    -   [GitHub spoke](https://www.servicenow.com/docs/access?context=github-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   Upgrade to DevOps Data Model and DevOps Integrations version 1.33 or later.

Role required: admin, sn\_devops.admin

## About this task

Whenever you create a Jira, Jenkins, and GitHub tool, the parent alias will be set to their respective spoke alias, if you have set up the spokes for the supported tools. In previous versions, when we created a tool, the parent alias was set to DevOps Basic Auth \(sn\_devops.DevOps\_BasicAuth\) for all the tools we onboarded.

If you have already created / onboarded tools with a connection and credential alias; the functionality does not change on upgrade and the parent alias remains DevOps Basic Auth \(sn\_devops.DevOps\_BasicAuth\) unless Jira, Jenkins, and GitHub tools are associated to spoke alias as parent alias. You can use a base system script include to ensure that the parent alias is reset to the spoke alias, for all existing and supported tools that were created earlier.

**Note:** Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes** &gt; **DevOpsReparentingConnectionAliasFixScript**.

2.  Copy the script from the **Script** field.

3.  Navigate to **System Definition** &gt; **Scripts - Background**.

4.  Paste the script in the **Run script \(JavaScript executed on server\)** field.

    **Note:** Ensure that the script is run in Global scope.

    Once the script run is successfully completed, all supported tools created prior to the version 1.33 upgrade, are reset to their corresponding parent alias.


## What to do next

Verify that the parent alias is set to sn\_jira\_spoke.Jira for Jira, sn\_github\_spoke.GitHub for GitHub, and sn\_jenkins\_v2\_spoke.Jenkins\_v2 for Jenkins in the **Connection &amp; Credentials Aliases** form.

**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

