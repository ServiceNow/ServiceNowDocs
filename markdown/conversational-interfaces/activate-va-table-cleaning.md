---
title: Activate table cleaning for Virtual Agent tables
description: Activate table cleaning for certain tables used in Virtual Agent and Conversational Interfaces.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data management in Conversational Interfaces, Conversational Interfaces reference, Conversational Interfaces Console, Conversational Interfaces]
---

# Activate table cleaning for Virtual Agent tables

Activate table cleaning for certain tables used in Virtual Agent and Conversational Interfaces.

## Before you begin

Role required: admin

## About this task

You can activate table cleaning for these Virtual Agent and Conversational Interfaces tables:

-   Chat Server \[sys\_cs\_analytics\]
-   Conversations \[sys\_cs\_conversation\]
-   Message Last Reads \[sys\_cs\_message\_last\_read\]
-   Ci Analytics \[sys\_ci\_analytics\]

## Procedure

1.  Open the Auto Flush \[sys\_auto\_flush\] table by typing `sys_auto_flush.list` in the filter navigator.

2.  Select the table to be activated for cleaning.

3.  Change the fields in the form as needed.

<table id="table_b5k_mgm_yrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Age in seconds

</td><td>

The time, in seconds, that specifies when records in the table are to be deleted.

 To change the age, enter the new value in seconds.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate table cleaning for this table. Select this option to activate table cleaning.

</td></tr><tr><td>

Cascade delete

</td><td>

Option to activate or deactivate table cleaning for related tables. Some tables may have child tables that are also automatically cleaned.

</td></tr><tr><td>

Conditions

</td><td>

Condition builder for specifying filter conditions that define the records to be removed.

</td></tr></tbody>
</table>4.  Select **Update**.

    The Table Cleaner scheduled job automatically runs the cleaner when the table records meet the specified record age and any conditions that you set for them.


**Parent Topic:**[Data management in Conversational Interfaces](../concept/va-data-mgmt.md)

