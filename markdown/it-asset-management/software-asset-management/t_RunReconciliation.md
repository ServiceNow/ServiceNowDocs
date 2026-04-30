---
title: Run software reconciliation
description: Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in your environment on demand.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Software license usage, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Run software reconciliation

Reconciliation is run as a scheduled job \(default is weekly\), but you can also run reconciliation manually to reconcile software products in your environment on demand.

## Before you begin

Role required: sam\_admin

## About this task

Reconciliation is run for products that have software entitlements or software installs. Grouping and subgrouping are supported so you can narrow the compliance results.

When running reconciliation manually, allow enough time for the process to complete. For faster results, narrow the scope by selecting specific publishers.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Run Reconciliation** and select the publishers for which compliance should be calculated, or select all publishers.

2.  To narrow results further, select **Group** and **Subgroup**, if desired.

    Available group and subgroup values include None, Country, Department, Company, Region, and Cost Center.

3.  Select **Continue**.

    The reconciliation process may take an extended amount of time to complete. Once reconciliation is complete, the reconciliation results are shown.


**Parent Topic:**[Software license usage](../concept/sam-license-workbench.md)

