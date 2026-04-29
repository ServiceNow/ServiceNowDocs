---
title: Handle alerts while CIs are in maintenance
description: When an alert occurs on a CI that is in the maintenance state, the alert state is also changed to maintenance. You should find and monitor the states of these alerts. Later, when changes on the CI are complete, finish triaging the alert and close it.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Handle alerts while CIs are in maintenance

When an alert occurs on a CI that is in the maintenance state, the alert state is also changed to maintenance. You should find and monitor the states of these alerts. Later, when changes on the CI are complete, finish triaging the alert and close it.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

Before completing this task, familiarize yourself with basic form configuration in an instance. You might need to add fields and related lists to forms.

The example in this topic assumes that a network administrator opened a change request to reconfigure a problematic web server.

Role required: evt\_mgmt\_operator

## Procedure

1.  Find alerts in maintenance:

    1.  Navigate to **Event Management** &gt; **Operators Workspace**.

    2.  Click the filter icon \(![Filter icon](../image/filter-icon.png)\) and in the Filter box, click **Advanced view** and specify:

        `State` \| `is` \| `Maintenance`.

2.  In the list of alerts, find an alert with a value in the **Configuration Item** column.

    This is the CI on which the alert occurred.

3.  Click the CI name to open the form that displays information about the CI.

    In this example, the status of the web server is **In Maintenance** and there is a change request scheduled so that someone can reconfigure it.

4.  Click the CI name to open the form that displays information about the CI.

    In this example, the status of the server \(on the **Details** tab\) is **In Maintenance**. You can view the scheduled change request on the **Change Requests** tab \(someone will reconfigure the CI\).

    ![Maintenance](../image/ci-in-maint.png)

    ![Change](../image/ci-change-request.png)

5.  At this point, you should not modify the alert associated with this CI.

    You can open the change request to see if a schedule is attached, or coordinate with your team to find out when the CI will no longer be in maintenance.

6.  After you verify that the **Status** field on the CI is not **In Maintenance**, open the alert again and clear the **Maintenance** check box.

7.  Continue to [triage the alert](operator-phase-triage-incident.md).


**Parent Topic:**[Advanced tasks for the Event Management operator](../concept/operator-advanced-tasks.md)

