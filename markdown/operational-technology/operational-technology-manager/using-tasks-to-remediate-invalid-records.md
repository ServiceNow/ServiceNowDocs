---
title: Use OT staging tasks to remediate invalid records
description: Remediate invalid records in the SG OT Excel Stagings table by using Operational Technology \(OT\) staging tasks. Using OT staging tasks can help you track the invalid records that you need to fix.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing Validations, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Use OT staging tasks to remediate invalid records

Remediate invalid records in the SG OT Excel Stagings table by using Operational Technology \(OT\) staging tasks. Using OT staging tasks can help you track the invalid records that you need to fix.

## Before you begin

Role required: cmdb\_ot\_admin, cmdb\_ot\_editor, and ot\_staging\_user

## About this task

You can use OT staging tasks to remediate your invalid records in the SG OT Excel Stagings \(sg\_ot\_excel\_staging\) table.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Import OT Devices - Staging Table**.

2.  In the table header, select the **Create tasks** button.

    The following confirmation message appears.![Confirmation message in the table header. It states "Staging task creation process for all invalid records have started in the background. It may take a few minutes to complete."](../image/staging-task-creation-message.png)

3.  Wait for the staging task creation process to complete.

    After the staging task creation is complete, the OT Staging Task column in the table is filled in with the OT staging tasks that are related to the invalid staging records.

4.  Review and edit the staging task record.

    1.  In the OT Staging Task column, select a record.
    2.  On the staging task record form, fill in the fields if applicable.

<table id="table_l3g_glw_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the staging task. The state moves and tracks the staging tasks through several stages of remediation.

</td></tr><tr><td>

Site

</td><td>

Site that the staging task is associated with. The default staging task record has an empty Site field. All invalid staging records with empty or invalid Site fields are associated with the default staging task.**Note:** If you change the **Site** field on a staging record, the related staging task record is removed.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation of the staging task.

</td></tr><tr><td>

Opened by

</td><td>

User that created the staging task record.

</td></tr><tr><td>

Assigned to

</td><td>

User who works on the staging task.

</td></tr><tr><td>

Assignment group

</td><td>

Assigned group that works on the staging task.

</td></tr></tbody>
</table>    3.  Select **Update**.
5.  View the OT staging task records that were created in the SG OT Excel Stagings Tasks \(sg\_ot\_excel\_staging\_task\) table by navigating to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Import OT Devices - Staging Task Table**.


## Result

The staging task record is now created and assigned to the user who is responsible for remediation.

**Parent Topic:**[Managing Validations](../concept/managing-validations.md)

