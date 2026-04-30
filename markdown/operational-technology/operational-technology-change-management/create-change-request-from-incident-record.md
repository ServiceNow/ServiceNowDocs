---
title: Create a change request from an incident record
description: Create an Operational Technology \(OT\) change request from an OT incident record. By creating a change request directly from an incident record, the data is automatically mapped to the new change request from the incident record.
locale: en-US
release: zurich
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Operational Technology Change Management, Operational Technology]
---

# Create a change request from an incident record

Create an Operational Technology \(OT\) change request from an OT incident record. By creating a change request directly from an incident record, the data is automatically mapped to the new change request from the incident record.

## Before you begin

Role required: sn\_ot\_incident\_write, sn\_ot\_incident\_admin, or sn\_ot\_change\_write

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace**.

2.  In the OT Incidents list module, select one of the available lists.

3.  Select the incident record that you want to create an OT change request from.

4.  Select the **Create OT Change** button.

    The Select OT change form opens.

5.  Select the change model that is applicable to your organization.

    For more information, see [Select a change model to fulfill change requests](select-change-model.md).

6.  Select **Create OT Change record**.

7.  Fill in the playbook and related forms as needed.

    For more information about the playbook and related forms, see [Basic OT Change Model playbook](../concept/basic-ot-change-model.md) and [Advanced OT Change Model playbook](../concept/advanced-ot-change-model.md) depending on which OT change model you chose.

    **Note:** In the Details related list of the new change request, the following fields and related lists are automatically filled in with the values from the related OT incident record:

    -   Site
    -   Equipment Model Entity
    -   OT Device \(CI\)
    -   Short Description
    -   Description
    -   Priority

        **Note:** A **Priority** field value from 1 through 4 is the same in the new change record. But a value of 5 in the incident record's **Priority** field is changed to 4 in the new change record.


**Parent Topic:**[Using Operational Technology Change Management](../concept/using-operational-technology-change-management.md)

