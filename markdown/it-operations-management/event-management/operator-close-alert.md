---
title: Operator phase 3: Close an alert
description: After you take action on an alert, you can verify several items on the alert and then close it.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Operator phase 3: Close an alert

After you take action on an alert, you can verify several items on the alert and then close it.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_pp3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Analyze icon](../image/progress-complete2.png)

</td><td>

[Analyze and acknowledge an alert](operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Triage icon](../image/progress-complete2.png)

</td><td>

[Triage alerts](operator-phase-triage-incident.md)

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Close alert icon](../image/progress-wip.png)

</td><td>

Close an alert

</td></tr></tbody>
</table>Role required: evt\_mgmt\_operator

## About this task

## Procedure

1.  Navigate to **Workspace Experience** &gt; **Workspaces** &gt; **Service Operations Workspace**.

2.  Find the alert you want to close.

    If the alert does not appear in the list, for example because it is in maintenance, change the filter options as needed.

3.  Click the alert number to open the Alert Details tab and review key information about the alert.

    ![Alert fields to check](../image/alert-form-close-verifyfields.png)

4.  Review information about application services on the **Impacted Services** tab.

    In this example, the service\_1474 application service appears in the list.

    ![Impacted services tab](../image/view-impacted-services.png)

    If you need more information about an application service and want to see the service map, click the service name and then click **Service Map**.

5.  Look at the alerts related to this application service, and modify the correlation if necessary.

    The process for a primary alert differs from the process for a secondary alert.

    -   On a primary alert, the secondary alerts that are correlated with the primary appear on the **Secondary Alerts** tab.

        ![Correlated alerts](../image/alert-form-secondary-alerts.png)

        Typically, you do not have to do anything with the secondary alerts unless you want to add more secondary alerts or remove the correlation altogether.

        **Note:** When you close a primary alert, the secondary alerts are also closed by default.

    -   On a secondary alert:

        The alert number of the primary alert appears in the **Parent** field. You do not have to do anything with the parent alert, unless you want to re-correlate this secondary alert with another primary alert, or remove the correlation altogether by clearing the field.

        ![Parent field](../image/alert-form-parent-field.png)

        **Note:** When you close a secondary alert, the primary alert is not closed. You must close the primary alert separately.

6.  When you are sure the underlying issue causing the event and corresponding alert has been rectified, click **Close**.

    If you think that the alert needs attention, do not close it. Instead, put it into maintenance by selecting the **Maintenance** checkbox.


## What to do next

You are finished with the Event Management Operator tutorial, which covers a basic workflow of analyzing alerts, triaging them, and closing them out.

After you close an alert, you might need to follow up on these items:

-   **Reopen an alert**

    If you think an alert requires further action, you can manually change its state to **Reopen**. When an alert reopens, any associated incidents can also be updated or reopened according to the incident state and the rules that your administrator configured.

    **Note:** Any time you reopen an alert, always go through the triage and close phases again.

-   **Work with alerts in the flapping state**

    In some cases, the same event that created the alert you just closed could be triggered again, even repeatedly, in a short amount of time. If this occurs, the **State** of the alert that you just closed changes to **Reopen**, and eventually to **Flapping** depending on settings that your administrator configures.

    See [Handle alerts in the flapping state](operator-handle-alerts-flapping.md) for more information on what to look for.


For a summary of other tasks that you might need to perform at some time, see [Advanced tasks for the Event Management operator](../concept/operator-advanced-tasks.md).

**Parent Topic:**[What Event Management operators do](../concept/operator-process.md)

