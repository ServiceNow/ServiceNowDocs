---
title: Approval definition form
description: Release admins can create approval definitions to get approvals of phase tasks for a release.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Digital Product Release, IT Service Management]
---

# Approval definition form

Release admins can create approval definitions to get approvals of phase tasks for a release.

For more information, see [Create an approval definition in Digital Product Release](../task/dpr-create-approval-definition.md).

<table id="table_rmd_rj5_lyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the approval definition.Providing a meaningful name that helps to identify the purpose of the approval.

</td></tr><tr><td>

Active

</td><td>

Option for marking the approval definition active.Only active approval definitions are available for selection when creating a task or task template.

</td></tr><tr><td>

Approver source

</td><td>

Source of the user or group who approves the tasks.-   **Approval Definition**: Selects a specific user or group.
-   **Digital Product**: Selects the user or group determined dynamically through a user reference field from the Application Models \[cmdb\_application\_product\_model\] table.
-   **Service**: Selects the user or group determined dynamically through a user reference field from the Service Models \[cmdb\_service\_product\_model\] table.

</td></tr><tr><td>

Approval action

</td><td>

Options for directing the approval to:-   An individual user based on the role
-   A user group

</td></tr><tr><td>

User field

</td><td>

Fields from the User \[sys\_user\] table.Select a user field. When an approval is initiated from a task, the approval request is directed to the person whose name is in that **User** field. For example, if you select the **Manager** user field, the approval record is assigned to the manager of the individual assigned with the task.

This field appears only when **User** is selected from **Approval action**.

</td></tr><tr><td>

Group field

</td><td>

Fields from the Groups \[sys\_user\_group\] table.Select a group field. When an approval is initiated from a task, the approval request is directed to members of the group listed in the **Group** field.

This field appears only when **Group** is selected from **Approval action**.

</td></tr><tr><td>

Wait for

</td><td>

Option to determine when an approval request should be considered approved.-   All responses: The request is considered approved when all group members approve it.
-   First response: The request is considered approved when any one of the group members approves it.
-   Percentage of users: The request is considered approved when the minimum specified percentage of group members approves it.

When you select this option, enter the percentage in the **Percentage** field.


This field appears only when **Group** is selected from **Approval action**.

</td></tr></tbody>
</table>**Parent Topic:**[Digital Product Release reference](../concept/dpr-reference.md)

