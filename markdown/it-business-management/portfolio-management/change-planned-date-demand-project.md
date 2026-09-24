---
title: Change planned start date of a demand or project
description: Balance the cost and resources by changing the start date of a demand or a project and shifting it to a different fiscal period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/change-planned-date-demand-project.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Legacy- Select demands and projects for portfolio planning, Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Change planned start date of a demand or project

Balance the cost and resources by changing the start date of a demand or a project and shifting it to a different fiscal period.

## Before you begin

The demands and projects are open in the [timeline view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/demands-projects-view-port-workbench.md) of portfolio workbench.

Role required: it\_portfolio\_manager

## Procedure

1.  Click **Select Demands and Projects** under **Step 2** in portfolio workbench.

2.  In the timeline view, click the filter icon \(\[Omitted image "filter\_icon.png"\] Alt text: Filter icon\), and add the **Planned start date** column if it is not visible.

3.  To change the planned start date of a demand, double-click the value under the **Planned start date** column and pick a new date.

4.  To change the planned start date of a project, perform the following actions.

    1.  Right-click the project and select the **Edit** option.

    2.  On the Project form, right-click the header bar and select the **Move project** option from the context menu.

    3.  In the dialog box, pick a date, and click **OK**.


## Result

Changing the date has the following effects on cost plans and [resource plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/resource-management/c_ResourcePlans.md):

-   Cost plans: Cost plan dates are changed with respect to the change in project or demand date. For example, if a demand is shifted by two months, all the associated cost plans are also shifted by two months.
-   Resource plans: The resource plan dates are changed regarding the change in project or demand date. The changes in resource plan state are as follows:
    -   Allocated state resource plan: The effects on a resource plan in the Allocated state are:
        -   If the resource plan has a start date in the future, the resource plan is moved back to the Requested state.
        -   If the resource plan has a start date in past, the resource plan is canceled. The hard allocations for the past date are retained, and the future hard allocations are deleted. A new resource plan with new dates is created in the Requested state.
    -   Confirmed state resource plan: The soft allocations are deleted and the plan moves to the Requested state.
    -   Planning and Requested state resource plans: There is no change in resource plan state.

**Note:** The [project property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-management/r_InstalledWithProjectManagement.md) **Change Resource Plan and Cost Plan Start Date with Demand or Project Start Date Change** controls the changes in cost and resource plans with respect to the change in the start date of a demand or project.

**Parent Topic:**[Legacy- Select demands and projects for portfolio planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_SelectProjectsAndDemands.md)

