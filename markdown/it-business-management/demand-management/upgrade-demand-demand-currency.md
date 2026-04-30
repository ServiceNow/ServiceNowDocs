---
title: Upgrade existing demands
description: Execute scheduled jobs to upgrade your existing active and inactive demands, respectively, after activating the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.
locale: en-US
release: yokohama
product: Demand Management
classification: demand-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Upgrade existing demands

Execute scheduled jobs to upgrade your existing active and inactive demands, respectively, after activating the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

## Before you begin

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Role required: admin

## About this task

Run these scheduled jobs on demand to upgrade your existing active and inactive demands in demand currency only when necessary.

**Note:** The jobs may have performance impact depending on the number of demands and cost plans, hence run the jobs only when necessary.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Execute a scheduled job to upgrade your existing active and inactive demands.

<table id="choicetable_ndl_hwg_2nb"><thead><tr><th align="left" id="d298099e82">

Demand type

</th><th align="left" id="d298099e85">

Steps

</th></tr></thead><tbody><tr><td id="d298099e91">

**Active demands**

</td><td>

1.  Find the **Upgrade demand currency fields for active demands** scheduled job and open.
2.  Click **Execute Now**
 Executing the job copies all amounts in the cost-related fields of the demands in demand currency. The Baseline, Cost Plan, Cost Plan Breakdown, Benefit Plan, Benefit Plan Breakdown fields are also changed to the demand currency. You cannot edit the demand currency after the values in the functional currency fields are copied to the demand currency fields since the financial costs exist.

</td></tr><tr><td id="d298099e117">

**Inactive demands**

</td><td>

1.  Find the **Upgrade demand currency fields for inactive demands** scheduled job and open.
2.  Click **Execute Now**.
 Executing the job copies the values in the cost-related fields for all existing inactive demands to the demand currency. The currency in the Baselines, Cost Plans, Cost Plan Breakdowns, Benefit Plans, Benefit Plan Breakdowns, Expense Lines forms changes to demand currency.

</td></tr></tbody>
</table>
**Parent Topic:**[Multicurrency in Demand Management](../concept/multicurrency-demand.md)

