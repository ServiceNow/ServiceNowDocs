---
title: Multicurrency fields in demand forms
description: Multicurrency fields are available in the demand forms when the demand currency view is enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/demand-tables-with-demand-currency-fields.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Multicurrency reference, Reference, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Multicurrency fields in demand forms

Multicurrency fields are available in the demand forms when the demand currency view is enabled.

## Demand form

<table id="table_nzw_snf_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Capital expense in demand currency

</td><td>

Capital expenditure \(Capex\) value of the demand.

</td></tr><tr><td>

Capital budget in demand currency

</td><td>

Total capital budget value allocated to the demand across all fiscal years.

</td></tr><tr><td>

Operating expense in demand currency

</td><td>

Operational expenditure \(Opex\) value of the demand.

</td></tr><tr><td>

Operating budget in demand currency

</td><td>

Total operational budget value allocated to the demand across all fiscal years in the selected demand currency.

</td></tr><tr><td>

Total planned cost in demand currency

</td><td>

Estimated cost of the demand.

</td></tr><tr><td>

Financial return in demand currency

</td><td>

Estimated revenue of the demand.

</td></tr><tr><td>

Financial benefit in demand currency

</td><td>

Estimated revenue if the demand is approved.

</td></tr><tr><td>

Net present value in demand currency

</td><td>

Present value of future cash based on the annual interest rate.This field compares the money spent today against the financial benefits expected in the future. It enables evaluation of overall investment performance.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Total cost incurred while working on a demand and its demand tasks.

</td></tr></tbody>
</table>## Demand Task form

<table id="table_pj5_syf_dnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Actual cost in demand currency

</td><td>

Total cost incurred while working on a demand and its demand tasks.

</td></tr></tbody>
</table>## Cost Plan form

<table id="table_amq_p4f_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Cost in demand currency

</td><td>

Rolled-up value from the **Entered cost** field of all cost plan breakdowns.

</td></tr></tbody>
</table>## Cost Plan Breakdown form

<table id="table_ccf_cpf_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Cost in demand currency

</td><td>

Cost amount for the demand.

</td></tr><tr><td>

Demand currency exchange rate

</td><td>

Rate in effect for the period corresponding to the cost plan breakdown.

</td></tr><tr><td>

Demand currency exchange rate date

</td><td>

Reference date on which the currency exchange rate is applied for conversion.

</td></tr></tbody>
</table>## Benefit Plan form

<table id="table_xtl_xy5_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Benefit in demand currency

</td><td>

Benefit incurred from the demand.

</td></tr><tr><td>

Actual benefit in demand currency

</td><td>

Actual benefit value of the demand.

</td></tr></tbody>
</table>## Benefit Plan Breakdown form

<table id="table_rsj_jz5_jjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Benefit in demand currency

</td><td>

Benefit incurred from the demand.

</td></tr><tr><td>

Demand currency exchange rate

</td><td>

Rate in effect for the period corresponding to the benefit plan breakdown.

</td></tr><tr><td>

Demand currency exchange rate date

</td><td>

Reference date on which the currency exchange rate is applied for conversion.

</td></tr></tbody>
</table>## Expense Line form

<table id="table_mnc_x5j_kjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Demand currency

</td><td>

Currency for managing and tracking the demand.This field is set to read-only after a cost plan, cost plan breakdown, benefit plan, or benefit plan breakdown is created.

</td></tr><tr><td>

Amount in demand currency

</td><td>

Expense cost amount for the expense line.

</td></tr></tbody>
</table>## Project Funding form

|Field|Description|
|-----|-----------|
|Capex budget in demand currency|Planned expense amount allocated for the capital expenditure of the demand.|
|Opex budget in demand currency|Planned expense amount allocated for the operating expenditure of the demand.|
|Total budget in demand currency|Sum of the Capex and Opex amounts.|

