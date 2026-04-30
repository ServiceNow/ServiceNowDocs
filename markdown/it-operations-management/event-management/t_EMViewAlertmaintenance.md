---
title: View all alerts by the maintenance status
description: The Maintenance status indicates that the CI is under maintenance. For example, there is a software upgrade, and the issues can result from that activity, therefore all maintenance alerts are discarded.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View alert information, Using Event Management, Event Management, ITOM Health, IT Operations Management]
---

# View all alerts by the maintenance status

The **Maintenance** status indicates that the CI is under maintenance. For example, there is a software upgrade, and the issues can result from that activity, therefore all maintenance alerts are discarded.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The alert maintenance status can change due to any of these reasons:

-   A user selected the **Maintenance** check box on the alert, or selected the alert from the list view, and then clicked the **Maintenance** UI action.
-   A new alert that had been bound to a CI whose status is in maintenance status on the CMDB table.
-   If all previous events associated with the alert are in maintenance, the alert **Maintenance** field can automatically be set to **true** showing maintenance is in progress. However, if an alert **Maintenance** field is **false** but the related CI status is changed to **In Maintenance** after the alert was created, any subsequent events do not put the alert into maintenance. For example, if an alert is generated for a router and later the router is taken down for maintenance, it is still assumed that there was a problem before maintenance started and the issue must not be ignored.

**Note:**

-   If a maintenance flag was set on an alert in Geneva, after upgrading to Helsinki it affects the impact as a regular alert.
-   If an alert is bound to a CI by a user action \(such as an alert management rule\) and the CI is in the Maintenance state, you must manually bind the CI to the alert and mark it with the **In Maintenance** status.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All alerts**.

2.  Review the **Maintenance** column for each alert.

    A value of **true** indicates that the CI is under maintenance.

    **Note:** If the **Maintenance** field is not visible on the Alert form, personalize the list to add the field. For more information, see [Personal lists](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


**Parent Topic:**[View alert information](t_EMViewAlert.md)

