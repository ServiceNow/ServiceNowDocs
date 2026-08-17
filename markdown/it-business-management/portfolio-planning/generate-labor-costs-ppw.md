---
title: Generate labor costs for a demand
description: Generate labor costs to view the expenses of resources using resource assignments and cost plans for a demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/generate-labor-costs-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage financials for demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Generate labor costs for a demand

Generate labor costs to view the expenses of resources using resource assignments and cost plans for a demand.

## Before you begin

Role required: it\_demand\_manager

## About this task

When the effort distribution for a resource assignment changes without changing the total planned effort, labor costs are recalculated automatically. The recalculated costs align with the updated effort distribution. For example, consider a resource assignment of 100 hours: 60 hours in January and 40 hours in February. If you swap the efforts to 40 hours in January and 60 hours in February, labor costs are recalculated automatically. January then reflects the cost of 40 hours and February reflects the cost of 60 hours.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select **Financials** from the navigation menu.

5.  Select **Generate labor costs**.

6.  Select **Generate** in the Generate labor costs confirmation window.

    **Tip:** Configure a scheduled job to generate labor costs at the required cadence. For more information, see [Activate a scheduled job to generate labor costs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/gen-labor-costs-scheduled-job-ppm.md).


