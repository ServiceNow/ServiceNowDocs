---
title: Create a user hierarchy configuration record
description: Create a user hierarchy configuration record for a table so that you can enable your managers to view the records of the users who report to them.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User hierarchy, Common GRC features, Governance, Risk, and Compliance]
---

# Create a user hierarchy configuration record

Create a user hierarchy configuration record for a table so that you can enable your managers to view the records of the users who report to them.

## Before you begin

Role required: sn\_grc.admin

## Procedure

1.  Navigate to **All** &gt; **GRC User Hierarchy &gt; User hierarchy configuration**.

    The tables where you have enabled the user hierarchy access control are displayed.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_wwp_2hv_ksb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table that you can use to configure the user hierarchy. For example, Issue \[sn\_grc\_issue\].

</td></tr><tr><td>

Active

</td><td>

Option to enable the user hierarchy. When you enable this option, the user hierarchy functionality is enabled on the table records.

</td></tr><tr><td>

User reference field 1

</td><td>

Field that corresponds to User reference field 1 in the user table. For example, you can select the value of the User reference field 1 as Assignee or Assigned to.

</td></tr><tr><td>

User reference field 2

</td><td>

Field that corresponds to User reference field 1 in the user table. For example, you can select the value of the User reference field 2 as Approver or Issue manager.

</td></tr><tr><td>

User hierarchy field 1

</td><td>

Field to configure the user hierarchy for User reference field 1.

</td></tr><tr><td>

User hierarchy field 2

</td><td>

Field to configure the user hierarchy for User reference field 2.

</td></tr><tr><td>

User hierarchy status field

</td><td>

Field that represents the status of the user hierarchy processing for the selected table.

</td></tr><tr><td>

Triggered event

</td><td>

Event that is used to recalculate the user hierarchy in the source table records.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[User hierarchy](../concept/user-hierarchy.md)

