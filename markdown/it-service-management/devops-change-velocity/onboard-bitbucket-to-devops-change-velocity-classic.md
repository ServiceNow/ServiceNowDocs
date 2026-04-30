---
title: Onboard Bitbucket to DevOps Change Velocity — Classic
description: Create, connect, discover, and configure your Bitbucket instance using the Classic UI.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Bitbucket, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Bitbucket to DevOps Change Velocity — Classic

Create, connect, discover, and configure your Bitbucket instance using the Classic UI.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Complete the steps specified in the [Getting started](../concept/setting-up-devops-change-velocity.md) section before connecting to a tool.

## About this task

-   **Connect** by using your Bitbucket instance details.
-   **Discover** repositories.
-   **Configure** to create the webhook in the Bitbucket repository automatically.
-   **Import** commits, branches, and pull request records.

## Procedure

1.  Enter the Bitbucket instance details to connect to DevOps Change Velocity by navigating to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  Enter a value in the **Tool Name** field and fill in the tool details.

<table id="table_jfq_lwn_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

Tool to integrate. In this case, select **Bitbucket**.

</td></tr><tr><td>

Tool URL

</td><td>

URL of the existing Bitbucket instance to integrate.

</td></tr><tr><td>

Tool username, Tool password / Access token

</td><td>

Login credentials of the existing Bitbucket instance.

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to Bitbucket, see Bitbucket permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

3.  Select **MID Server** for an on-premises tool that is attached to a MID Server.

    Application is automatically set to DevOps and capability is set to REST.

4.  Select **Submit**.

    The tool is connected successfully.

5.  On successful tool creation, you are taken to the tool record page.
6.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

7.  Select **Discover** to discover existing repositories for the coding tool.

    Repository records are added to the **Repositories** related list.

8.  Automatically configure the webhook URL in a Bitbucket repository to send notifications to the DevOps tool by selecting **Configure**.

    Alternatively, you can choose to enable nightly polling to fetch data system for any tracked repositories by setting the **Enable Polling** property to **Yes**.

9.  Select **Import** to import historical data from the repository.

    **Note:** If your tool credential has changed, you must update the credentials in your ServiceNow instance. For more information, see [Update third-party tool credentials in DevOps Change Velocity](update-third-party-tool-credentials-in-devops-change-velocity.md).

    Imported commits, branches, and pull request records from the repository are added to the corresponding related lists.

10. In the **App** field, click the lookup list and select an App record to associate with the repository, or click **New** to create one.


**Parent Topic:**[Bitbucket integration with DevOps Change Velocity](../concept/bitbucket-integration-dev-ops.md)

