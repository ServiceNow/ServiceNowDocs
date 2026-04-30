---
title: Recalculate costs of resource assignments of a demand
description: Recalculate the costs of all active resource assignments of a demand whenever the hourly rates change in the associated rate model so that the plan costs are up to date.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and manage resource assignments, Create a demand, Use, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Recalculate costs of resource assignments of a demand

Recalculate the costs of all active resource assignments of a demand whenever the hourly rates change in the associated rate model so that the plan costs are up to date.

## Before you begin

Ensure the following setup:

-   The demand must be active.
-   The demand must have an active rate model assigned.

Role required: demand\_manager

## About this task

This option recalculates the costs of all resource assignments of the demand at once. You can also open a resource assignment from the **Resource assignments** related list to [recalculate the resource costs of an individual resource assignment](../../resource-management/task/recalculate-resource-costs.md).

## Procedure

1.  Navigate to **All** &gt; **Demand** &gt; **Demands** &gt; **All**.

2.  Open a demand.

3.  On the Demand form, right-click on the header bar and select the **Recalculate Resource Costs**.

4.  In the Recalculate Resource Cost form, fill in the fields.

    For a description of the field names, see [Recalculate resource costs form](../reference/recalculate-resource-costs-form.md).

5.  Click **OK**.


## Result

-   Recalculates the selected resource costs of all the applicable resource assignments in the demand based on the latest hourly rates. The hourly rates are derived from the rate model associated with the demand.
-   Updates the recalculated resource costs on the respective cost fields on the resource assignment form and the Resource assignments related list.
-   Reflects the revised values in the respective cost fields of the demand.

**Parent Topic:**[Create and manage resource assignments for a demand](create-manage-resource-plans-demand.md)

