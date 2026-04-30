---
title: Upgrade existing demands
description: Execute scheduled jobs to upgrade your existing active and inactive demands after activating the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.
locale: en-US
release: zurich
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-02-05"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Upgrade existing demands

Execute scheduled jobs to upgrade your existing active and inactive demands after activating the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

## Before you begin

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Role required: admin

## About this task

Run these scheduled jobs on demand to upgrade your existing active and inactive demands in demand currency only when necessary.

**Note:** The jobs can impact performance depending on the number of demands and cost plans. Run the jobs only when necessary.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Execute the appropriate scheduled job for your demands.

<table id="choicetable_ndl_hwg_2nb"><thead><tr><th align="left" id="d154641e86">

Demand type

</th><th align="left" id="d154641e89">

Steps

</th></tr></thead><tbody><tr><td id="d154641e95">

**Active demands**

</td><td>

1.  Find and the **Upgrade demand currency fields for active demands** scheduled job.
2.  Select **Execute Now**.
 The job copies all amounts in the cost-related fields of the demands to demand currency. The Baseline, Cost Plan, Cost Plan Breakdown, Benefit Plan, and Benefit Plan Breakdown fields also change to the demand currency. You can’t edit the demand currency after the values are copied because the financial costs exist.

</td></tr><tr><td id="d154641e122">

**Inactive demands**

</td><td>

1.  Find and open the **Upgrade demand currency fields for inactive demands** scheduled job.
2.  Select **Execute Now**.
 The job copies the values in the cost-related fields for inactive demands to the demand currency. The currency in the Baselines, Cost Plans, Cost Plan Breakdowns, Benefit Plans, Benefit Plan Breakdowns, and Expense Lines forms changes to the demand currency.

</td></tr></tbody>
</table>
