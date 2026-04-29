---
title: Recalculate costs of resource assignments of a demand
description: Recalculate the costs of all active resource assignments of a demand whenever the hourly rates change in the associated rate model. This feature helps keep the plan costs are up to date.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage resource assignments, Manage demands, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Recalculate costs of resource assignments of a demand

Recalculate the costs of all active resource assignments of a demand whenever the hourly rates change in the associated rate model. This feature helps keep the plan costs are up to date.

## Before you begin

-   The demand must be active.
-   The demand must have an active rate model assigned.

Role required: it\_demand\_manager

## Procedure

1.  Open a demand from the home page of Next Experience for Demand Management.

    For more information, see [Access demands](access-demand-workspace.md).

2.  Select **Details** from the L-2 \(level 2\) navigation menu.

3.  Select the **Resource assignments** tab.

    **Note:** If the required **Resource assignments** tab isn’t visible, select **More** and then select the required **Resource assignments** tab.

4.  Select the resource assignment record that you want to recalculate the costs for.

5.  Select the More Actions option and select **Recalculate Resource Cost**.![Use the Recalculate Resource Cost button to recalculate the costs of a resource.](../images/recalculate-resource-cost-button.png)

6.  On the Recalculate Resource Cost form, fill in the fields.

<table id="table_dht_bbx_j3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start date

</td><td>

Start date of the time period for which the costs are recalculated.By default, the field shows the current date.

</td></tr><tr><td>

End date

</td><td>

End date of the time period for which the costs are recalculated.By default, the field shows the due date of the demand. If the due date isn’t specified for the demand, the field is empty.

</td></tr></tbody>
</table>7.  Select **OK**.

    **Note:** Alternatively, you can recalculate the resource costs using the **Estimate resource requirements** playbook activity. For more information, see [Use Playbooks](use-playbooks-in-dw.md).


## Result

-   Recalculates the selected resource costs of all the applicable resource assignments in the demand based on the latest hourly rates. The hourly rates are derived from the rate model associated with the demand.
-   Updates the recalculated resource costs on the respective cost fields on the resource assignment form and the **Resource assignments** tab.
-   Reflects the revised values in the respective cost fields of the demand.

**Related topics**  


[Use Playbooks](use-playbooks-in-dw.md)

[Demand default playbook stages and activities](../reference/demand-default-playbook-stages.md)

[Create resource assignment form](../reference/create-resource-assignment-form-dw.md)

