---
title: Cost Plan form
description: Learn about the fields of cost plan form.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Cost Plan form

Learn about the fields of cost plan form.

<table id="table_mb3_rfw_1r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name of the cost plan.

</td></tr><tr><td>

Project/Demand

</td><td>

Project or demand to which the cost plan belongs.

</td></tr><tr><td>

Start fiscal period

</td><td>

Indicates the starting fiscal period.When you change the start fiscal period, the associated cost plan breakdowns also change. Start fiscal period also changes when you create cost plan breakdowns earlier than the start fiscal period.

</td></tr><tr><td>

End fiscal period

</td><td>

Indicates the ending fiscal period.When you change the end fiscal period, the associated cost plan breakdowns also change. End fiscal period also changes when you create cost plan breakdowns later than the end fiscal period.

</td></tr></tbody>
</table><table id="table_uq5_1pz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entered currency

</td><td>

Currency in which you want the cost plan to be created. If the selected currency is different from the functional currency, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the total planned cost, planned capital, planned operating of the project.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of a single unit of the resource, which is in terms of entered currency.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of the resource that is required.

</td></tr><tr><td>

Recurring

</td><td>

Option to indicate that the cost is recurring for each fiscal period. **Quantity** x **Unit cost** incurred for every fiscal period.

</td></tr><tr><td>

Cost type

</td><td>

[Cost type definition](../task/t_CreateAResourceTypeDefinition.md).

</td></tr><tr><td>

Investment

</td><td>

Name of the investment created for the project.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source type

</td><td>

Funding entity to associated with the project investment for funding.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Source

</td><td>

Funding entity value from which you request fund.

 The field is available when you select a value in the **Source type** field.

 This field appears only if the legacy Investment Funding \(com.snc.investment\_funding\) plugin is activated or the Investment Funding \(sn\_invst\_pln\) application is installed.

</td></tr><tr><td>

Total planned cost

</td><td>

Total estimated cost of the cost plan. If the cost is recurring, the calculation is **Quantity** x **Unit cost** x **number of fiscal periods**. If the cost is non-recurring, the calculation is **Quantity** x **Unit cost**.

</td></tr><tr><td>

Functional currency

</td><td>

Currency that is obtained from the [**glide.system.locale** property](https://www.servicenow.com/docs/access?context=currency-properties&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).For upgraded customers, if the selected currency is different from the functional currency configured in the Financial Management application, the corresponding [budget reference rate](../concept/c_BudgetReferenceRates.md) is used to calculate the total planned cost, planned capital, planned operating of the project.

 **Note:** If budget reference rates are not defined, then exchange rate is considered as 1. For example, if functional currency is USD, entered cost is EUR, and no exchange rate is defined, then 1000 USD equals to 1000 EUR.

</td></tr><tr><td>

Cost in functional currency

</td><td>

Value that is rolled up from the **Functional cost** field of all cost plan breakdowns.

</td></tr><tr><td>

Total actual cost

</td><td>

Value that is rolled up from the **Actual cost** field of all cost plan breakdowns.

</td></tr><tr><td>

Estimate at Completion

</td><td>

Sum of all actuals for past fiscal periods added to the functional cost for future fiscal periods.For example, the duration of a project is from January 01 to December 31, and if you check the Estimate at Completion in the month of May, it is calculated as: `Sum of actuals from Jan to April + Sum of functional cost from May to December`.

</td></tr></tbody>
</table>**Related topics**  


[Create a project cost plan](../task/t_CreateAProjectCostPlan.md)

