---
title: Impact of modifying the scenario planning type and scope
description: Modifying the planning type and scope impacts the demands and project selection in your planning scenarios and portfolio planning. You can change the planning type and scope at any time during portfolio planning.
locale: en-US
release: yokohama
product: Portfolio Management
classification: portfolio-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure the scenario planning type and scope, Scenario Planning for PPM, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Impact of modifying the scenario planning type and scope

Modifying the planning type and scope impacts the demands and project selection in your planning scenarios and portfolio planning. You can change the planning type and scope at any time during portfolio planning.

## Changing the planning type

Changing the planning type affects your portfolio planning regardless of whether the portfolio has any confirmed plan or planning scenarios in it at the time of this change.

-   **From annual financial planning to multi-year, resource capacity based planning**

    This change in the planning type has the following impact on your confirmed plans and planning scenarios:

    -   Deletes all scenarios and scenario funding records.
    -   A default scenario is created with the current month as starting month and a default of 3-month planning window.
-   **From multi-year, resource capacity based planning to annual financial planning**

    This change in the planning type has the following impact on your confirmed plans and planning scenarios:

    -   Deletes all scenarios and scenario funding records.
    -   If you were previously using annual planning, the target budget is retrieved. If not, the current fiscal year is set as default and you must set the target budget.

## Changing the planning window

Changing the planning window effects all the users involved in planning and has the following impact on your portfolio planning:

-   The new planning window applies to all scenarios and the confirmed plan of every portfolio.
-   A demand or project outside of the selected planning window cannot be selected or deselected. However, the value of **Planned** check box for the project or demand will not change. These demands and projects continue to be related to the scenario.
-   When you confirm a scenario, only the demands and projects that fall in the planning window are confirmed, the demands and projects outside the planning window are not confirmed.

## Changing the planning scope

Changing the planning scope from a single selected portfolio to all portfolios has the following impact on your confirmed plans and planning scenarios:

-   In case of annual planning, creates a portfolio planning record in the Tracking state if a confirmed plan exists for any of the portfolios.
-   In case of annual planning, creates a confirmed plan for all the fiscal years with at least one confirmed plan for any of the portfolios.
-   In case of multi-year planning, your confirmed plans for the portfolios are retained.
-   Deletes all existing scenarios and scenario funding records.

**Parent Topic:**[Configure the scenario planning type and scope](../task/configure-scenario-planning.md)

