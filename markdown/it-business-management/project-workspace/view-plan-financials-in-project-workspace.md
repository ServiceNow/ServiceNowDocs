---
title: View forecasts and manage financial plans for a project in classic Project Workspace
description: Use the Financials tab in Project Workspace to capture the costs and benefits of a project.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Project workspace classic - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# View forecasts and manage financial plans for a project in classic Project Workspace

Use the **Financials** tab in Project Workspace to capture the costs and benefits of a project.

**Important:**

Classic Project Workspace is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base. Use new Project Workspace with enhanced UI to help you efficiently manage your projects.

## Before you begin

Role required: it\_project\_manager

## About this task

The **Financials** tab provides a detailed breakdown of the cost components of a project. The total planned cost, budget cost, actual cost, and planned returns with their breakdowns are displayed in the form of read-only cards, while the cost plans, benefit plans, and their breakdowns are provided in an editable grid view. Using the grid view, you can:

-   Group the plan level columns; configure, sort, expand, collapse, and freeze both the plan level and breakdown columns.
-   Inline edit the breakdown values of a cost plan or benefit plan without opening the plan in a form. Inline edit is available only in the Monthly view.
-   Create a cost plan and benefit plan for the project.

## Procedure

1.  [Open](access-the-project-workspace.md) the required project in [project workspace](../concept/project-workspace-classic.md).

2.  Click the **Financials** tab.

3.  To create a cost plan:

    1.  Select **Cost Plans** from the list.

    2.  Click **New**.

4.  To create a monetary benefit plan:

    1.  Select **Monetary Benefit Plans** from the list.

    2.  Click **New**.

5.  To view the project costs and financial breakdown summary of a project for the selected fiscal year, select **Overview** from the list.

    The **Overview** tab gives the financial summary for Planned Cost, Actual Cost, Variance \(Planned vs Actual cost\), Estimate At Completion, and Estimate To Completion.

    **Note:** If a project has a sub-project with a cost plan, the financials overview breakdown view is not enabled by default. To enable this view, a user with the it\_pps\_admin role should set the value of the **com.snc.project.rollup.cost** property to **true**.

    -   You can manage the financial summary view on the **Overview** tab.

        1.  Navigate to **All** &gt; **System Definitions** &gt; **Script Includes**.
        2.  Search for and select the **PmOverviewTabConsts** script.
        3.  Rearrange or remove the code from the **Script** and click **Update**.
        You can drag the headers and drop them at the required position to rearrange the financial summary columns on the **Overview** tab. This arrangement resets after the current session ends or expires.

    -   The admin can configure the level at which the financials overview data is displayed for the fiscal year in the **Project related properties** page by navigating to **Project Administration** &gt; **Settings** &gt; **Preferences - Project**. If no value is specified, by default, the financials are displayed at the quarterly breakdown.
6.  Review additional fields, view plan details, or reorganize the comparative data on the form.

    -   To create a baseline or compare the available baselines, click the baseline information icon \(![Baseline information icon.](../../planning-and-policy/image/gannt_chart_icon.png)\) and then select **Create New Baseline** or **Compare Baselines** option, respectively.

        In the Financial Baseline comparison screen, the top two rows show all the values in either functional currency or project currency. To display the values in project currency, click the configuration icon \(![Configuration icon.](../image/configuration_investment.png)\) and toggle the Show Widgets in Project Currency view.

        The Financial Baseline Details pane indicates the Functional Currency and the Project Currency that has been selected.

        The Financial Baseline grid shows the Functional cost, Cost in Project currency, Actuals, and Actuals in Project Currency. You can view the Project currency at the grid level. This view is helpful when there are cost plans of sub-projects that are in different project currency.

    -   To view a cost plan or benefit plan details on a form, click the information icon \(![Information icon.](../../planning-and-policy/image/informationicon.png)\) available in the Name column of the grid.
    -   To view a cost plan or benefit plan details in yearly, quarterly, or monthly format, click the **Year**, **Quarter** or **Month** views respectively.
    -   To toggle viewing the widgets in the Financial Summary section, click the widgets icon \(![Widgets icon.](../image/configuration_investment.png)\) and then select the **Show Widgets** option.

        Select an individual widget name to display the widget. Clear the selection to hide the widget.

        The selected field preferences are saved and are available when you reopen the **Financial** tab.

    -   To show or hide columns in the grid, click the configuration icon \(![Configuration icon.](../image/configuration_investment.png)\) and select the field names.

        You cannot hide the grouped columns. To reset to the default grid column layout, select the **Reset to defaults** option.

    -   To view the project costs in project currency, click the configuration icon \(![Configuration icon.](../image/configuration_investment.png)\) and select the five widgets to show project currency amounts. The widgets are Total Planned Cost in Project Currency, Budget Cost in Project Currency, Actual Cost in Project Currency, Planned Return in Project Currency, and Benefit in Project Currency.

        You can view both the functional and project currencies in the currency indicator.

        In the Financial Summary grid view of the **Cost Plans** and **Benefit Plans** tabs, all items related to project currencies are configured in the column heads such as **Cost in project currency**, **Project currency**, and **Total actual cost in project currency**.

        By default, you can view only the functional currency columns. To view the project currency columns, click the configuration icon \(![Configuration icon.](../image/configuration_investment.png)\) and select the project currency column check boxes in the item columns.

        The aggregated amount in the **Cost in project currency** field is clear if there are cost plans of sub-projects with different project currency.


-   **[Configure a widget for project financial metrics](configure-widget-project-financials.md)**  
Configure a widget to view and track the financial metrics of a project on the **Financials** tab of the Project Workspace page.

**Parent Topic:**[Project workspace classic - Legacy](../concept/project-workspace-classic.md)

