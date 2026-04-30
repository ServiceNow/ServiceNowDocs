---
title: Activate teams and services in SRM
description: Activate teams and services on ServiceNow's platform to be managed in the SRM application.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Activate teams and services in SRM

Activate teams and services on ServiceNow's platform to be managed in the SRM application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  In the **Service Operations Management** tile, select **Configure**.

    You’re taken to **Service Operations Management**

3.  Navigate to **Assign and activate** &gt; **Activate teams and services**.

4.  Select **Activate teams and services**.

    You reach to the **Activate teams** option to import or add teams. The Assignment groups view below contains teams that can be imported into SRM.

5.  In the Editor pane, use the Condition builder to add new filters to the list view.

    **Note:**

    Filters for the same fields evaluate as AND, filters for different fields evaluate as OR. For example, if you filter for **Business Criticality** and **State** is **Open**, the filter evaluates **Business Criticality** as 1- most critical OR 2 - somewhat critical OR 3 - less critical OR 4 - not critical AND **State** **Open**.

    When you change your list view filters, it remembers your settings, automatically, so that if you navigate away they are still set when you return.

    The list view refreshes with all filters.

6.  From the Assignment groups, select the teams you want to add, and select **Activate**.

    You reach to the **Activate services** option to add services.

7.  From the **Select a service class** list, select a service.

    The following six services are available:

    -   Application Services
    -   Mapped Application Services
    -   Calculated Application Services
    -   Dynamic CI Group
    -   Technical Services
    -   Tag-based Services
    The selected services view below contains services that can be imported into SRM.

8.  In the Editor pane, use the Condition builder to add new services to the list view.

    **Note:**

    Filters for the same fields evaluate as AND, filters for different fields evaluate as OR. For example, if you filter for **Business Criticality** and **State** is **Open**, the filter evaluates **Business Criticality** as 1- most critical OR 2 - somewhat critical OR 3 - less critical OR 4 - not critical AND **State** **Open**.

    When you change your list view filters, it remembers your settings, automatically, so that if you navigate away they are still set when you return.

    The list view refreshes with all filters.

9.  From the selected services, select the services you want to add, and select **Activate**.

    The **Activate Services** pop-up opens.

10. From the **Support Group** drop-down, select the support group which will own the services, and select **Confirm**.


## Result

On the **Activate teams and services** page, the following options appear:

-   Existing teams
-   Existing services

You can select the options to view the teams or services.

**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Import services for use in Service Reliability Management](sr-import-services.md)

**Next topic:**[Customize service approval settings in SRM](sr-add-approval-services.md)

