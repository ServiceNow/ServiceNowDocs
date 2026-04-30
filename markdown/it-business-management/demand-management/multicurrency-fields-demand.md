---
title: Multicurrency fields in demand-related forms
description: When you enable the Demand Currency view in a Demand, Cost Plan, and Cost Plan Breakdown forms, you can observe the multicurrency fields in the Financials section of the forms.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Enable demand currency view, Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Multicurrency fields in demand-related forms

When you enable the **Demand Currency** view in a Demand, Cost Plan, and Cost Plan Breakdown forms, you can observe the multicurrency fields in the Financials section of the forms.

## Financials tab of the demand form

<table id="table_nzw_snf_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency in which you want to manage and track the demand.**Note:**

The ability to select a demand currency depends on the currency option you selected in **Preferences-Project** under **Project Administration**. For more information, see [Select demand currency preference](../task/select-demand-currency.md).

The **Demand currency** field of a demand becomes read-only once you create a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown.

</td></tr><tr><td>

Project currency

</td><td>

Currency in which you want to implement the project when this demand is converted to a project.**Note:**

The **Project currency** field in the Project form of Project Management is carried over from the demand when it is converted.

</td></tr><tr><td>

Capital expense in demand currency

</td><td>

Capital expenditure \(Capex\) for the demand.

</td></tr><tr><td>

Capital budget in demand currency

</td><td>

Total capital budget allocated to the demand across all fiscal years.The value is rolled up from the capital expenditure \(Capex\) budget of the demand.

</td></tr><tr><td>

Operating expense in demand currency

</td><td>

Operational expenditure \(Opex\) for the demand in the selected demand currency.

</td></tr><tr><td>

Operating budget in demand currency

</td><td>

Total operational budget allocated to the demand across all fiscal years in the selected demand currency.The value is rolled up from the Opex budget of the demand.

</td></tr><tr><td>

Total planned cost in demand currency

</td><td>

Estimated cost of the demand in demand currency.

</td></tr><tr><td>

Financial return in demand currency

</td><td>

Estimate of the revenue based on the **Total planned costs in demand currency** and **Financial benefit in demand currency** fields.

</td></tr><tr><td>

Financial benefit in demand currency

</td><td>

Estimate of revenue if the demand is approved in the selected demand currency.This value is rolled up from the benefit breakdown of the demand.

</td></tr><tr><td>

Net present value in demand currency

</td><td>

Present value of future cash based on the given annual interest rate in the selected demand currency.It is a measure for comparing money spent today against future expected financial benefits. It helps when evaluating the overall investment performance.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Total cost incurred while working on a demand and demand tasks in the selected demand currency.

</td></tr></tbody>
</table>## Multicurrency fields of the Demand Task form

<table id="table_pj5_syf_dnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency that you specified in the **Demand currency** field of the Demand form.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Total cost incurred while working on a demand tasks in the selected demand currency. Actual cost comes after the assignee of the demand task creates and submits a time card. When the time card is approved, the resource rate, derived from the rate card, labor rate, or system properties, is used to populate this field.

</td></tr></tbody>
</table>## Financials section of the Cost Plan form

|Field|Description|
|-----|-----------|
|Demand currency|Currency that you specified in the **Demand currency** field of the Demand form.|
|Cost in demand currency|Value that is rolled up from the **Entered cost** field of all cost plan breakdowns.|

**Note:** Any change that you make to the unit cost, quantity, or fiscal period of a cost plan has the amounts recalculated in demand currency. See [Cost plan updates and cost recalculation in demand currency](../concept/cost-recalculation-demand-multicurrency.md).

## Multicurrency fields in the Cost Plan Breakdown form

|Field|Description|
|-----|-----------|
|Demand currency|Currency that you specified in the **Demand currency** field of the Demand form.|
|Cost in demand currency|Breakdown amount in demand currency.|
|Demand currency exchange rate|Rate in effect for the period corresponding to the cost plan breakdown in the demand currency.|
|Demand currency exchange rate date|The reference date on which the currency exchange rate is applied for conversion.|

## Financials section of the Benefit Plan form

|Field|Description|
|-----|-----------|
|Demand currency|Currency that you specified in the **Demand currency** field of the Demand form.|
|Benefit in demand currency|Benefit incurred from demand in demand currency.|
|Actual benefit in demand currency|Actual benefit value rolled up from the actual benefit in the benefit breakdown.|

## Multicurrency fields in the Benefit Plan Breakdowns form

|Field|Description|
|-----|-----------|
|Demand currency|Currency that you specified in the **Demand currency** field of the Demand form.|
|Benefit in demand currency|Benefit incurred from demand in demand currency.|
|Demand currency exchange rate|Rate in effect for the period corresponding to the benefit plan breakdown in demand currency.|
|Demand currency exchange rate date|The reference date on which the currency exchange rate is applied for conversion.|

## Multicurrency fields in the Expense Line form

|Field|Description|
|-----|-----------|
|Demand currency|Currency that you specified in the **Demand currency** field of the Demand form.|
|Amount in demand currency|Expense cost in demand currency. Amount entered in the Amount field is converted to demand currency.|

## Multicurrency fields in the Demand Budget form

|Field|Description|
|-----|-----------|
|Capex budget in Demand Currency|Planned expense amount allocated for capital expenditure in the selected currency.|
|Opex budget in Demand Currency|Operating expense amount in the selected currency in the selected currency.|
|Total Budget in Demand Currency|Sum of Capex and Opex amounts in the selected currency.|

**Parent Topic:**[Enable demand currency view](../task/enable-multicurrency-demand.md)

