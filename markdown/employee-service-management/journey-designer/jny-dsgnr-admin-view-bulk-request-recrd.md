---
title: View Journey designer bulk request task records
description: View bulk update records to determine if updates were successful or failed.
locale: en-US
release: yokohama
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage Journey designer bulk updates for tasks, Configure Journey designer features, Installation and configuration overview, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# View Journey designer bulk request task records

View bulk update records to determine if updates were successful or failed.

## Before you begin

Role required: sn\_jny.admin

## Procedure

1.  Type `sn_jny_bulk_request.list` in the **All** search filter.

2.  View information about bulk updates, including status.

    -   **Created**: The date that the record was created.
    -   **Requested by**: The name of the user that requested the bulk update.
    -   **Status**:
        -   Error
        -   Requested
        -   Success
    -   **Bulk request initiated from**: The task that the bulk update was requested for.
    -   **Action taken**:
        -   Completed
        -   Skipped: Only optional tasks can be skipped.
        -   Approved
        -   Rejected
    -   **Message**: The message that is returned to the UI.
    -   **Bulk task IDs**: A number used by the system to track the bulk request.
    Links that are selectable lead to additional information for the listed column.


**Parent Topic:**[Manage Journey designer bulk updates for tasks](../concept/jny-dsgnr-bulk-update-admnstrtn.md)

