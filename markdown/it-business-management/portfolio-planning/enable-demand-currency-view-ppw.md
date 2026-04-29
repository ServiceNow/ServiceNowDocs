---
title: Enable demand currency view
description: Switch to the demand currency view to track the planned costs of a demand in the selected currency.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multicurrency, Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Enable demand currency view

Switch to the demand currency view to track the planned costs of a demand in the selected currency.

## Before you begin

Activate the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin.

Role required: admin or it\_demand\_manager

## About this task

To manage demands in a currency different from the functional currency, demand currency fields are added to the demand tables such as dmn\_demand and dmn\_demand\_task.

|Table|Description|
|-----|-----------|
|Demand \[dmn\_demand\]|Demands can be tracked in a different currency. When you create a demand, select another currency by navigating to the **Financials** tab and selecting a currency in the **Demand Currency** field.|
|Demand Task \[dmn\_demand\_task\]|Demand tasks delegate cost, effort, risk, and benefit assessment activities.|
|Cost Plans \[cost\_plan\]|Cost plans capture the costs of demands.|
|Cost Plan Breakdown \[cost\_plan\_breakdown\]|Cost plan breakdowns specify the estimated cost and actual cost at a granular level for a fiscal period.|
|Benefit Plan \[benefit\_plan\]|When you open the demand form in Demand Currency view, fields related to the demand currency appear in the Benefit Plans related list by default.|
|Benefit Plan Breakdowns \[benefit\_plan\_breakdown\]|Benefit plans capture the potential benefits accrued when the demand is executed.|
|Expense Line \[fm\_expense\_line\]|Expense lines are part of demand cost plans and store costs associated with a specific resource.|
|Project Funding \[project\_funding\]|Stores the demand target and budget expense values for both capital and operating expenses for a single fiscal period.|

## Procedure

1.  Navigate to the form in which you want to enable the demand currency view.

2.  Right-click the form header or select the additional actions icon to open the context menu.

3.  Select **View**.

4.  Select **Demand Currency** from the list.


## What to do next

Review the form fields exclusive to the **Demand Currency** view. All other form tabs and fields remain the same in both default view and demand currency view. Continue entering values as you would in the default view. For more information, see [Multicurrency fields in demand-related forms](../reference/multicurrency-fields-in-demand-related-forms-ppw.md).

