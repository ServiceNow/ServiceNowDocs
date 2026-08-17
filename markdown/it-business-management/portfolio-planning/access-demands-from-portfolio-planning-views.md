---
title: Access execution records from Portfolio Plans
description: After creating a planning item demand in a Portfolio Plan, access the corresponding execution demand record directly from the Prioritization, Kanban, or Roadmap view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/access-demands-from-portfolio-planning-views.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 1
keywords: [access, demand, Kanban, roadmap, Portfolio Planning]
breadcrumb: [Prioritize portfolio plan work, Portfolio Planning, Strategic Portfolio Management]
---

# Access execution records from Portfolio Plans

After creating a planning item demand in a Portfolio Plan, access the corresponding execution demand record directly from the Prioritization, Kanban, or Roadmap view.

## Before you begin

Role required: apw\_user, ap\_read\_only

## About this task

An execution record is created in the Demands module for each planning item demand, using alignment integration. For more information, see [Configuring Portfolio Planning with PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/configuring-portfolio-planning-with-ppm.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  Open an execution demand from the Prioritization, Kanban, or Roadmap view.

<table id="choicetable_access_demands_ppw"><thead><tr><th align="left" id="d76531e124">

View

</th><th align="left" id="d76531e127">

Action

</th></tr></thead><tbody><tr><td id="d76531e133">

**Prioritization**

</td><td>

1.  Select the row context menu of a planning item of type demand.
2.  Select **Open demand**.

\[Omitted image "ppw-open-demand.png"\] Alt text: Row context menu with the Open demand option.

</td></tr><tr><td id="d76531e161">

**Kanban**

</td><td>

1.  Select the Actions menu of a planning item demand card.
2.  Select **Open demand**.

\[Omitted image "demand-kanban-ppw.png"\] Alt text: Actions menu with the Open demand option.

</td></tr><tr><td id="d76531e189">

**Roadmap view**

</td><td>

1.  Select a demand planning item from the roadmap.
2.  Select the execution URL from the side panel.


</td></tr></tbody>
</table>    The execution demand is opened in the **Demands** module.

    \[Omitted image "demand-from-portfolio-plan.png"\] Alt text: A demand in the Demands module opened from a portfolio plan.


