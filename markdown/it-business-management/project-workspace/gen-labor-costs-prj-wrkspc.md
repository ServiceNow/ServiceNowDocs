---
title: Generate labor costs
description: Generate labor costs for projects and sub-projects based on the attribute-based resource assignments and the financial attributes configured in the planning attributes page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/project-workspace/gen-labor-costs-prj-wrkspc.html
release: zurich
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage financials, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Generate labor costs

Generate labor costs for projects and sub-projects based on the attribute-based resource assignments and the financial attributes configured in the planning attributes page.

## Before you begin

When the distribution of effort for a resource assignment is adjusted without changing the total planned effort, the system automatically recalculates and generates labor costs to align with the updated effort distribution. For example, consider a resource assignment of 100 hours distributed as 60 hours in January and 40 hours in February; now if you swap the efforts to make 40 hours in January and 60 hours in February. Now the system automatically adjusts the labor costs so that January reflects the cost of 40 hours and February reflects the cost of 60 hours, ensuring that costs accurately correspond to the revised effort distribution.

Role required: it\_project\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  Select **Financials** from the left menu.

3.  Select **Generate labor costs** \(\[Omitted image "financials-gen-labor-costs.png"\] Alt text: Generate labor costs button.\).

4.  Select **Generate** on the Generate labor costs confirmation window.

    **Note:** Alternatively, you can [activate a scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/labor-cost-scheduler-job-spw.md) to automatically create baselines at the required cadence.


**Parent Topic:**[Managing financials for your projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/using-financials-prj-wrkspc.md)

