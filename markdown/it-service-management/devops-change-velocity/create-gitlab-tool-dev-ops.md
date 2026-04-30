---
title: Onboard GitLab to DevOps Change Velocity — Classic
description: Create an GitLab tool record in DevOps Change Velocity to connect, discover, and import GitLab tool data.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard GitLab to DevOps Change Velocity — Classic

Create an GitLab tool record in DevOps Change Velocity to connect, discover, and import GitLab tool data.

## Before you begin

Complete the steps specified in the [Getting started](../concept/setting-up-devops-change-velocity.md) section before connecting to a tool.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## About this task

-   **Connect** by using your GitLab instance details.
-   **Discover** plans, repositories, and pipelines.
-   **Configure** webhooks in GitLab.
-   **Import** branch and commit records, work items, task execution and step execution records.

## Procedure

1.  Enter the GitLab instance details to connect to DevOps Change Velocity.

    1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)** and create a record.

    2.  Enter a **Tool Name** and fill in the tool details.

<table id="table_hjt_jkz_xmb"><tbody><tr><td>

Tool URL

</td><td>

GitLab tool URL.

 For example:

 `https://gitlab.com`

</td></tr><tr><td>

Tool Username

</td><td>

GitLab username

</td></tr><tr><td>

Tool Password / Access Token

</td><td>

GitLab access token**Note:** Only personal access token is supported. When you generate the token, select the scope api and grant read/write access including all groups and projects, the container registry, and the package registry.

</td></tr></tbody>
</table>        For a list of all the permissions required on the credentials for connecting to GitLab, see GitLab permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    3.  Select **MID Server** for an on-premises tool that is attached to a MID Server.

        The **Application** value is automatically set to DevOps and the **Capability** value is set to REST.

    4.  Click **Submit**.

        The tool is connected successfully.

2.  On successful tool creation, you’re taken to the tool record page.
3.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

4.  Click **Discover** to discover existing plans, repositories, and pipelines, and fill in the fields in the project Search Filter window.

    **Note:** GitLab plans, repos, and pipelines discovered are determined by these filter conditions. To discover additional repos, modify the project filter to expand the results.

<table id="table_dbz_l1f_xmb"><tbody><tr><td>

Owned by me \(recommended\)

</td><td>

Searches for the repositories in the project that the current user owns.

</td></tr><tr><td>

Currently member of

</td><td>

Searches for the repositories in the project that the current user is a member of.

</td></tr><tr><td>

Search

</td><td>

Searches for the repositories in projects with the specified text string.

</td></tr></tbody>
</table>    **Note:** GitLab plans, repositories, and pipelines discovered are also determined by the credentials \(level of access\) configured in the connection.

    Records are added to the corresponding related lists.

5.  Automatically configure the webhook URL in a GitLab repository to send notifications to the DevOps tool by selecting **Configure**.

    Alternatively, you can choose to enable nightly polling to fetch data system for any tracked plans, repositories, or pipelines by setting the **Enable Polling** property to **Yes**.

6.  For discovered plans, repositories, and pipelines, import historical data for the tool and associate with an app.

    1.  Open the repository or plan or pipeline record from the corresponding related list and click **Import**.

        Imported branch records, commits, pipeline executions, work items and so on are added to the corresponding related lists.

    2.  In the **App** field, click the lookup list and select an App record to associate with the repository, plans, or pipeline.

    Imported historical data records are added to the corresponding related lists.


**Parent Topic:**[GitLab integration with DevOps Change Velocity](../concept/gitlab-integration-dev-ops.md)

