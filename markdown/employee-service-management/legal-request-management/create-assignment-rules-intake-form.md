---
title: Assignment rule to automatically assign legal requests or matters
description: Create an assignment rule for an intake form to assign the associated legal request or matter to a user or group.
locale: en-US
release: zurich
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assigning legal request, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Assignment rule to automatically assign legal requests or matters

Create an assignment rule for an intake form to assign the associated legal request or matter to a user or group.

## Before you begin

Role required: sn\_lg\_ops.legal\_config or sn\_lg\_matter.matter\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Practice Areas**.

2.  Open the intake form from the Intake Form related list.

3.  In the Assignment Rules related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_hzh_zdb_2jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the assignment rule.

</td></tr><tr><td>

Active

</td><td>

Option for marking the assignment rule active.A legal request is assigned to a group or user based on active assignment rules only.

</td></tr><tr><td class="sub-head" colspan="2">

Applies To tab

</td></tr><tr><td>

Table

</td><td>

Name of the table to which the assignment rule applies.

</td></tr><tr><td>

Conditions

</td><td>

Conditions under which the assignment rule applies. For example, to apply a rule when a legal request is submitted in a Privacy category, you would enter the following condition:

 **\[Category\]\[is\]\[Privacy\]**.

</td></tr><tr><td class="sub-head" colspan="2">

Assign To tab

</td></tr><tr><td>

User

</td><td>

User to whom the legal request is assigned.

</td></tr><tr><td>

Group

</td><td>

User group to which the legal request is assigned.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

An assignment rule with conditions is created. Any legal request or matter that meets the rule's conditions is assigned to the specified group or user.

