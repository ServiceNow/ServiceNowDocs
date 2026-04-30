---
title: Components installed with Strategic Spend Tracking for PPM
description: Several types of components are installed with activation of Strategic Spend Tracking for PPM, including tables and scheduled jobs.
locale: en-US
release: zurich
product: PPM Collaboration
classification: ppm-collaboration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install Strategic Spend Tracking for PPM, Strategic spend tracking, Project Portfolio Management, Strategic Portfolio Management]
---

# Components installed with Strategic Spend Tracking for PPM

Several types of components are installed with activation of Strategic Spend Tracking for PPM, including tables and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Demo data is available for this feature.

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|PPM Strategic Spend Tracking - Generate Strategy/Goal Allocation Breakdowns for Projects and Demands|Generates breakdown of strategy and goal allocation for the associated projects and demands.|
|PPM Strategic Spend Tracking - Update projects and Demands with strategy and goal allocations|Updates strategy and goal allocations for the associated projects and demands.|

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BO Job Execution Log\[sn\_ppm\_sst\_run\_log\]

</td><td>

Stores information about execution of the scheduled jobs such as time of execution and tasks there were included.

</td></tr><tr><td>

Goal Allocation\[sn\_ppm\_sst\_task\_goal\]

</td><td>

Stores goal allocation details for a project or demand. The details include project or demand number, strategy name, % allocated towards the strategy, budget, planned cost, actual cost, and benefit amount.

</td></tr><tr><td>

Goal Allocation Breakdown\[sn\_ppm\_sst\_goal\_allocation\_breakdown\]

</td><td>

Stores goal breakdown details for a project or demand. The details include fiscal year, strategy allocation amount, cost details \(planned and actual\), and capex and opex amounts \(planned and actual\).

</td></tr><tr><td>

Strategy Allocation\[sn\_ppm\_sst\_task\_strategy\]

</td><td>

Stores strategy allocation details for a project or demand. The details include project or demand number, strategy name, % allocated towards the strategy, budget, planned cost, actual cost, and benefit amount.

</td></tr><tr><td>

Strategy Allocation Breakdown\[sn\_ppm\_sst\_strategy\_allocation\_breakdown\]

</td><td>

Stores strategy breakdown details for a project or demand. The details include fiscal year, strategy allocation amount, cost details \(planned and actual\), and capex and opex amounts \(planned and actual\).

</td></tr></tbody>
</table>**Parent Topic:**[Install Strategic Spend Tracking for PPM](../task/install-strategic-spend.md)

