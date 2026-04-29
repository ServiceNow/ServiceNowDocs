---
title: Generate labor costs
description: Generate labor costs in the Financials view for attribute-based resource assignments based on the financial attributes configured in the planning attributes page.
locale: en-US
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage financials for planning items, Portfolio Planning, Strategic Portfolio Management]
---

# Generate labor costs

Generate labor costs in the Financials view for attribute-based resource assignments based on the financial attributes configured in the planning attributes page.

## Before you begin

When the distribution of effort for a resource assignment is adjusted without changing the total planned effort, the system automatically recalculates and generates labor costs to align with the updated effort distribution. For example, consider a resource assignment of 100 hours distributed as 60 hours in January and 40 hours in February; now if you swap the efforts to make 40 hours in January and 60 hours in February. Now the system automatically adjusts the labor costs so that January reflects the cost of 40 hours and February reflects the cost of 60 hours, ensuring that costs accurately correspond to the revised effort distribution.

Role required: sn\_align\_ws.spw\_financial\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** and select a planning item.

2.  Select the **Financials** tab.

3.  Select **Generate labor costs** \(![Generate labor costs button.](../../spw-financials/images/financials-gen-labor-costs.png)\).

4.  Select **Generate** on the Generate labor costs confirmation window.

    **Note:** Alternatively, you can [activate a scheduled job](../../spw-financials/task/labor-cost-scheduler-job-spw.md) to automatically create baselines at the required cadence.


