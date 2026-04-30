---
title: Track project budget in project currency
description: Allocate budget to a project and enter amounts for capital expense budget \(Capex\) and operating expense \(Opex\) budget in project currency. The sum of the Capex and Opex budgets are calculated as total budget in project currency.
locale: en-US
release: zurich
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Track project budget in project currency

Allocate budget to a project and enter amounts for capital expense budget \(Capex\) and operating expense \(Opex\) budget in project currency. The sum of the Capex and Opex budgets are calculated as total budget in project currency.

## Before you begin

Role required: it\_portfolio\_manager

## About this task

Allocate budget in a similar manner as you do with functional currency. For more information, see [Allocate budget to a project](../../project-management/task/allocate-budget-to-project.md).

Enable the project currency view of the Project form to allocate budget in project.

## Procedure

1.  Click the Project Budget related link of the Project form.

<table id="table_h2y_3lb_1kb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Currency

</td><td>

Currency in which budget is allocated for a project.If you activate multicurrency plugin, then you have the option to budget in project currency or functional currency.

</td></tr><tr><td>

Capex Budget in Project Currency

</td><td>

Planned expense amount allocated for capital expenditure in the selected currency.

</td></tr><tr><td>

Opex Budget in Project Currency

</td><td>

Operating expense amount in the selected currency.

</td></tr><tr><td>

Total Budget in Project Currency

</td><td>

Sum of Capex and Opex amounts.The total project funding budget amount rolls up to the **Budget cost in project currency field**.

</td></tr></tbody>
</table>2.  Click **OK**.

3.  Click the Project Budget related list to update or view the record.


## What to do next

The project target and budget expense values for both capital and operating expenses for a single fiscal period is stored in the [Project Funding \[project\_funding\] table](../reference/multicurrency-fields-project-form.md#project_funding_project_curr). When you update the project funding record, the amounts are converted to project currency.

