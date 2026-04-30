---
title: Modify assignment rule for contract requests
description: As a contracts configurator modify the assignment rule available in the base system for any changes required in the user or group to whom the contract request should be assigned.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Modify assignment rule for contract requests

As a contracts configurator modify the assignment rule available in the base system for any changes required in the user or group to whom the contract request should be assigned.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment**.

2.  Open the assignment rule Default assignment Group for CLM request

3.  On the form, modify the fields.

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

Option for marking the assignment rule active.The contract request is assigned to a group or user based on active assignment rules only.

</td></tr><tr><td class="sub-head" colspan="2">

Applies To tab

</td></tr><tr><td>

Table

</td><td>

Name of the table to which the assignment rule applies.

</td></tr><tr><td>

Conditions

</td><td>

Conditions under which the assignment rule applies. For example, to apply a rule when a contract request is submitted for Own type paper, you would enter the following condition.

**\[Type of paper\]\[is\]\[Own paper\]**

</td></tr><tr><td class="sub-head" colspan="2">

Assign To tab

</td></tr><tr><td>

User

</td><td>

User to whom the contract request is assigned.

</td></tr><tr><td>

Group

</td><td>

User group to which the contract request is assigned.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Managing Contract Management Pro](../concept/cncore-manage-cmpro.md)

**Related topics**  


[Manage clauses, tables, and contract templates](../concept/cncore-manage-clauses-ctemplates.md)

[Manage contract records](cncore-manage-cont-records.md)

[Platform Analytics Solutions for Contract Management Pro](../../../use/application-content-packs/concept/cncore-analytics-pa.md)

