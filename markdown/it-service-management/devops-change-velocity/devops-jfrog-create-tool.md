---
title: Onboard JFrog to DevOps Change Velocity — Classic
description: Connect to an instance of the JFrog artifact tool to enable you to track artifacts published to JFrog.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard JFrog to DevOps Change Velocity — Classic

Connect to an instance of the JFrog artifact tool to enable you to track artifacts published to JFrog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Complete the steps specified in the [Getting started](../concept/setting-up-devops-change-velocity.md) section before connecting to a tool.

## Procedure

1.  Enter the JFrog instance details to connect to DevOps Change Velocity by navigating to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  Enter a value in the **Tool Name** field and fill in the tool details.

<table id="table_jfq_lwn_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool integration

</td><td>

Tool to integrate. In this case, select **JFrog**.

</td></tr><tr><td>

Tool URL

</td><td>

URL of the existing JFrog instance to integrate.

</td></tr><tr><td>

Tool username, Tool password / Access token

</td><td>

Login credentials of the global admin for the existing JFrog instance.

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to JFrog, see JFrog permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

3.  Select **MID Server** for an on-premises tool that is attached to a MID Server.

    Application is automatically set to DevOps and capability is set to REST.

4.  Click **Submit**.

    **Note:** If your tool credential has changed, you must update the credentials in your ServiceNow instance. For more information, see [Update third-party tool credentials in DevOps Change Velocity](update-third-party-tool-credentials-in-devops-change-velocity.md).

    If the connection is successful, the tool is created in ServiceNow and connected to your JFrog instance.

5.  On successful tool creation, you're taken to the tool record page.
6.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.


**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

