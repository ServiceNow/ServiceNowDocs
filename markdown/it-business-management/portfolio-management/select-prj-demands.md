---
title: Select demands and projects for portfolio planning
description: After you create a planning scenario, select the demands and projects to include in budget planning. You can view all the demands and projects for the selected fiscal year or planning window with their planned cost and priorities to finalize them for execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-management/select-prj-demands.html
release: zurich
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Create planning scenarios, Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Select demands and projects for portfolio planning

After you create a planning scenario, select the demands and projects to include in budget planning. You can view all the demands and projects for the selected fiscal year or planning window with their planned cost and priorities to finalize them for execution.

## Before you begin

You should have at least one planning scenario. For more information, see [Create planning scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-management/create-scenarios.md).

Role required: it\_portfolio\_manager

## About this task

You can perform a what-if analysis by including or excluding demands or projects and their planned cost for annual type of planning. The planned cost is derived from all the cost plans created for a project or demand. It is the total of all the costs from all cost plans for a given project or demand in the fiscal year or planning window.

You can perform a what-if analysis by including or excluding demands or projects and their planned cost, budget, and utilization for multi-year resource capacity type of planning.

## Procedure

1.  Navigate to Portfolio Planning Workbench from either of two starting points.

<table id="choicetable_xfs_1fh_jlb"><thead><tr><th align="left" id="d142793e84">

Location

</th><th align="left" id="d142793e87">

Steps

</th></tr></thead><tbody><tr><td id="d142793e93">

**From application navigator**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Portfolios** &gt; **Portfolio Planning Workbench**.
2.  From the **Portfolio** choice list, select the portfolio that you want to perform the planning for.


</td></tr><tr><td id="d142793e129">

**From the portfolio list**

</td><td>

1.  Navigate to **All** &gt; **Project** &gt; **Portfolios** &gt; **All**.
2.  Open the portfolio that you want to perform the planning for.
3.  In the Portfolio form, click the **Portfolio Planning** related link.


</td></tr></tbody>
</table>2.  In the Portfolio Planning Workbench, click the scenario for which you want to include or exclude demands and projects.

    The projects and demands from the selected portfolio appear on the **Timeline View**.

3.  Compare and evaluate the relative standing of demands using the **Bubble Chart** tab.

    Right-click a demand and select **Select for execution** from the context menu to include a demand in portfolio planning. For more information, see [Demand workbench bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/c_DemandWorkbenchBubbleChart.md). You can search for specific demands by applying filters using the Filter\( \[Omitted image "filter-timeline-bubble.png"\] Alt text: Filter icon to filter for demands\) icon.

    **Note:** The **Bubble Chart** tab is not available for Multi-year Resource Capacity Based Planning configuration.

4.  Include or exclude demands and projects from planning in the **Timeline View** tab by selecting or clearing the check boxes next to each project or demand.

    You can search for specific demands and projects in the timeline by applying filters using the Filter\(\[Omitted image "filter-timeline-bubble.png"\] Alt text: Filter icon to filter for projects or demands\) icon.

    The number of selected project and demands is updated in the **Selected Items** section of the **Overview** tab.

5.  Review the external dependencies between the selected projects in your portfolio.

    For more information, see [Review external dependencies between projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-management/sp-review-ext-dependencies-between-prj.md).

6.  Review the information in the Overview section on the right, and the **Resources** tab to evaluate and adjust your selection of the demands and projects to be included in the plan.

    Review the following sections in the **Overview** tab:

    -   Total budget versus the targets that you entered in the **Set Target** stage in the **Budget vs. Target** section for annual type planning. If the total budget is more than the target cost, an exception icon \(\[Omitted image "exception\_icon\_1.png"\] Alt text: exception icon\) is shown with the total planned cost.
    -   Total planned cost for all the projects and demands for multi-year type planning in the **Total Planned Cost** section.
    -   Potential benefit amount that would accrue on execution of the selected demands and projects in the **Benefit Amount** section.

        **Note:** For multi-year resource capacity type planning, the total value of planned cost and benefit for the entire duration of the projects or demands is displayed irrespective of the selected planning window.

    -   Strategic alignment of your portfolio by viewing the number of demands and projects that are not associated with any organizational strategy or goal in the **Unaligned** section.
    -   Number of assignment groups where, for any quarter of the selected fiscal year, the number of requested hours is greater than the total hours capacity in the **Overallocated Groups** section.
    -   Review how much in actuals have been spent on the projects selected for execution and the rest of the projects in your portfolio in the **Actuals** section.

        **Note:** For multi-year resource capacity type planning, the actuals value is displayed in the widget without the selected and unselected project actual legends.

    The following image shows an example of how the portfolio information is displayed in the Overview section for annual type planning.

    \[Omitted image "overview-annual.png"\] Alt text: Overview tab in annual type planning

    The following image shows an example of how the portfolio information is displayed in the Overview section for multi-year type planning.

    \[Omitted image "overview-multi.png"\] Alt text: Overview tab for multi-year type planning

    Review the following sections of the **Resources** tab:

    View percentage of utilization for all the resources requested by the selected demands and projects of the portfolio in a heat map. You can view the percentage utilization of all resource groups or overallocated resource groups in months or quarters.

    **Tip:** Click any cell in the heat map to view the project or demand associated with the selected resource group.

    The following image shows an example of how the resource information is displayed in the heat map.

    \[Omitted image "percent\_utilization.png"\] Alt text: Heat map of % Utilization

    **Tip:** To bring the planned cost within the target budget and the resource utilization within 100%, consider deselecting a few low-priority demands or projects. Deselected demands and projects could then be moved over to a different fiscal period

7.  Review the capex and opex budget for individual projects and demands directly using **Capex Budget** and **Opex Budget** columns and revise it if necessary.

    **Note:** Click the Show or hide columns \(\[Omitted image "show\_hide\_columns.png"\] Alt text: Show or hide columns in Gantt icon\) in the **Timeline View** tab and add the **Capex Budget** and **Opex Budget** columns if these columns are not visible.

8.  Update the name and short description by clicking the edit icon \(\[Omitted image "edit\_scenario-details.png"\] Alt text: Edit scenario icon\) and making the modifications.

9.  Delete the scenario by clicking the delete icon \(\[Omitted image "delete\_scenario.png"\] Alt text: Delete scenario icon\).

10. Convert the selected scenario to become the current plan by clicking **Confirm**.

11. Create more planning scenarios to compare them.

12. Manually refresh the cost and resource widgets after a demand or a project is selected or cleared for execution by clicking the Refresh icon\[Omitted image "refresh\_icon.png"\] Alt text: Refresh button\).


## What to do next

Compare planning scenarios to analyze different combinations of projects and demands and select a scenario that best aligns with your organizational goals. For more information, see [Compare planning scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-management/compare-scenarios.md).

**Parent Topic:**[Create planning scenarios](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-management/create-scenarios.md)

