---
title: Launch a web application from an alert
description: As an Event Management operator, you can also launch a web application from an alert. The web application might be a console for the event monitoring tool that your organization uses, or any external website that provides additional information you might need about the alert.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Operator phase 2: Triage an alert, What Event Management operators do, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Launch a web application from an alert

As an Event Management operator, you can also launch a web application from an alert. The web application might be a console for the event monitoring tool that your organization uses, or any external website that provides additional information you might need about the alert.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_qq3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Analyze icon](../image/progress-complete2.png)

</td><td>

[Analyze and acknowledge an alert](operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Triage icon](../image/progress-wip.png)

</td><td>

Triage alerts

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Close alert icon](../image/progress-not-started.png)

</td><td>

[Close an alert](operator-close-alert.md)

</td></tr></tbody>
</table>Role required: evt\_mgmt\_operator

You can launch a web application if your administrator has set up a link to the application. You should be familiar with your organization’s policies on triaging alerts.

## About this task

## Procedure

1.  From the Service Operations Workspace dashboard, open the alert that you acknowledged in Phase 1: Analyze and acknowledge an alert.

2.  On the Alert form, click **Quick Response**.

    ![Quick response](../image/quick-response.png)

3.  In the Quick Response window, click the name of the application under **Launch Application**.

    Your administrator has specified which applications should appear in the list.

    ![Launching a Web app](../image/launch-web-app.png)


## What to do next

There are also other tasks you can take as part of the triage stage:

-   [Run a remediation workflow on an alert](operator-run-remdiation.md) if your Event Management administrator already set up a workflow in your ServiceNow instance and your policies allow you to trigger it from the alert.
-   [Put an alert into maintenance](operator-put-alert-into-maintenance.md) to temporarily hide it from the Service Operations Workspace dashboard if the alert does not require action at this time.
-   [Associate a knowledge base article with an alert](operator-associate-kb.md) if there is existing information about the alert that might help resolve the underlying issue.

If you do not need to perform any other triage actions, proceed to [Phase 3: Close an alert](operator-close-alert.md).

**Parent Topic:**[Operator phase 2: Triage an alert](operator-phase-triage-incident.md)

