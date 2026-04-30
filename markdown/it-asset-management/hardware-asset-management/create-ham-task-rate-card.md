---
title: Create a task rate card in Hardware Asset Workspace
description: Create a task rate card to define the type of task and the method of calculating the associated costs.
locale: en-US
release: xanadu
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure the Total Cost of Ownership of assets, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Create a task rate card in Hardware Asset Workspace

Create a task rate card to define the type of task and the method of calculating the associated costs.

## Before you begin

Role required: asset\_admin

Activate the ServiceNow® Cost Management \(com.snc.cost\_management\) plugin. For more information, see [Activate Cost Management](https://www.servicenow.com/docs/access?context=t_ActivatingCostManagement&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Asset operations** &gt; **TCO configuration** &gt; **Task rate card**.

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

Use time worked

</td><td>

Option for forcing the rule to calculate the task cost based on the related task time worked entries.

By default, a flat rate for each task is defined in the **Task rate** field.

</td></tr><tr><td>

Table

</td><td>

The type of tasks the rate card applies to.

</td></tr><tr><td>

Active

</td><td>

Option to determine if the rate card is actively used.

</td></tr><tr><td>

Task rate

</td><td>

Rate of the task, with a currency list.To add a new currency, use the Edit link.

</td></tr><tr><td>

Default labor rate

</td><td>

The default hourly rate to apply to the time worked entries if the worker doesn’t have a labor rate card. This field appears only when **Use time worked** is selected.

</td></tr><tr><td>

Order

</td><td>

Order in which the task rate card applies to the same task.When more than one task rate card applies to the same task, the one with the lowest order is used.

</td></tr><tr><td>

Set conditions

</td><td>

Filter to run on the table selected to determine whether this rate card applies to a given task. This field uses the Condition Count Widget to preview what records would be returned by the conditions.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

After a task rate card is defined for a task, expense lines are created by the **Use time worked** value. When you select the Use time worked field for a task rate card, the time worked records created against users and labor rate are used to calculate expense lines. For more information, see [Process task rate cards](https://www.servicenow.com/docs/access?context=r_ProcessTaskRateCards&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

**Parent Topic:**[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

**Related topics**  


[Asset Total Cost of Ownership for Hardware Asset Management](../concept/asset-mgmt-tco.md)

[Asset analytics view](../concept/asset-analytics-view.md)

[Asset operations view](../concept/asset-operations-view.md)

