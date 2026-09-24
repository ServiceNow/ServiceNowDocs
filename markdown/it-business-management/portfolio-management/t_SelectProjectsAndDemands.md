---
title: Legacy- Select demands and projects for portfolio planning
description: After you select the fiscal period and set budget targets, select the demands and projects to include in budget planning. You can view all the demands and projects lined up for the selected fiscal year with their planned cost and priorities to finalize them for execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/t\_SelectProjectsAndDemands.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Select demands and projects for portfolio planning

After you select the fiscal period and set budget targets, select the demands and projects to include in budget planning. You can view all the demands and projects lined up for the selected fiscal year with their planned cost and priorities to finalize them for execution.

## Before you begin

Role required: it\_portfolio\_manager

## About this task

In this stage, you can perform a what-if analysis by including or excluding demands or projects and their planned cost. The planned cost is derived from all the cost plans created for a project or demand. It is the total of all the costs from all cost plans for a given project or demand in the fiscal year.

## Procedure

1.  Click **Select Demands and Projects** under **Step 2** in portfolio workbench.

2.  In the [planning view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/demands-projects-view-port-workbench.md) of portfolio workbench.

<table id="choicetable_gqr_bgj_nx"><tbody><tr><td id="d198458e90">

**In Bubble Chart**

</td><td>

Right-click and select:-   **View demand** to open and view the [demand form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/demand-management/t_CreatingDemands.md).
-   **Select for execution** to include a demand in portfolio planning.
-   **Remove** to exclude a demand from portfolio planning.


</td></tr><tr><td id="d198458e124">

**In Timeline View**

</td><td>

Use the check box next to each project or demand in the list to include or exclude it from planning.

</td></tr></tbody>
</table>3.  Review these items in the planning view to select the demands and projects to be included or excluded from planning:

    -   Use the **Cost \(Planned vs. Target\)** chart to see planned costs versus the targets that you entered in the **Set Target** stage. If planned cost is more than the target cost, an exception icon \(\[Omitted image "ExceptionIcon.png"\] Alt text: screenshot for exception icon\) appears with the planned cost.
    -   Use the **Resource Overview** chart to see how many resource hours are requested to execute the selected demands and projects. Compare that to how many requested resources have been confirmed/allocated across all portfolios.
    -   Use the **% Utilization** heat map for all requested resources by the selected demands and projects in the portfolio.
    **Note:** To bring the planned cost within target budget and resource utilization within 100%, the portfolio manager deselects a few low priority demands or projects. These deselected demands and projects can be [moved over](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/change-planned-date-demand-project.md) to a different fiscal period.

4.  Review or revise the capex and opex [budget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/allocate-budget-to-project.md) for individual projects and demands directly using **Capex Budget** and **Opex Budget** columns, if required.

    Click the filter icon \(\[Omitted image "filter\_icon.png"\] Alt text: Filter icon\) in timeline view and add **Capex Budget** and **Opex Budget** columns if they are not visible.

5.  Once you have finalized the demands and projects, click **Confirm**.

6.  On the Confirm dialog box, you can select the two check boxes to perform additional actions on the selected demands and projects.

    Select the first check box either to only approve the selected demands or to convert them to projects. The check box differs depending on whether the [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **Create project\(s\) on confirming demands from portfolio workbench** is set to true or false:

    -   If the project property is true, then the check box is **Convert all the selected demands to projects** and selecting it approved and converts the selected demands to projects.
    -   If the project property is false, then the check box is **Approve all the selected demands to projects** and selecting it only approves the selected demands.
    Select the second check box **Confirm resources for selected projects and demands** to confirm the resources for selected demands and projects.

7.  Click **OK** on the Confirm dialog box.


## Result

Based on the check boxes selected on the Confirm dialog box, the following actions are performed:

-   Selected demands are either approved and converted to projects or only approved.
-   The resources are confirmed for selected demands and projects. All associated [resource plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/c_ResourcePlans.md) move from **Requested** state to **Confirmed** state.

## What to do next

[Legacy- Create and promote a budget plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_CreateABudgetPlanFromPortfolio.md) if [**Portfolio Planning**](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md) is set to **Advanced**.

-   **[Change planned start date of a demand or project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/change-planned-date-demand-project.md)**  
Balance the cost and resources by changing the start date of a demand or a project and shifting it to a different fiscal period.

**Parent Topic:**[Legacy- Plan the portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/c_FinancialPlanningForPortfolio.md)

