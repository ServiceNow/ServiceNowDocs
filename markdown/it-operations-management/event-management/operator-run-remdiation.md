---
title: Run a remediation workflow on an alert
description: As an Event Management operator, you can also run a workflow on your ServiceNow instance that helps remediate the alert. For example, you might run a workflow that automatically restarts a server on your network, which might resolve an alert about CPU usage.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Operator phase 2: Triage an alert, What Event Management operators do, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Run a remediation workflow on an alert

As an Event Management operator, you can also run a workflow on your ServiceNow instance that helps remediate the alert. For example, you might run a workflow that automatically restarts a server on your network, which might resolve an alert about CPU usage.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_pw3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Analyze alert icon](../image/progress-complete2.png)

</td><td>

[Analyze and acknowledge an alert](operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Triage alert icon](../image/progress-wip.png)

</td><td>

Triage alerts

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Close alert icon](../image/progress-not-started.png)

</td><td>

[Close an alert](operator-close-alert.md)

</td></tr></tbody>
</table>**Note:** You can run a remediation workflow if your administrator already set up workflows for you to choose from. You should be familiar with your organization’s policies regarding triaging of alerts.

Role required: evt\_mgmt\_operator

## Procedure

1.  From the Service Operations Workspace dashboard, open the alert that you acknowledged in Phase 1: Analyze and acknowledge an alert.

2.  On the Alert form, click **Quick Response**.

    ![Quick response](../image/quick-response.png)

3.  In the Quick Response window, click the name of the remediation under **Run Remediation**.

    ![Running a remediation](../image/run-remediation.png)


## What to do next

There are also other tasks you can take as part of the triage stage:

-   [Launch a web application from an alert](operator-launch-web-app.md) to open a website or an event monitoring tool that provides more information about the alert.
-   [Put an alert into maintenance](operator-put-alert-into-maintenance.md) to temporarily hide it from the Service Operations Workspace dashboard if the alert does not require action at this time.
-   [Associate a knowledge base article with an alert](operator-associate-kb.md) if there is existing information about the alert that might help resolve the underlying issue.

If you do not need to perform any other triage actions, proceed to [Phase 3: Close an alert](operator-close-alert.md).

**Parent Topic:**[Operator phase 2: Triage an alert](operator-phase-triage-incident.md)

