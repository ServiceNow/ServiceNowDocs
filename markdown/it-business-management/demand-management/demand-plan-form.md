---
title: Cost plan form
description: Use the cost plan form to capture the costs of demands.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Demand Management forms, Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost plan form

Use the cost plan form to capture the costs of demands.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for the cost plan.

</td></tr><tr><td>

Project/Demand

</td><td>

Demand number to which the cost plan belongs.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period.When you change the start fiscal period, the associated cost breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period.When you change the end fiscal period, the associated cost breakdown values also change.

</td></tr><tr><td>

Group

</td><td>

This field is a read-only field.

</td></tr></tbody>
</table><table id="table_f5j_sl3_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered currency

</td><td>

Currency for the cost plan.If the selected currency is different from the default currency configured in the Financial Management application, the [budget reference rate](../../project-management/concept/c_BudgetReferenceRates.md) is used to calculate the cost of the demand.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of single unit of the resource.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of resource required.

</td></tr><tr><td>

Recurring

</td><td>

Indicates if the cost is recurring for each fiscal period. **Quantity** x **Unit cost** value is incurred for every fiscal period.

</td></tr><tr><td>

Cost type

</td><td>

Cost type of the plan. See [Create a cost type definition](../../project-management/task/t_CreateAResourceTypeDefinition.md).

</td></tr><tr><td>

Investment

</td><td>

Name of the investment created for the project. This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source type

</td><td>

Funding entity to associated with the project investment for funding. This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source

</td><td>

Funding entity value from which you request fund.The field is available when you select a value in the Source type field.

This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Total planned cost

</td><td>

Total planned costs of the cost plan. If the cost is recurring, the calculation is **Quantity** x **Unit cost** x **number of fiscal periods**.If the cost is non-recurring, the calculation is **Quantity** x **Unit cost**.

This value is rolled up from cost breakdown.

</td></tr><tr><td>

Functional currency

</td><td>

The default currency configured in the Financial Management application and used for managing the demand or project.

</td></tr><tr><td>

Cost in functional currency

</td><td>

The total planned cost for the demand in functional currency. The value in this field changes if the **Entered currency** is different from the functional currency.

</td></tr><tr><td>

Total actual cost

</td><td>

Total actual costs of the cost plan. This value is rolled up from cost breakdown.

</td></tr></tbody>
</table>**Parent Topic:**[Demand Management forms](../concept/demand-management-forms.md)

