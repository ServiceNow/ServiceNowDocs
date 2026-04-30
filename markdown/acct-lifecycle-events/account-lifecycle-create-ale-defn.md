---
title: Create an ALE definition record
description: Create an ALE definition record to set up categories and sub categories for success play workflows.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure customer success, Customer success, Customer Success Management]
---

# Create an ALE definition record

Create an ALE definition record to set up categories and sub categories for success play workflows.

## Before you begin

-   The subflow used to trigger the success workflow must be defined.
-   Role required: sn\_acct\_lc.ale\_success\_play\_admin

## About this task

Use the ALE definition record to specify categories that can be used to launch success play workflows that can create records and trigger playbooks automatically.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **ALE Definition** and click **New**.

3.  On the form, fill in the fields.

<table id="table_ddj_yyb_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flow

</td><td>

Select the subflow that should be triggered by this ALE definition record. This subflow must be defined and configured using Flow Designer.

</td></tr><tr><td>

Category

</td><td>

Select the category for the success play.

</td></tr><tr><td>

Sub category

</td><td>

Based on the category you select, the related sub categories are displayed. Select the sub category from the drop down list.

</td></tr><tr><td>

State

</td><td>

Select the state for this ALE definition record. This can be:-   Draft
-   Published
-   Closed
-   Canceled


</td></tr><tr><td>

Order

</td><td>

Specify the order in which the categories should appear in the workflow launcher pages.

</td></tr><tr><td>

Title

</td><td>

Enter a title for the workflow launcher item.

</td></tr><tr><td>

Description

</td><td>

Enter a description to specify the purpose of this workflow launcher item.

</td></tr></tbody>
</table>4.  Set the state of this record to **Published** and click **Save**.

    The category defined here can be used while creating the success play.


