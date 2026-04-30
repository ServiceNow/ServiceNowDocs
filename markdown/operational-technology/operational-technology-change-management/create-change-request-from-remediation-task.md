---
title: Create a change request from a remediation task
description: Create an Operational Technology \(OT\) change request from an OT remediation task. Creating a change request from a remediation task automatically populates the information in your change request record, such as the Site and the OT Device fields.
locale: en-US
release: xanadu
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Create a change request from a remediation task

Create an Operational Technology \(OT\) change request from an OT remediation task. Creating a change request from a remediation task automatically populates the information in your change request record, such as the Site and the OT Device fields.

## Before you begin

Roles required: sn\_ot\_change\_write and sn\_otvr.remediation\_owner

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  Open the remediation task record that you want to create a change request from.

3.  Select the **Create OT Change** button as shown in the following example. ![Create OT Change button on a remediation task record.](../image/create-ot-change-button.png)

    **Note:** If there's no active change model, the following error appears.![Error when creating a change task without an active change model.](../image/ot-change-error-message.png)

4.  Select the OT change model that applies to your organization.

5.  Select **Next**.

6.  Complete the playbook as needed as your team works on the change request.

    For more information about the Basic OT Change Model playbook, see [Basic OT Change Model playbook](../concept/basic-ot-change-model.md). For more information about the Advanced OT Change Model playbook, see [Advanced OT Change Model playbook](../concept/advanced-ot-change-model.md).

    The following fields are automatically populated depending on the conditions that you set.

    -   The **OT Device** field is auto-populated only if the Industrial Process Manager application is enabled.
    -   If the Industrial Process Manager is installed, then the site assigned to the OT device shows up in the **Site** field.
    -   If the Industrial Process Manager is enabled and there's only one entity that is associated with the OT device, then the **Equipment model entity** field is automatically populated.

        **Note:** If multiple entities are associated with an device, the **Equipment model entity** field is left empty.


**Parent Topic:**[Using Operational Technology Change Management](../concept/using-operational-technology-change-management.md)

