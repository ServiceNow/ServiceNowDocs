---
title: Remove a task type from bulk update
description: As an admin you can remove a task type from the types available for bulk update.
locale: en-US
release: australia
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Journey designer bulk updates for tasks, Configure Journey designer features, Configure, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Remove a task type from bulk update

As an admin you can remove a task type from the types available for bulk update.

## Before you begin

Role required: sn\_jny.admin

## Procedure

1.  Type `sys_properties.list` in the **All** search filter.

2.  Press enter.

3.  Search for `Journey designer` in the **Application** column.

    If the **Application** column isn't visible, select the gear icon to add the **Application** column to the **Personalize List Columns**.

4.  Select **sn\_jny.bulk\_management\_task\_type** from the name column.

    **Note:** You must be in the Journey designer scope to be able to edit this property.

5.  In the **Value** field, delete any task type entry that you want removed from the bulk update feature.

    ```
    {
    "sn_hr_core_task": ["submit_catalog_item", "submit_order_guide", "mark_when_complete"],
    "sysapproval_approver": true
    }
    ```

    -   Approval \[sysapproval.approver\]
    -   Mark when complete \[mark\_when\_complete\]
    -   Submit catalog item \[submit\_catalog\_item\]
    -   Submit order guide \[submit\_order\_guide\]
6.  Select **Update**.


**Parent Topic:**[Manage Journey designer bulk updates for tasks](../concept/jny-dsgnr-bulk-update-admnstrtn.md)

