---
title: Managing portfolio financials in Strategic Planning Workspace
description: View the financial breakdown of estimates, approved costs, benefits, and actuals and so on for portfolio financials.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-10"
reading_time_minutes: 4
breadcrumb: [Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Managing portfolio financials in Strategic Planning Workspace

View the financial breakdown of estimates, approved costs, benefits, and actuals and so on for portfolio financials.

As a portfolio user, you can view the rolled up financial values of top-level demands, projects, and epics.

You can view the costs by expense type or cost type. Using the Financials view at portfolio level, you can view different financial fields such as Budget \(approved budget for planning items\), Forecast, Variance \(difference between the approved budget and latest forecast\), Actuals, and the Remaining Estimates for Capex, Opex, Total, and Benefits for each planning item. This information can be used to track the financials status of the planning items and take an informed decision on which planning items to consider while working on the next planning cycle and track the to avoid overspending.

Using the portfolio financials, portfolio managers can:

-   Track the financial performance and status of planning items.
-   Arrive at an informed decision by analyzing the estimated cost and benefits of a planning item while planning and prioritizing for the next Portfolio cycle.
-   View the financials based on the expense type or cost type depending on the [budget attribute configuration](../task/config-budget-allocation-attribute-spw.md).
-   Avoid overspending on planning items by comparing the approved budget with the latest forecast and actuals.

**Important:** New and existing customers need to configure the portfolio financials to view the financials of your planning items at portfolio level. For more information, see [Configure portfolio financials in Strategic Planning](../task/config-portfolio-fin-spw.md).

The portfolio financials view supports Demands, Epics, and Projects with Fiscal Calendar type configuration only.

![Portfolio financials page view expense type budget attribute.](../images/fin-portfolio-financials-page-expense-type.png "Portfolio financials grouped by Budget status with expense type as the budget attribute")

![Portfolio financials page view cost type budget attribute.](../images/fin-portfolio-financials-page-cost-type.png "Portfolio financials grouped by Planning status with cost type as the budget attribute")

**Note:** Group header row displays the rolled up values for Budget, Forecast, Variance, Actuals, and Remaining estimate of all the planning items in the group.

The default view of portfolio financials is set to display the planning items grouped by their budget approval status. Budget approved grouping lists the planning items which have the budget allocated and approved. Approval pending grouping lists the planning items which do not have any budget or if the requested budget is not approved.

**Note:** Portfolio financials view is not yet compatible with Investment Funding. This view may not show the right budget values allocated to planning items from Investment Funding application. This will be add as a future enhancement.

In the left-grid, planning item details such as name, rank, planning state, planning item type, approved start date, total planned cost, total actual costs, total planned benefits and ROI for the full planning item duration.

In the right-grid, financial attributes of the planning items such as, Budget, Forecast, Variance, Actuals, and Remaining Estimates for Capex, Opex, Total, and Benefits portfolio for the portfolio timeline or breakdowns by year, quarter, month, or period.

**Tip:** You can select the name of a planning item from the left-grid to directly access the financials record page of that planning item.

You can export the portfolio financials details to Excel or CSV using the **Export** option \(![Downward facing arrow indicating download option.](../images/fin-export-option.png)\).

## Customize your financials view

Customize the portfolio financials to view and access the required parameters helping you in better planning your portfolio and planning items.

-   You can get a more detailed and granular view of the financials at monthly, quarterly, and yearly view by defining Timescale and Range. Use time scale to select a fiscal period and filter the range within the time scale to view the financials for any specific months, quarters, or years.

    ![Time scale and range modal window.](../images/fin-timescale-range-modal.png)

<table id="table_uvy_5bw_12c"><thead><tr><th>

Time scale

</th><th>

Description and range

</th></tr></thead><tbody><tr><td>

Fiscal Month

</td><td>

Portfolio financials view by monthly breakdown.You can select up to 12 months.

</td></tr><tr><td>

Fiscal Quarter

</td><td>

Portfolio financials view by quarterly breakdown.You can select up to 4 quarters.

</td></tr><tr><td>

Fiscal Year

</td><td>

Portfolio financials view by yearly breakdown.You can select up to 5 years period.

</td></tr><tr><td>

Plan Timeline

</td><td>

Portfolio financial breakdown for the entire portfolio timeline.

</td></tr></tbody>
</table>-   Personalize grouping and columns in the grids.

    Configure the columns and groupings in the right-grid using Personalize option \(![Gear icon for personalization settings.](../images/icon-personalization-gear-symbol.png)\) to build a custom view.

    ![Checkboxes list to customize portfolio financials view.](../images/fin-personalize-right-grid.png)

    For example, if you want to compare budget and actuals breakdowns, select only these two options and apply your preferences. You can also customize the left-grid by selecting the required columns from the **Left Grid** list from the personalize settings.

-   Group the planning items.

    By default, the financials view is grouped by the Budget status column. You can remove Budget status grouping from the Grouped by row and drag-drop the required header to change this view.


