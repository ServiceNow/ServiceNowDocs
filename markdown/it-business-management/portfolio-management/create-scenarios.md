---
title: Create planning scenarios
description: Create planning scenarios with different combinations of projects and demands in your portfolio. Experiment with different scenarios to plan your budget expenditure for a fiscal year.
locale: en-US
release: australia
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create planning scenarios

Create planning scenarios with different combinations of projects and demands in your portfolio. Experiment with different scenarios to plan your budget expenditure for a fiscal year.

## Before you begin

Ensure that you have set the target budget for the fiscal year for which you want to create a planning scenario for annual type of planning. For more information, see [Set target budget for a fiscal year](select-fiscal-period-set-target.md). Setting of target is not required for multi-year resource capacity type of planning.

Role required: it\_portfolio\_manager

## About this task

You can create up to four planning scenarios with different combinations of projects and demands for execution. For example, you might create a scenario A and select all the projects and demands with your standard resource allocation. If you’re aware that a risk might affect the business outcome, you can create a scenario B with a reduced number of projects and demands to see whether that strategy might mitigate or avoid the risk. For more information about defining scenarios, see [Scenario Planning for PPM](../concept/portfolio-planning-overview.md).

## Procedure

1.  Navigate to the Portfolio Planning Workbench from either of two starting points.

<table id="choicetable_xfs_1fh_jlb"><thead><tr><th align="left" id="d248986e78">

Location

</th><th align="left" id="d248986e81">

Steps

</th></tr></thead><tbody><tr><td id="d248986e87">

**From application navigator**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **Portfolio Planning Workbench**.
2.  From the **Portfolio** choice list, select the portfolio that you want to perform the planning for.


</td></tr><tr><td id="d248986e120">

**From the portfolio list**

</td><td>

1.  Navigate to **Project** &gt; **Portfolios** &gt; **All**.
2.  Open the portfolio that you want to perform the planning for.
3.  In the Portfolio form, click the **Portfolio Planning** related link.


</td></tr></tbody>
</table>2.  In the Planning Portfolio Workbench, create a scenario for annual financial and resource capacity based planning or multi-year resource capacity based planning.

    -   For annual planning, perform the following steps:
    1.  Select the fiscal year for which you want to create a planning scenario.

    2.  Click the **Start Planning** button on the Welcome page.

        A default planning scenario is created with all active demands and projects for the selected fiscal year.

        **Note:** If a portfolio plan exists for the selected fiscal year, the Portfolio Planning Workbench displays it as the current plan.

    3.  Click the create scenario icon \(![Create scenario icon](../image/create_scenario_icon.png)\).

    4.  In the Create Scenario dialog box, enter a name and short description for the scenario.

    5.  In the Copy Data From list, select the source for copying data.

        The available options are:

        -   **None**: Creates a scenario with no projects or demands selected.
        -   **Ongoing projects funded last year**: Creates a scenario using projects funded during the previous year and continuing in the current year selected. This option is available only if an existing approved plan for the previous year exists. This is the default option when you create an initial scenario for a given fiscal year.
        -   **A list of other scenarios**: Creates a scenario using projects and demands selected from another existing scenario. This option is available if other scenarios exist for the same portfolio for the same fiscal year.
        -   **Confirmed Plan**: Creates a scenario with projects and demands selected from the existing approved plan. This option is available only if a confirmed plan exists for the current fiscal year.
    6.  Click **Save**.

    -   For multi-year planning, a default plan is automatically created with the current month as the starting month, and the planning window period as configured in the Scenario Planning Configuration page. To create a new scenario, perform the following steps:
    1.  Click the create scenario icon \(![Create scenario icon](../image/create_scenario_icon.png)\).

    2.  In the Create Scenario dialog box, enter a name and short description for the scenario.

    3.  In the Copy Data From list, select the source for copying data.

        The available options are:

        -   **None**: Creates a scenario with no projects or demands selected.
        -   **Ongoing projects funded last year**: Creates a scenario using projects funded during the previous year and continuing in the current year selected. This option is available only if an existing approved plan for the previous year exists. This is the default option when you create an initial scenario for a given fiscal year.
        -   **A list of other scenarios**: Creates a scenario using projects and demands selected from another existing scenario. This option is available if other scenarios exist for the same portfolio for the same fiscal year.
        -   **Confirmed Plan**: Creates a scenario with projects and demands selected from the existing approved plan. This option is available only if a confirmed plan exists for the current fiscal year.
    4.  Click **Save**.


## Result

The planning scenario is created and displayed in a new tab.

## What to do next

[Select projects and demands for execution](select-prj-demands.md) in the planning scenario.

-   **[Select demands and projects for portfolio planning](select-prj-demands.md)**  
After you create a planning scenario, select the demands and projects to include in budget planning. You can view all the demands and projects for the selected fiscal year or planning window with their planned cost and priorities to finalize them for execution.
-   **[Review external dependencies between projects](sp-review-ext-dependencies-between-prj.md)**  
Review the external dependencies between projects in a portfolio to track projects that are dependant on each other more closely.
-   **[Rank demands and projects](rank-demands-projects.md)**  
Rank demands and projects to prioritize demands and projects for their approval and execution within a portfolio.

**Parent Topic:**[Scenario Planning for PPM](../concept/portfolio-planning-overview.md)

