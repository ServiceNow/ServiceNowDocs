---
title: Multicurrency fields in demand-related forms
description: When you enable the Demand Currency view in Demand, Cost Plan, and Cost Plan Breakdown forms, multicurrency fields appear in the Financials section of these forms.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-02-04"
reading_time_minutes: 4
breadcrumb: [Multicurrency reference, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Multicurrency fields in demand-related forms

When you enable the **Demand Currency** view in Demand, Cost Plan, and Cost Plan Breakdown forms, multicurrency fields appear in the Financials section of these forms.

<table id="table_nzw_snf_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand. The available currency options depend on your selection in **Preferences-Project** under **Project Administration**. For more information, see [Select demand currency preference](../task/select-demand-currency-preference-dw.md).This field becomes read only once you create a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown.

</td></tr><tr><td>

Project currency

</td><td>

Currency for implementing the project when this demand is converted to a project. This value carries over to the Project form in Project Management.

</td></tr><tr><td>

Capital expense in demand currency

</td><td>

Capital expenditure \(Capex\) for the demand.

</td></tr><tr><td>

Capital budget in demand currency

</td><td>

Total capital budget allocated to the demand across all fiscal years. Rolled up from the Capex budget of the demand.

</td></tr><tr><td>

Operating expense in demand currency

</td><td>

Operational expenditure \(Opex\) for the demand in the selected demand currency.

</td></tr><tr><td>

Operating budget in demand currency

</td><td>

Total operational budget allocated to the demand across all fiscal years in the selected demand currency. Rolled up from the Opex budget of the demand.

</td></tr><tr><td>

Total planned cost in demand currency

</td><td>

Estimated cost of the demand in demand currency.

</td></tr><tr><td>

Financial return in demand currency

</td><td>

Estimated revenue based on the **Total planned costs in demand currency** and **Financial benefit in demand currency** fields.

</td></tr><tr><td>

Financial benefit in demand currency

</td><td>

Estimated revenue if the demand is approved in the selected demand currency. Rolled up from the benefit breakdown of the demand.

</td></tr><tr><td>

Net present value in demand currency

</td><td>

Present value of future cash based on the given annual interest rate in the selected demand currency. A measure for comparing money spent today against future expected financial benefits, helping evaluate overall investment performance.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Total cost incurred while working on a demand and demand tasks in the selected demand currency.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency** field of the Demand form.|
|Actual cost in demand currency|Total cost incurred while working on the demand tasks in the selected demand currency. Actual cost populates after the assignee creates and submits a time card. When the time card is approved, the resource rate from the rate card, labor rate, or system properties populates this field.|

## Financials section of the Cost Plan form

|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency**Demand currency field of the Demand form.|
|Cost in demand currency|Value that is rolled up from the **Entered cost** field of all cost plan breakdowns.|

**Note:** Any change to the unit cost, quantity, or fiscal period of a cost plan recalculates the amounts in demand currency. See [Cost plan updates and cost recalculation in demand currency](cost-plan-recalculation-in-dw.md).

|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency** field of the Demand form.|
|Cost in demand currency|Breakdown amount in demand currency.|
|Demand currency exchange rate|Rate in effect for the period corresponding to the cost plan breakdown in the demand currency.|
|Demand currency exchange rate date|Reference date on which the currency exchange rate is applied for conversion.|

|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency** field of the Demand form.|
|Benefit in demand currency|Benefit incurred from demand in demand currency.|
|Actual benefit in demand currency|Actual benefit value rolled up from the actual benefit in the benefit breakdown.|

|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency** field of the Demand form.|
|Benefit in demand currency|Benefit incurred from demand in demand currency.|
|Demand currency exchange rate|Rate in effect for the period corresponding to the benefit plan breakdown in demand currency.|
|Demand currency exchange rate date|Reference date on which the currency exchange rate is applied for conversion.|

|Field|Description|
|-----|-----------|
|Demand currency|Currency specified in the **Demand currency** field of the Demand form.|
|Amount in demand currency|Expense cost in demand currency. Amount entered in the Amount field is converted to demand currency.|

|Field|Description|
|-----|-----------|
|Capex budget in Demand Currency|Planned expense amount allocated for capital expenditure in the selected currency.|
|Opex budget in Demand Currency|Operating expense amount in the selected currency.|
|Total Budget in Demand Currency|Sum of Capex and Opex amounts in the selected currency.|

