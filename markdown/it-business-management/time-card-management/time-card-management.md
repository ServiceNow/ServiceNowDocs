---
title: Time Card Management
description: The Time Card Management feature enables time card users such as task assignees to report and track their time for the assigned tasks.
locale: en-US
release: zurich
product: Time Card Management
classification: time-card-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Project Portfolio Management, Strategic Portfolio Management]
---

# Time Card Management

The Time Card Management feature enables time card users such as task assignees to report and track their time for the assigned tasks.

Video explaining how to set up the time tracking feature for projects, enter time, and approve time cards.Watch this three-minute video to learn about setup of the time tracking feature, entering time and approvals.

Time Card Management works with the Task table to record time worked on various task types, such as projects, incidents, problems, and change requests.

With the Time Card Management feature:

-   The time card users can record the time worked on a task using [time cards](c_TimeCards.md) and [time sheets](time-sheets.md). They can submit their time cards and time sheets for approval.
-   Time cards and time sheets are routed for approval based on the **Non-project time approver** and **Project time approver** fields in the user time sheet policy. User managers with time card approver role can also log time and [submit the time sheet of their resources](../task/submit-time-sheet-other-users.md)
-   The time card approvers can perform the following tasks:

    -   Review and approve or reject the time cards in a submitted time sheet.
    -   Recall the approved time sheets or time cards to return them to the users for corrections.
    -   Use dashboards to view reports of time card and time sheet exceptions, and categorize time reported by the users.
    -   Delegate another time card approver to process time sheets from your resources when you might not have time or will be unavailable. Note the following points for delegation:
        -   You cannot delegate approval only for an individual resource.
        -   The delegated time card approver cannot further delegate your time sheet approvals.
    The project\_manager and the resource\_manager roles contain the timecard\_approver role in the base system. However, the timecard\_approver role can also be used independently without these roles.

-   The time card admin can create and manage [time sheet policies](../task/create-time-sheet-policy.md#time_sheet_policy_form), and can also approve or reject by exception and process the time sheets. Time card admin can also create or edit time cards of any users if the time cards are in Pending or Rejected state.

**Note:** The [Time Card Management plugin](../task/t_ActivateTimeCardManagement.md) is required to use time cards. Some of the procedures require the project management feature, which activates time cards automatically. For more information, see [Project Management](../../../product/project-management/concept/c_ProjectApplicationOverview.md) \(com.snc.financial\_planning\_pmo\).

## Domain separation in Time Card Management

[Domain separation](domain-separation-time-card.md) provides complete data isolation for domain-specific users. Time card Management is domain separation compliant at the **Data only** level.

-   **[Activate Time Card Management](../task/t_ActivateTimeCardManagement.md)**  
Administrators can activate the Time Card Management plugin \(com.snc.time\_card\). The plugin also activates the Performance Analytics - Content Pack - Project Portfolio Suite Dashboards plugin \(com.snc.pa.time\_card\). However, you need a Performance Analytics license to use the dashboards.
-   **[Time sheet policies](time-sheet-policies.md)**  
Time sheet policies contain the policies to which a time sheet, or a time card must adhere.
-   **[Create a project time category](../task/create-project-time-category.md)**  
A time card admin or a project manager can create subcategories to define specific activities in the projects. The time card users can use these project subcategories to report time for a specific activity in a project.
-   **[Create a rate type](../../../product/cost-management/task/CreateRateType.md)**  
You can create rate types using the Rate Types feature.
-   **[Time Sheet Portal](worker-portal.md)**  
Time Sheet Portal categorizes and displays all your assigned tasks in a single view for a given week. The portal enables you to record time spent on tasks on a day-to-day basis and submit the time sheet in a single action.
-   **[Time Sheets](time-sheets.md)**  
A time sheet groups all the time cards for a user for the given week.
-   **[Time cards](c_TimeCards.md)**  
Time cards are used to record the time worked on a task by a task assignee.
-   **[Record time worked](c_RecordTimeWorked.md)**  
The time card retrieves time accrued on a project or spent working on any record in the Task table from the **Time worked** field.
-   **[Manage costs](c_ManageCosts.md)**  
When the cost management feature is enabled, time cards can be used to manage the cost of labor in the Cost Management application.
-   **[Analytics Project manager](project-manager-dashboard.md)**  
The Analytics Project manager provides the project managers with quick reports of time card exceptions, and category wise time reported for their projects. The dashboard displays time card reports only for the projects managed by a project manager.
-   **[Analytics User manager](user-manager-dashboard.md#)**  
The Analytics user manager provides the user managers with reports of time sheet exceptions, and category wise time reported by the users.
-   **[Performance Analytics dashboard for Time Card Management](../../../use/dashboards/application-content-packs/time-card-management-content-pack.md#)**  
This Platform Analytics Solution contains preconfigured dashboards. These dashboards contain actionable data visualizations that help you improve your business processes and practices.
-   **[Domain separation and Time Card](domain-separation-time-card.md)**  
Domain separation is supported in Time Card. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Mobile Time Sheets](../../../product/timesheet-mobile/concept/timesheet-mobile.md)**  
The ServiceNow® Mobile Timesheets app enables time sheet users and managers to access their time sheets from a mobile device. Mobile Time Sheets is available on the Now Mobile app and is supported on iOS and Android devices.

**Parent Topic:**[Project Portfolio Management](../../../product/project-portfolio-suite/concept/c_ProjectPortfolioSuite.md)

