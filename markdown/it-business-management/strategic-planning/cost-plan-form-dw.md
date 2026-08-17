---
title: Cost plan form
description: The cost plan form enables you to create a cost plan for a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/cost-plan-form-dw.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [cost plan]
breadcrumb: [Forms, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Cost plan form

The cost plan form enables you to create a cost plan for a demand.

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

Demand associated with the cost plan. This field is automatically set to the associated demand.

</td></tr><tr><td>

Start fiscal period

</td><td>

Starting fiscal period for the cost plan.When you change the start fiscal period, the associated cost breakdown values also change.

</td></tr><tr><td>

End fiscal period

</td><td>

Ending fiscal period for the cost plan.When you change the end fiscal period, the associated cost breakdown values also change.

</td></tr></tbody>
</table><table id="table_ibz_kkp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered currency

</td><td>

Currency to capture the unit cost value.

</td></tr><tr><td>

Total planned cost

</td><td>

Total planned cost value of the cost plan. -   If the cost is recurring: Quantity × Unit cost × number of fiscal periods.
-   If the cost is non-recurring: Quantity × Unit cost.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of single unit of the resource.

</td></tr><tr><td>

Functional currency

</td><td>

Currency used for managing the demand.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of units of resources.

</td></tr><tr><td>

Cost in functional currency

</td><td>

Total planned cost for the demand in functional currency.The value in this field changes if the entered currency is different from the functional currency.

</td></tr><tr><td>

Recurring

</td><td>

Indicates whether the cost is recurring for each fiscal period.

</td></tr><tr><td>

Total actual cost

</td><td>

Total actual cost of the cost plan. Value rolled up from cost breakdown.

</td></tr><tr><td>

Cost type

</td><td>

Category of cost associated with the plan.

</td></tr><tr><td>

Source

</td><td>

Funding entity funds.The field is available when you select a value in the **Source type** field.

**Note:** This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Investment

</td><td>

Name of the investment created for the demand.**Note:** This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source type

</td><td>

Funding entity type from which you request fund such as Project, Demand, and Epic. **Note:** This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr></tbody>
</table>