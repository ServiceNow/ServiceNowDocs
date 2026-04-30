---
title: Create a change request from OT device details
description: Create an Operational Technology \(OT\) change request from an OT device record. Creating a change request from a device record automatically populates the information in your change request record, such as the site or business service and the OT Device field.
locale: en-US
release: xanadu
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Create a change request from OT device details

Create an Operational Technology \(OT\) change request from an OT device record. Creating a change request from a device record automatically populates the information in your change request record, such as the site or business service and the OT Device field.

## Before you begin

Role required: sn\_ot\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  In the All OT Devices list, select an OT device record.

3.  Under the **Related Records** tab, select the OT Change Requests related list.

4.  Select **New**.

5.  Select the OT change model that applies to your organization.

6.  Select **Create OT Change Record**.

7.  Complete the playbook as needed as your team works on the change request.

    For more information about the Basic OT Change Model playbook, see [Basic OT Change Model playbook](../concept/basic-ot-change-model.md). For more information about the Advanced OT Change Model playbook, see [Advanced OT Change Model playbook](../concept/advanced-ot-change-model.md).

    The following fields are automatically populated depending on the conditions that you set.

    -   The **OT Device** field is auto-populated only if the Industrial Process Manager application is enabled.
    -   If the Industrial Process Manager is installed, then the site assigned to the OT device shows up in the **Site** field.
    -   If the Industrial Process Manager is enabled and there's only one entity that is associated with the OT device, then the **Equipment model entity** field is automatically populated.

        **Note:** If multiple entities are associated with an device, the **Equipment model entity** field is left empty.


## Result

The change request is created, and the users in the Assignment group, Assigned to, and Watch list fields are notified.

**Parent Topic:**[Using Operational Technology Change Management](../concept/using-operational-technology-change-management.md)

