---
title: Legacy- Financial planning workbench
description: The financial planning workbench is a central location to manage budget tasks, review, and approve the promoted plans. Financial planning workbench is deprecated in the Paris release. Financial planning workbench is still available on instances upgraded from a previous release but is not available for new instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/financial-planning-workbench.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Financial planning workbench

The financial planning workbench is a central location to manage budget tasks, review, and approve the promoted plans. Financial planning workbench is deprecated in the Paris release. Financial planning workbench is still available on instances upgraded from a previous release but is not available for new instances.

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

You must have the itfm\_plan\_analyst role to use the financial planning workbench.

Budget tasks help in streamlining the budget process. It helps finance to converse with budget owners during the budgeting period.

With the IT finance analyst role, you can use the workbench to:

-   **Generate budget task**: Create a budget task for every budget owner.
-   **Publish the budget task**: Publish the budget task for the budget owners to start their work on the plan for the budget period.
-   **Track the progress of the plan**: View and monitor the promoted plans for the budget period.
-   **Approve the plan**: Approve the promoted plan by approving the task.

**Note:** The planning workbench replaces the budget console that was used in the Jakarta release. Only the IT finance analyst can use the planning workbench and not the budget owner.

The financial planning workbench details are as follows:

-   The finance analyst can select the year and the budget plan definition. If budgeting period is open and the plans are not promoted yet, then the analyst has the option to create budget tasks for the budget owners.
-   After the budget tasks are generated, the finance analyst can update the targets and enter specific instructions in the budget tasks. The budget tasks are published for the budget owners to work on the plan for the budget period.
-   Then the promoted plans for the open budget or forecast period can be seen on the left pane.

\[Omitted image "FinancialPlanningWorkbenchAnalyst.png"\] Alt text: A sample of the planning workbench

The right pane of the financial planning workbench provides three types of views:

-   **Task View**

    View the list of tasks for each planner along with its status. Open a task record to add a note to the planner and update the state of the task.

-   **Plan View**

    View the plans that the planners have promoted. Use the grid view to:

    -   View the data by the columns that you configured in the template.
    -   Group the columns by any column, for example by cost center or vendor.
    -   View the budgeted amount, last forecast amount, and the actuals by year, quarter, or month.
-   **VTB View**

    View the budget tasks by its state:

    -   **Draft**

        The IT finance analyst has generated the task for a budget period.

    -   **Published**

        The IT finance analyst has published the task for the planner to work on the plan task.

    -   **Awaiting Input**

        The planner promotes the task to the IT finance analyst, but the analyst updates the task work note for the planner to rework on the budget amount.

    -   **Pending Approval**

        The planner has submitted the task and waiting for the IT finance analyst to approve or provide any comments on the plan task.

    -   **Approved**

        The IT finance analyst approves the plan.


The **Generate Actuals** button enables you to [generate actuals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_GeneralLedgerActuals.md) for the budget definition data source to view in the grid.

## What to do next

Create a budget period to promote a budget plan.

-   **[Legacy- Create a budget period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/create-a-budget-period.md)**  
The budget period controls the promotion of the budget plans. Budget plans created for a fiscal year can be promoted only if the budget period is open.
-   **[Legacy- Forecast period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/forecast-period.md)**  
Forecast periods are similar to budget periods that aim to control the promotion of forecast plans.
-   **[Legacy: Create a budget target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_CreateABudgetTarget.md)**  
A budget target is an estimated amount of money for a specific fiscal period and budget key combination for operating and capital expenses. Use budget targets to set up a financial goal for a budget plan.
-   **[Legacy- Generated actuals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_GeneralLedgerActuals.md)**  
Account code, or budget key, expenses are records that show general ledger amounts for a budget key. The amounts are aggregated for each fiscal period.
-   **[Legacy- Use the planning workbench to initiate a budget plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/use-the-financial-workbench-to-initiate-budget.md)**  
After you configure the budget process definition, you can initiate a budget. Open the budget period. Use the financial planning workbench, and select the fiscal period and the budget plan definition, and generate a budget task.

**Parent Topic:**[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)

