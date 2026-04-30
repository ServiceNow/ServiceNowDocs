---
title: Create a labor rate card in Hardware Asset Workspace
description: Create a labor rate card to record the time worked on a task and associate a rate to the task.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure the Total Cost of Ownership of assets, Use, Hardware Asset Management, IT Asset Management]
---

# Create a labor rate card in Hardware Asset Workspace

Create a labor rate card to record the time worked on a task and associate a rate to the task.

## Before you begin

Role required: asset\_admin

Activate the ServiceNow® Cost Management \(com.snc.cost\_management\) plugin. For more information, see [Activate Cost Management](https://www.servicenow.com/docs/access?context=t_ActivatingCostManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations** &gt; **TCO configuration** &gt; **Labor rate card**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_pln_ql2_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Purpose of the rate card.

</td></tr><tr><td>

Active

</td><td>

Option to determine if the rate card is actively used.

</td></tr><tr><td>

Hourly rate

</td><td>

Identifies the hourly rate to be applied to task time worked entries when the worker meets the condition defined.

</td></tr><tr><td>

Order

</td><td>

Order in which the labor rate card applies to the same task.When more than one labor rate card applies to the same task, the one with the lowest order is used.

</td></tr><tr><td>

Set conditions

</td><td>

Filter to determine whether the **Use time worked** option applies to this rate card. For more information, see [Create a task rate card in Hardware Asset Workspace](create-ham-task-rate-card.md).This field uses the Condition Count widget to preview what records would be returned by the conditions.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

If you’re working on multiple HAM workflows including a labor rate card, the same value is used for all the time recorded tasks. But a labor rate card isn't included, the Default labor rate mentioned in the task rate card is used. For more information, see [Create a task rate card in Hardware Asset Workspace](create-ham-task-rate-card.md).

**Parent Topic:**[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

**Related topics**  


[Asset Total Cost of Ownership for Hardware Asset Management](../concept/asset-mgmt-tco.md)

[Asset analytics view](../concept/asset-analytics-view.md)

[Asset operations view](../concept/asset-operations-view.md)

