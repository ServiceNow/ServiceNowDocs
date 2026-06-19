---
title: Work with flapping alerts
description: If an alert is in the flapping state, you might need to triage the alert again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/operator-handle-alerts-flapping.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Work with flapping alerts

If an alert is in the flapping state, you might need to triage the alert again.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

Role required: evt\_mgmt\_operator

## About this task

If an event repeatedly triggers the same alert in a short amount of time, the alert is put into the flapping state, even if an operator closed it previously. The event can also be fluctuating between severity levels, such as Info and Critical. You should triage the alert again, and take action to try to prevent the event from reoccurring.

**Note:** Your Event Management administrator can configure several settings that determine when to mark an alert as flapping, and other settings that determine what action you can take. This topic covers a generic example.

## Procedure

1.  Find alerts in the flapping state:

    1.  Navigate to **Event Management** &gt; **Operators Workspace**.

    2.  Modify the list of alerts by clicking the filter icon \(\[Omitted image "filter-icon.png"\] Alt text: Filter icon\) and specifying criteria to find flapping alerts.

        Click **Advanced view** to modify filter settings. For example, you can specify:

        `State` \| `is` \| `Flapping`.

2.  Click the alert number to open it.

3.  On the alert, click the **Flapping** tab and review the information:

<table id="table_uzq_zff_3db"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flap count

</td><td>

The number of times the alert started flapping since the time in the **Flap start window** field.

</td></tr><tr><td>

Flap start window

</td><td>

The time that flapping started.

</td></tr><tr><td>

Flap last update time

</td><td>

The last time flapping occurred. This time is the instance processing time, not the source system time.

</td></tr><tr><td>

Flap last state

</td><td>

The state of the alert before it entered the flapping state.

</td></tr></tbody>
</table>4.  Decide which action to take based on how often flapping has occurred.

    You can do any of the following, depending on what your organization's standard operating procedures are and what your Event Management administrator configured:

    -   [Run a remediation workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-run-remdiation.md) that might do something like reboot a server or reset a router.
    -   [Access a web application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-launch-web-app.md), like the application for your event monitoring software on your network.
    -   [Modify an associated incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-phase-triage-incident.md) or a [KB article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-associate-kb.md) to include additional information or steps.
5.  After you are certain that the underlying issue is addressed, [close the alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-close-alert.md).


**Parent Topic:**[Advanced tasks for the Event Management operator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/operator-advanced-tasks.md)

