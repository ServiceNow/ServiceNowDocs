---
title: Legacy- Use the planning workbench to initiate a budget plan
description: After you configure the budget process definition, you can initiate a budget. Open the budget period. Use the financial planning workbench, and select the fiscal period and the budget plan definition, and generate a budget task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/use-the-financial-workbench-to-initiate-budget.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Legacy- Financial planning workbench, Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Use the planning workbench to initiate a budget plan

After you configure the budget process definition, you can initiate a budget. Open the budget period. Use the financial planning workbench, and select the fiscal period and the budget plan definition, and generate a budget task.

## Before you begin

Role required: itfm\_plan\_analyst

An IT finance analyst generates a task for each planner. The planner can view the tasks that the planner owns by navigating to **Financial Planning** &gt; **My Tasks**.

## Procedure

1.  Navigate to **Financial Planning** &gt; **Workbench**.

2.  Select the budget period for which you are planning from the choice list on the top-right of the workbench.

    You can also [create a budget period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/create-a-budget-period.md) and open it to make it available for budgeting.

3.  Select the budget plan definition from the choice list.

4.  Click **Generate Task**.

    If the plan does not exist, and a plan task for the selected fiscal period, then clicking the **Generate Task** button creates a plan for each plan key. The plan key associated with the planner is considered only while generating the plan. The generated budget task is in **Draft** state.

5.  Open a budget task record from the budget list to review and update if required.

    As an IT finance analyst you can add a note to the planner in the **Work notes** field.

6.  Click **Update** to save your changes.

7.  Click **Publish** to publish the tasks.

    Set a **Start date** and an **End date** as a deadline for the plan in the Publish Planning Tasks pop-up that opens up.

8.  Click **Create**.

9.  Click the **Plan view**.

    To hide columns in the view, click the **Configuration** \[Omitted image "configurationplanview.png"\] Alt text: Configuration plan view icon icon.

    Item columns are rendered from the Budget Definition \[itfm\_plan\_definition\] table. Hiding or displaying an item column does not update the table. Grouped columns cannot be hidden.

10. Click the **VTB View**.

11. View the budget tasks by its state.

    If the planner had promoted the plan, then the plan is in **Pending Approval** column. If required, you can review the plan and make a recommendation.

12. To make a recommendation to the budget, click the task in the **Pending Approval** column.

13. Add a comment in the **Add description** field.

14. Close the budget task pop-up.

15. Drag the plan to the **Awaiting Input** column.

    After the planner updates and promotes the plan, then the state of the task becomes **Pending Approval**.

16. If the planner updates the plan with your recommendation and if the budgeted amount meets the target, then move the plan to the **Approved** column.

    The budget plan is approved.


## What to do next

As a planner you can update and promote your plans to finance.

**Parent Topic:**[Legacy- Financial planning workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/financial-planning-workbench.md)

