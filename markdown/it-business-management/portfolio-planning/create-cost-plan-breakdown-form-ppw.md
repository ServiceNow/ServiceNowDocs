---
title: Create cost plan breakdown form
description: The cost plan breakdown form information is used to create and edit a cost plan breakdown record for a cost plan of a demand.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Form field information, Reference, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Create cost plan breakdown form

The cost plan breakdown form information is used to create and edit a cost plan breakdown record for a cost plan of a demand.

<table id="table_ibz_kkp_c3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cost plan

</td><td>

Name of the cost plan to which the breakdown is associated.

</td></tr><tr><td>

Fiscal period

</td><td>

Fiscal period for the cost plan breakdown.

</td></tr><tr><td>

Entered currency

</td><td>

Currency to capture the unit cost value.If the selected currency is different from the default currency configured in the Financial Management application, the budget reference rate is used to calculate the cost of the demand.

</td></tr><tr><td>

Entered cost

</td><td>

Breakdown amount in entered currency.

</td></tr><tr><td>

Task

</td><td>

Task to which the cost plan breakdown belongs.

</td></tr><tr><td>

Functional cost

</td><td>

Functional cost obtained by multiplying exchange rate with entered cost.

</td></tr><tr><td>

Exchange rate

</td><td>

Rate in effect for the period corresponding to the cost plan breakdown. When the period corresponding to the cost plan break down has multiple rates, the rate in effect on the first date of that period is used. Exchange rate is used to convert entered cost into functional cost. It is obtained from the itfm\_fx\_rate \[budget\_reference\_rates\] table.

</td></tr><tr><td>

Exchange rate date

</td><td>

First date of the fiscal period corresponding to the cost plan breakdown.

</td></tr></tbody>
</table>