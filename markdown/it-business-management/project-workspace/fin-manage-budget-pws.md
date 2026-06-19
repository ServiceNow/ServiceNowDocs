---
title: Manage budget of your projects using Project Workspace
description: Allocate, manage, and approve budget for your projects. Lean budgeting enables you to allocate budget for short planning cycles for different fiscal periods such as monthly, quarterly, or yearly breakdown level rather than allocating the budget to the complete duration of the planning item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/fin-manage-budget-pws.html
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage financials, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Manage budget of your projects using Project Workspace

Allocate, manage, and approve budget for your projects. Lean budgeting enables you to allocate budget for short planning cycles for different fiscal periods such as monthly, quarterly, or yearly breakdown level rather than allocating the budget to the complete duration of the planning item.

## Before you begin

-   As an Admin, enable the property to work on budgeting. For more information, see [Enable financial budget allocation for projects in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/enable-fin-budget-pws.md).
-   As an Admin, configure the attribute to allocate and approve budget by cost type or expense type. For more information, see [Configure budget attribute at instance-level to allocate budget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/config-budget-allocation-attribute-pws.md).
-   Role required: it\_portfolio\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  Select **Financials** from the left menu.

3.  Enable the **Budget allocation** toggle \(\[Omitted image "fin-budget-allocation-toggle.png"\] Alt text: Budget allocation toggle enabled to view budget.\).

4.  You can manage the budget by one of the following ways for the selected time scale at monthly, quarterly, or yearly level.

    -   Double-click each cell in the Budget column to manually enter the value.
    -   Select **Copy cost as budget** from the Budget column options to copy the EAC as budget.
    You can always reforecast the budget for each cost type using the in-grid editing feature even if the EAC is copied as budget.

    **Note:** Unapproved budget values are indicated with \[Omitted image "fin-copy-budget-icon.png"\] Alt text: Tick mark in a circle representing the unapproved budget icon.

5.  Select **Approve budget** \(\[Omitted image "fin-approve-budget-icon.png"\] Alt text: Approve budget button.\).

    Approve budget confirmation window is displayed. The **Create a financial baseline for this budget approval** option is enabled by default which captures the latest budget and financial estimates.

    **Tip:** The financial baseline created while approving the budget can be compared with the future baselines once the actual expenses are captured to track financial performance.

6.  On the confirmation window, select **Approve** \(\[Omitted image "fin-approve-icon.png"\] Alt text: Approve button.\).


## Result

Budget widget is updated to reflect the latest approved budget. Project Manager can view the approved budget and compare it with the planned costs using the **budget vs cost** view by cost type.

**Parent Topic:**[Managing financials for your projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-workspace/using-financials-prj-wrkspc.md)

