---
title: Import services for use in Service Reliability Management
description: Filter and import services on ServiceNow's platform to be managed in the Service Operations Management applications.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Import services for use in Service Reliability Management

Filter and import services on ServiceNow's platform to be managed in the Service Operations Management applications.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Navigate to **Service Operations Management** &gt; **Assign and import** &gt; **Import services**.

    Only services which aren’t already imported to SRM will be visible.

    The Services list view below contains default filters already applied for which services can be imported into SRM. They aren’t editable.

    **Note:**

    Filters for the same fields evaluate as AND, filters for different fields evaluate as OR. For example, if you filter for **Business Criticality** and **State** is **Open**, the filter evaluates **Business Criticality** as 1- most critical OR 2 - somewhat critical OR 3 - less critical OR 4 - not critical AND **State** **Open**.

    When you change your list view filters, it remembers your settings, automatically, so that if you navigate away they are still set when you return.

3.  In the **Filter and select** tab:

    1.  Use **View default filters** to see the filters in the pop-up window.

    2.  Use the condition builder to add new filters to the list view.

    The list view refreshes with all filters.

4.  Use the check boxes in the list view to select the services to import.

5.  Select **Preview**.

    You move to the **Services for import** tab.

6.  Review the services and select **Import**.

    If you change your mind and return to the **Filter and select** tab, you can still import the services you selected, or leave without importing.

    The imported services are available in SRM.

7.  Use the **View imported services** link that now appears in the **Assign and import** &gt; **Import services** screen to see all the services available in SRM.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

**Next topic:**[Activate teams and services in SRM](sr-activate-teams-and-services-in-srm.md)

