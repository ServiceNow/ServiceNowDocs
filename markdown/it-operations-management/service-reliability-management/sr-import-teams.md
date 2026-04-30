---
title: Import teams to Service Reliability Management
description: REVISE FOR ADMIN CENTER
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Import teams to Service Reliability Management

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Navigate to **Service Operations Management** &gt; **Assign and import** &gt; **Import teams**.

    The Teams list view below contains default filters already applied for which teams can be imported into SRM. They are not editable.

    **Note:**

    Filters for the same fields evaluate as AND, filters for different fields evaluate as OR. For example, if you filter for **Business Criticality** and **State** is **Open**, the filter evaluates **Business Criticality** as 1- most critical OR 2 - somewhat critical OR 3 - less critical OR 4 - not critical AND **State** **Open**.

    When you change your list view filters, it remembers your settings, automatically, so that if you navigate away they are still set when you return.

    Default filters are:

    -   **\[Type\] \[!=\] \[c419b12deb412110...\]**
    -   **\[Type\] \[is\] \[empty\]**
    -   **\[Active\] \[is\] \[true\]**
3.  In the Filter and select tab:

    1.  Use **View default filters** to see the filters in the pop-up window.

    2.  Use the Condition builder to add new filters to the list view.

    The list view refreshes with all filters.

4.  Use the check box in the list view to select the teams to import.

5.  Select **Preview**.

    You move to the **Teams for import** tab.

6.  Review the teams and select **Import**.

    If you change your mind and return to the **Filter and select** tab, you can still import the teams you selected, or leave without importing.

    The imported teams are available in SRM.

7.  Use the **View imported teams** link that now appears in the **Assign and import** &gt; **Import teams** screen to see all the teams available in SRM.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Customize team approval settings in SRM](sr-add-approval-teams.md)

**Next topic:**[Edit and publish a team request form for SRM](sr-edit-team-request-form.md)

