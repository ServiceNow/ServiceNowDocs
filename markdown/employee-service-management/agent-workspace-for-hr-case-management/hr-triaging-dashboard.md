---
title: HR Triaging Dashboard
description: The HR Triaging Dashboard enables you to review your teams' case assignments in a layout where cases are displayed as cards. This layout enables easy movement of case cards between lanes, enabling you to review and reassign cases by auto-updating HR service, or user, or priority.Configure the settings in the Triaging Dashboard so that you can view your team's case assignments categorized by HR service, or priority, or assignment group.
locale: en-US
release: australia
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Agent Workspace for HR Case Management, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# HR Triaging Dashboard

The HR Triaging Dashboard enables you to review your teams' case assignments in a layout where cases are displayed as cards. This layout enables easy movement of case cards between lanes, enabling you to review and reassign cases by auto-updating HR service, or user, or priority.

## Key features

-   Ability to configure lane \(priority, or assignment group, or HR service\) by which you want to view your teams' HR cases.
-   Ability to configure case fields and the order by which you want case fields to appear on the case card.
-   Auto-update priority, assignment, or HR service of an HR case by moving a case card from one lane to another.

![Triaging cases by users or assignment groups](../image/triage-by-user.png "HR Triaging Dashboard")

## Configure the HR Triaging Dashboard

Configure the settings in the Triaging Dashboard so that you can view your team's case assignments categorized by HR service, or priority, or assignment group.

### Before you begin

Role required: sn\_hr\_core.case\_writer

**Note:** Ensure that Kanban Components \[sn\_knbn\_comp\] and Kanban board component \[sn\_visual\_board\] are installed.

### Procedure

1.  Open HR Agent Workspace.

2.  Select the Triaging Dashboard icon ![Triaging dashboard](../image/triaging-dashboard-icon.png).

3.  Select the Settings icon ![Settings](../image/triage-settings.png).

4.  In the Settings section, perform the following steps:

    -   Select a COE \(Centers of Excellence\) to view only the HR cases specific to that COE. HR Centers of Excellence categorize cases based on unique function or discipline such as payroll or employee relations.
    -   Specify filter criteria to select fields that you want to view on the HR case card. Use the **Filter** criteria, or select the fields manually by expanding the **Fields to show on case card**.
    -   Choose a lane by selecting a value from the **Vertical lane** list: HR service, or priority or HR assignment group.

        1.  Select **HR Service** in the **Vertical lane** list.
        2.  Select the HR services that you want to view as vertical lanes in the HR Triaging dashboard.
        3.  Select the required value in the **Transfer method** field.

            |Field value|Description|
            |-----------|-----------|
            |Always ask|The transfer case window appears when you move a case card to another lane.|
            |Transfer with existing case number|When you move a case card to another lane, the case is assigned to the new HR service with the existing case number.|
            |Transfer with new case number.|When you move a case card to another lane, the case is assigned to the new HR service with a new case number.|

        4.  Select **Apply**.
        or

        1.  Select **Assignment group** in the **Vertical lane** list.
        2.  Select users.
        3.  Select **Apply**.
        or

        1.  Select **Priority** in the **Vertical lane** list.
        2.  Select **Apply**.

### What to do next

1.  View HR cases based on configured settings.
2.  Drag and move a card to the respective lane.
    1.  **HR service** as lane heading: When you drag a case from one lane to another, case transfer is done based on the value selected in the **Transfer method** field.
    2.  **Priority** as lane heading: When you drag a case from the one lane to another, the priority of case is updated to the respective lane value.
    3.  **Assignment group** as lane heading: When you drag a case from the one lane to another, the case is assigned to the respective lane user.

