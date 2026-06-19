---
title: Upgrade existing demands
description: Execute scheduled jobs to upgrade your existing active and inactive demands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-planning/upgrade-existing-demands-in-dw.html
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multicurrency in demands, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Upgrade existing demands

Execute scheduled jobs to upgrade your existing active and inactive demands.

## Before you begin

The PPM Standard Multicurrency feature must have been installed. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/ppm-collaboration/t_ActivateProjectPortfolioSuiteWithFinancials.md).

Role required: admin

## About this task

**Note:** Because these jobs can impact performance depending on the number of demands and cost plans, run the jobs only when necessary.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Search for and select the appropriate scheduled job for your demands.

    -   For active demands: **Upgrade demand currency fields for active demands**

        The job copies all amounts in the cost-related fields of the demands to demand currency. The Baseline, Cost Plan, Cost Plan Breakdown, Benefit Plan, and Benefit Plan Breakdown fields also change to the demand currency. You cannot edit the demand currency after the values are copied because the financial costs exist.

    -   For inactive demands: **Upgrade demand currency fields for inactive demands**

        The job copies the values in the cost-related fields for inactive demands to the demand currency. The currency in the Baselines, Cost Plans, Cost Plan Breakdowns, Benefit Plans, Benefit Plan Breakdowns, and Expense Lines forms changes to the demand currency.

3.  Select **Execute Now**.


