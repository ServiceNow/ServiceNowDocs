---
title: Onboard GitHub to DevOps Change Velocity — Classic
description: Connect your GitHub instance to discover, configure, and import repositories, plans, and pipelines.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard GitHub to DevOps Change Velocity — Classic

Connect your GitHub instance to discover, configure, and import repositories, plans, and pipelines.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Complete the steps specified in the [Getting started](../concept/setting-up-devops-change-velocity.md) section before connecting to a tool.

## About this task

-   **Connect** to GitHub and get the webhook URL when you submit a DevOps tool record.
-   **Discover** repositories and plans.
-   **Configure** the webhook in the GitHub repository.
-   **Import** branch and commit records.

## Procedure

1.  Enter the GitHub instance details to connect to DevOps Change Velocity by navigating to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  Enter a value in the **Tool Name** field and fill in the tool details.

<table id="table_jfq_lwn_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

Tool to integrate. In this case, select **GitHub**.

</td></tr><tr><td>

Tool URL

</td><td>

URL of the existing GitHub instance to integrate. For e.g, https://api.github.com

</td></tr><tr><td>

GitHub credential type

</td><td>

-   Basic Auth

    -   GitHub username
    -   Personal access token \(classic\)
Only a personal access token \(classic\) is supported with basic authentication. When you generate a personal access token \(classic\) for GitHub, you must specify the scopes to authorize if you are not granting complete access. The minimum scopes that you must select for authorization are repo, admin:repo\_hook, and user:email.

-   OAuth

GitHub Tool Credential. See [Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity](../concept/setting-up-github-oauth-dev-ops.md).

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to GitHub, see GitHub permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

3.  Select **MID Server** for an on-premises tool that is attached to a MID Server.

    Application is automatically set to DevOps and capability is set to REST.

    **Note:** The OAuth Authorization Code &amp; JWT grant types are supported for GitHub &amp; GitHub Enterprise with MID server.

4.  Select **Submit**.

5.  On successful tool creation, you are taken to the tool record page.
6.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

7.  Select **Discover** to discover existing repositories, plans, or pipelines for the tool.

    Repository records are added to the Repositories related list.

8.  Automatically configure the webhook URL in a GitHub repository to send notifications to the DevOps tool by selecting **Configure**.

    Alternatively, you can choose to enable nightly polling to fetch data system for any tracked repositories or pipelines by setting the **Enable Polling** property to **Yes**.

    **Note:** If you do not have admin privileges for your GitHub tool \(to allow automatic configuration of the webhook URL\), you might need to have the tool admin user configure it for you \(create and configure the webhook URL manually in your tool instance\). Once the webhook is configured in the tool, Enter Manual Configuration Mode to connect to the tool manually, then exit.

9.  Click **Import** to import historical data from the repository.

    Imported branch records and commit records from the repository are added to the corresponding related lists.

10. In the **App** field, click the lookup list and select an App record to associate with the repository, or click **New** to create one.


**Parent Topic:**[GitHub integration with DevOps Change Velocity](../concept/github-integration-dev-ops.md)

