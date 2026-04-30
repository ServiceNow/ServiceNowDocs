---
title: Create cost plan form
description: The cost plan form information is used to create a cost plan for a demand.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-01-19"
reading_time_minutes: 1
breadcrumb: [Form field information, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create cost plan form

The cost plan form information is used to create a cost plan for a demand.

<table id="table_m2l_pjp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost plan.

</td></tr><tr><td>

Project/Demand

</td><td>

The demand to which this cost plan belongs.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting month in a fiscal period for the cost plan.When you change the start fiscal period, the associated cost breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending month in a fiscal period for the cost plan.When you change the end fiscal period, the associated cost breakdown values also change.

</td></tr></tbody>
</table><table id="table_ibz_kkp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered currency

</td><td>

Currency to capture the unit cost value.If the selected currency is different from the default currency configured in the Financial Management application, the budget reference rate is used to calculate the cost of the demand.

</td></tr><tr><td>

Total planned cost

</td><td>

Total planned cost value of the cost plan. If the cost is recurring, the calculation is Quantity x Unit cost x number of fiscal periods. If the cost is non-recurring, the calculation is Quantity x Unit cost.

This value is rolled up from the cost breakdown.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of single unit of the resource.

</td></tr><tr><td>

Functional currency

</td><td>

The default currency configured in the Financial Management application and used for managing the demand.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of cost plans.

</td></tr><tr><td>

Cost in functional currency

</td><td>

The total planned cost for the demand in functional currency. The value in this field changes if the entered currency is different from the functional currency.

</td></tr><tr><td>

Recurring

</td><td>

Indicates if the cost is recurring for each fiscal period. Quantity x Unit cost value is incurred for every fiscal period.

</td></tr><tr><td>

Total actual cost

</td><td>

Total actual costs of the cost plan. This value is rolled up from cost breakdown.

</td></tr><tr><td>

Cost type

</td><td>

Cost type of the plan.

</td></tr><tr><td>

Source

</td><td>

Funding entity value from which you request fund.The field is available when you select a value in the Source type field.

This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Investment

</td><td>

Name of the investment created for the project.This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source type

</td><td>

Funding entity type from which you request fund.This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr></tbody>
</table>