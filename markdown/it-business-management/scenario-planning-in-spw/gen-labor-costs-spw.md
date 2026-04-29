---
title: Generate labor costs
description: Generate labor costs for projects and sub-projects based on the attribute-based resource assignments and the financial attributes configured in the planning attributes page.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage financials for planning items, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Generate labor costs

Generate labor costs for projects and sub-projects based on the attribute-based resource assignments and the financial attributes configured in the planning attributes page.

## Before you begin

Role required: sn\_align\_ws.spw\_financial\_user

## About this task

When the distribution of effort for a resource assignment is adjusted without changing the total planned effort, the system automatically recalculates and generates labor costs to align with the updated effort distribution. For example, consider a resource assignment of 100 hours distributed as 60 hours in January and 40 hours in February; now if you swap the efforts to make 40 hours in January and 60 hours in February. Now the system automatically adjusts the labor costs so that January reflects the cost of 40 hours and February reflects the cost of 60 hours, ensuring that costs accurately correspond to the revised effort distribution.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** and select portfolio plan.

2.  Select a planning item from the Planning module.

3.  Select the **Financials** tab.

4.  Select **Generate labor costs** \(![Generate labor costs button.](../images/financials-gen-labor-costs.png)\).

5.  Select **Generate** on the Generate labor costs confirmation window.

    **Note:** Alternatively, you can activate a scheduled job to generate labor costs at the required cadence. For more information, see [Activate scheduled job to generate labor costs for your planning items](labor-cost-scheduler-job-spw.md).


