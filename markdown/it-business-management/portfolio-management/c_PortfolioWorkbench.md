---
title: Legacy portfolio workbench
description: The portfolio workbench provides a central location for viewing a list of associated demands and projects, planning a portfolio, and tracking its progress. Portfolio workbench is deprecated in the Paris release. Portfolio workbench is still available on instances upgraded from a previous release but is not available for new instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/c\_PortfolioWorkbench.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy portfolio workbench

The portfolio workbench provides a central location for viewing a list of associated demands and projects, planning a portfolio, and tracking its progress. Portfolio workbench is deprecated in the Paris release. Portfolio workbench is still available on instances upgraded from a previous release but is not available for new instances.

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

You must have the it\_portfolio\_manager role to use the portfolio workbench for:

-   [Portfolio planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md): Perform the planning of the portfolio. You can set the targets, select projects and demands, and create a budget plan in the portfolio.
-   [Portfolio budget forecasting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/forecast-plan-for-portfolio.md): As part of financial planning, re-estimate \(forecast\) the portfolio budget for future periods based on the actual costs.
-   [Portfolio tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_ReviewFinancialPlanning.md): View and monitor the progress of the program and the projects and demands that are part of the portfolio.

**Note:**

-   Portfolio workbench is based on Service Portal which means that you can configure, customize, and extend the workbench per your requirements and organizational workflow. See the [Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/c_ServicePortal.md) documentation for more information.
-   Portfolio workbench does not support mobile devices.

In addition to the Portfolio Workbench, starting with New York, you can use the Portfolio Planning Workbench do a scenario-based portfolio planning. This scenario-based planning enables you to focus your investment budget and resources on demands and projects that best position your organization.

Scenario Planning for PPM enables you to identify risks and uncertainties that might occur in the future and create possible planning scenarios and pursue whichever scenario becomes a reality. For example, you may have scenario A with all your chosen demands and projects, but you know that there's a risk that might reduce your team's velocity. You can reduce the velocity in scenario B and switch to it when the risk that you identified becomes a reality. For more information, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

The portfolio workbench shows the following sections for an [opened](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_AccessThePortfolioWorkbench.md) portfolio:

-   The left section provides the following fields used to plan the portfolio:
    -   **Fiscal Year**: The list to select the fiscal year you want to perform the planning for.

        **Note:** If there is no fiscal year in the list, [generate a fiscal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_GenerateFiscalCalendar.md).

    -   **Planning Steps**: The steps involved in planning the portfolio.

        -   Shows the completed and the current planning step number.
        -   Checks off the completed planning step.
        -   Highlights the current planning step in the portfolio.
        In the portfolio workbench example shown, the portfolio is in Step 2 \([**Select Demands and Projects**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_SelectProjectsAndDemands.md)\). It has completed through Step 1 \([**Set Target**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_SelectFiscalPeriodAndSetTargets.md)\).

-   The middle section shows a list of all the demands and projects that are part of the portfolio and fall under the selected fiscal year. The green check mark shows the demands and projects that have been selected for execution for the selected fiscal year.

    **Note:**

    -   Click a demand or a project in this section to open the respective record. You can make required changes to the project or demand form.
    -   A demand is included only if the **Expected Start** and **Due Date** fields are populated and the demand is in the approved or qualified state.
-   The lock in the upper-right section indicates that portfolio planning is not yet complete and that the tracking action is not enabled. Once the financial planning is complete, the [**Track Portfolio**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/track-view-portfolio-workbench.md)action is enabled for portfolio manager to track the progress of the portfolio.

\[Omitted image "PortfolioWorkbench.png"\] Alt text: Screen shot of Portfolio workbench

-   **[Access the legacy Portfolio workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_AccessThePortfolioWorkbench.md)**  
When you access the portfolio workbench, the dashboard displays a list of all the portfolios.
-   **[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)**  
As a portfolio manager, you can perform financial planning for a portfolio for a fiscal year using the portfolio workbench. Portfolio planning can be completed using either simple or advanced mode.
-   **[Legacy- Forecast the budget for portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/forecast-plan-for-portfolio.md)**  
As a project or portfolio manager, you can forecast the future costs of projects and portfolios based on the actual cost and changed project requirements. Budget forecast is deprecated in the Paris release. Budget forecast is still available on instances upgraded from a previous release but is not available for new instances.
-   **[Legacy- Track the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_ReviewFinancialPlanning.md)**  
After you complete financial planning, you can start tracking the progress of the portfolio. The portfolio tracking view displays only the selected demands and projects in the portfolio.
-   **[Actual project costs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_ActualProjectCosts.md)**  
Actual project costs come after you create expense lines for cost plans or after human resources use time cards to create expense lines.

**Parent Topic:**[Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_PortfolioManagement.md)

**Related topics**  


[Create a portfolio]()

[Open a portfolio status list]()

[Scenario Planning for PPM]()

[Portfolio Dashboard]()

