---
title: View all alerts by the maintenance status
description: The Maintenance status indicates that the CI is under maintenance. For example, there is a software upgrade, and the issues can result from that activity, therefore all maintenance alerts are discarded.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/event-management/t\_EMViewAlertmaintenance.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View alert information, Use, Event Management, ITOM AIOps, IT Operations Management]
---

# View all alerts by the maintenance status

The **Maintenance** status indicates that the CI is under maintenance. For example, there is a software upgrade, and the issues can result from that activity, therefore all maintenance alerts are discarded.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The alert maintenance status can change due to any of these reasons:

-   A user selected the **Maintenance** check box on the alert, or selected the alert from the list view, and then clicked the **Maintenance** UI action.
-   A new alert that had been bound to a CI whose status is in maintenance status on the CMDB table.
-   If all previous events are in maintenance, the **Maintenance** field is automatically set to **true**. However, if the **Maintenance** field is **false** and the CI status changes to **In Maintenance** after the alert was created, subsequent events do not put the alert into maintenance. For example, if a router alert is generated and the router is later taken down for maintenance, the original problem predates maintenance and must not be ignored.

**Note:**

-   If a maintenance flag was set on an alert in Geneva, after upgrading to Helsinki it affects the impact as a regular alert.
-   If a user action binds an alert to a CI in the Maintenance state, manually bind the CI to the alert and set its status to **In Maintenance**.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All alerts**.

2.  Review the **Maintenance** column for each alert.

    A value of **true** indicates that the CI is under maintenance.

    **Note:** If the **Maintenance** field is not visible on the Alert form, personalize the list to add the field. For more information, see Personal lists.


**Parent Topic:**[View alert information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/t_EMViewAlert.md)

