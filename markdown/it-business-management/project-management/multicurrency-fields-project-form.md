---
title: Multicurrency fields in project-related forms
description: When you enable the Project Currency view in Project, Cost Plan, and Cost Plan Breakdown forms, you can observe multicurrency fields in the Financials section of the forms.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Enable project currency view in project-related forms, Multicurrency in Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Multicurrency fields in project-related forms

When you enable the Project Currency view in Project, Cost Plan, and Cost Plan Breakdown forms, you can observe multicurrency fields in the Financials section of the forms.

## Financials tab of the Project form

<table id="table_nzw_snf_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project currency

</td><td>

Currency in which the project is to be implemented.**Note:**

The **Project currency** field defaults to the Functional Currency if you modify the currency field and save the Project form without selecting a currency.

The **Project currency** field of a project becomes read-only field and cannot be modified once you create a cost plan, cost plan breakdown, benefit plan, benefit plan breakdown, or an expense line for the project.

</td></tr><tr><td>

Total planned cost in project currency

</td><td>

Estimated cost of the project in project currency.

</td></tr><tr><td>

Planned capital in project currency

</td><td>

Capital expenditure \(Capex\) for the project.

</td></tr><tr><td>

Planned operating in project currency

</td><td>

Operational expenditure \(Opex\) for the project in project currency.

</td></tr><tr><td>

Budget cost in project currency

</td><td>

Budgeted cost in local currency for the project.

</td></tr><tr><td>

Actual cost in project currency

</td><td>

Actual cost of the project in local currency.

</td></tr><tr><td>

Estimate at completion in project currency

</td><td>

Sum of all actuals for past fiscal periods added to the functional cost for future fiscal periods in project currency.

</td></tr><tr><td>

Planned benefit in project currency

</td><td>

Planned benefit for the project in project currency.

</td></tr><tr><td>

Planned return in project currency

</td><td>

Difference between Planned benefit and Planned cost values.

</td></tr><tr><td>

Planned ROI %

</td><td>

Percentage calculated based on the values in the Planned return and Estimated cost fields.

</td></tr><tr><td>

Net present value in project currency

</td><td>

Present value of future cash in project currency based on the given annual interest rate.

</td></tr><tr><td>

Internal rate of return %

</td><td>

Annual interest rate required to achieve the net present value \(NPV\) of zero.

</td></tr><tr><td>

Estimate to completion in project currency

</td><td>

Sum of functional cost for all fiscal periods in project currency.

</td></tr></tbody>
</table><table id="table_n2c_ppz_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status report currency

</td><td>

Currency in which the project status report is generated.If you have the Project currency view enabled in the Project form, then you have the choice to generate the project status report using any of the following currency options:

 -   **Functional currency**: Currency obtained from the glide.system.locale property in which the project status report is created.
-   **Project currency**: Project status report is created in the local currency that is selected. If you select Project currency, you can view the planned cost and actual cost in the selected project currency.

 To view the status report of the project, see [View project status reports](../../project-management/task/project-status-report.md).

</td></tr></tbody>
</table>## Financials section of the Cost Plan form

|Field|Description|
|-----|-----------|
|Project currency|Currency in which you can create the cost plan.|
|Cost in project currency|Value that is rolled up from the Entered cost field of all cost plan breakdowns.|
|Total actual cost in project currency|Value that is rolled up from the **Actual cost** field of all cost plan breakdowns in project currency.|
|Estimate at completion in project currency|Sum of all actuals for past fiscal periods added to the functional cost for future fiscal periods in project currency.|
|Estimate to completion in project currency|Sum of functional cost for all fiscal periods in project currency.|

**Note:** Any change that you make to the unit cost, quantity, or fiscal period of a cost plan has the amounts recalculated in project currency. See [Updates in cost plan and recalculation of cost in project currency](../concept/change-cost-calculated-project-currency.md).

## Multicurrency fields in the Cost Plan Breakdown form

|Field|Description|
|-----|-----------|
|Exchange rate for project currency|Rate in effect for the period corresponding to the cost plan breakdown in project currency.|
|Project currency|Local currency selected for the cost plan breakdown.|
|Cost in project currency|Breakdown amount in project currency.|
|Actual cost in project currency|Actual cost generated from processed expense lines in project currency.|
|Variance project currency|Difference between Cost in project currency and Actual cost in project currency.|
|Budget|Project budget amount entered for a fiscal year gets distributed equally into monthly breakdowns in functional currency.|
|Budget cost in project currency|Project budget amount entered for a fiscal year gets distributed equally into monthly breakdowns in project currency.|

## Financials section of the Benefit Plan form

<table id="table_xtl_xy5_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Project currency

</td><td>

Project currency that was selected in the project is populated.Benefit plan attached to a project inherits the same currency as that of the project.

</td></tr><tr><td>

Benefit in project currency

</td><td>

Benefit incurred from project or demand in project currency.

</td></tr></tbody>
</table>## Multicurrency fields in the Benefit Plan Breakdowns form

|Field|Description|
|-----|-----------|
|Project currency|Currency that is selected in the Project form.|
|Benefit in project currency|Benefit incurred from project or demand in project currency.|
|Project currency exchange rate|Rate in effect for the period corresponding to the benefit plan breakdown in project currency.|
|Project currency reference rate|Rate at which the entered currency is exchanged for project currency.|

## Multicurrency fields in the Expense Line form

|Field|Description|
|-----|-----------|
|Project currency|Currency inherited from the project if the project has a related expense line.|
|Amount in project currency|Expense cost in project currency. Amount entered in the Amount field is converted to project currency.|

## Multicurrency fields in the Project Funding form

<table id="table_a3w_1mb_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capital budget in project currency

</td><td>

Planned expense amount allocated for capital expenditure in the selected currency.

</td></tr><tr><td>

Operating budget in project currency

</td><td>

Operating expense amount in the selected currency.

</td></tr><tr><td>

Budget in project currency

</td><td>

Sum of Capex and Opex amounts.The total project funding budget amount rolls up to the **Budget cost in project currency** field.

</td></tr><tr><td>

Project currency

</td><td>

Currency in which the project is funded.

</td></tr><tr><td>

Exchange rate

</td><td>

Currency conversion based on the exchange rates between currencies.

</td></tr><tr><td>

Exchange rate date

</td><td>

Date on which the exchange rate is applied.

</td></tr><tr><td>

Exchange reference date

</td><td>

Budget Reference Rate from where the exchange rate is retrieved.

</td></tr></tbody>
</table>