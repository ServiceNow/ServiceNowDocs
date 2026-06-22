---
title: Prioritize work
description: Review and prioritize the items of your portfolio plan pipeline to add them to the plan's roadmap so that your teams can start working on them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/scenario-planning-in-spw/prioritize-planning-items-strategic-planning-workspace.html
release: zurich
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [alignment planner workspace, portfolio planning workspace, portfolio planner, strategic planner, strategic planning workspace]
breadcrumb: [Prioritize portfolio plan work, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Prioritize work

Review and prioritize the items of your portfolio plan pipeline to add them to the plan's roadmap so that your teams can start working on them.

## Before you begin

-   [Create a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/scenario-planning-in-spw/create-portfolio-plans-in-alignment-planner-workspace.md).
-   Ensure that the planning items in the Prioritization tab are sorted by the Rank column in ascending order.

Role required: sn\_align\_core.apw\_user

## About this task

Review and prioritize the items in the Prioritization, Kanban, or Hierarchy tab during your grooming sessions. You can use the MoSCoW values assigned to an item to help you decide the priority of work.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Strategic Planning Workspace** &gt; **Portfolio Planning**.

2.  From the list of portfolio plans, select one and then select **Planning**.

3.  From the Prioritization tab or any other tab, mark a planning item as In Review or Prioritized.

<table id="choicetable_knp_gs5_dwb"><thead><tr><th align="left" id="d76815e132">

Tab

</th><th align="left" id="d76815e135">

Action

</th></tr></thead><tbody><tr><td id="d76815e141">

**Prioritization**

</td><td>

Update the **Planning state** field of the item.

 \[Omitted image "backlog-planning-state.png"\] Alt text: Planning state update in Prioritization page.

</td></tr><tr><td id="d76815e163">

**Kanban**

</td><td>

Move the item card into the **Prioritized** lane.

 \[Omitted image "kanban-prioritize-item.png"\] Alt text: Prioritize item in kanban view

</td></tr><tr><td id="d76815e185">

**Hierarchy**

</td><td>

Update the **Planning state** field of the item.

 \[Omitted image "prioritize-item-hierarchy.png"\] Alt text: Planning state in Prioritization.

 For a high-level portfolio plan, you can’t edit the Planning state inline. Select the short description of the item to open its Full details page and then update the item's Planning item.

</td></tr></tbody>
</table>    After you mark a planning item as **Prioritized**, it’s automatically added to your portfolio roadmap, based on the values in the **Approved start date** and **Approved end date** fields. Your roadmap shows only those items that have their Planning state set to **Prioritized**.

    -   If the dates fall within the portfolio planning period, then the item is displayed on the roadmap.
    -   If either of the date fields is empty, then the item is added to the Unscheduled items list of the roadmap.
    If you've marked an item as **Done** or **Cancelled**, that item isn’t displayed on the Prioritization page by default. You can update the filter on the Planning state column to show the items that are completed or canceled.

4.  From the Prioritization tab, you can update the planning state of multiple items at once.

    1.  Select the **Planning state** cell of one of the rows that you want to update.

    2.  Press and hold the **Ctrl** key \(for Windows OS\) or **command** key \(for Mac OS\), and select the **Planning state** cells of the other rows that you want to update.

    3.  Double-click one of the selected cells and choose a state.

    \[Omitted image "backlog-multi-row-update.gif"\] Alt text: Update planning state of multiple rows at once in Prioritization page.


