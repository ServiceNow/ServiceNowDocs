---
title: Manage a task rate card
description: Task rate cards are rate cards associated with records in a task table.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Task and labor rate cards, Cost Management, Strategic Portfolio Management]
---

# Manage a task rate card

Task rate cards are rate cards associated with records in a task table.

## Before you begin

Role required: financial\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Costs**.

2.  Create or edit a record \(see table for details\).

<table id="simpletable_ekz_2ss_qq"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String field summarizing the purpose of the rate card.

</td></tr><tr><td>

Table

</td><td>

Which type of tasks the rate card applies to.

</td></tr><tr><td>

Order

</td><td>

If more than one task rate card apply to the same task, the one with the lowest order is used.

</td></tr><tr><td>

Active

</td><td>

Check box which determines if the rate card will be actively used.

</td></tr><tr><td>

Summary type

</td><td>

High-level type of expense for easier summary reports. This value will be used to set the expense line summary type field.

</td></tr><tr><td>

Condition

</td><td>

Filter to run on the table selected to determine whether this rate card applies to a given task. This field uses the Condition Count Widget to preview what records would be returned by the conditions.

</td></tr><tr><td>

Task rate

</td><td>

Rate of the task, with a currency list. To add a new currency, use the **Edit** link.

</td></tr><tr><td>

Use time worked

</td><td>

By default a flat rate per task is defined in the rate card. Selecting the check box will force the rule to calculate the task cost based on the related task time worked entries.

</td></tr><tr><td>

Default labor rate

</td><td>

Defines the default hourly rate to apply to the time worked entries if the worker does not have a labor rate card. Displayed when **Use time worked** is selected.

</td></tr></tbody>
</table>
**Parent Topic:**[Task and labor rate cards](../concept/c_TaskAndLaborRateCards.md)

