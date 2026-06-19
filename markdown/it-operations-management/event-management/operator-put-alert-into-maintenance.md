---
title: Put an alert into maintenance
description: As an Event Management operator, you can put an alert into maintenance if the alert does not require any further action, but you still want to keep the alert active. Putting the alert into maintenance hides it from the Service Operations Workspace dashboard so that other operators do not need to access it, but it does not close the alert.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/event-management/operator-put-alert-into-maintenance.html
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Operator phase 2: Triage an alert, Operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Put an alert into maintenance

As an Event Management operator, you can put an alert into maintenance if the alert does not require any further action, but you still want to keep the alert active. Putting the alert into maintenance hides it from the Service Operations Workspace dashboard so that other operators do not need to access it, but it does not close the alert.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_pp3_ttt_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

\[Omitted image "progress-complete2.png"\] Alt text: Analyze icon

</td><td>

[Analyze and acknowledge an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

\[Omitted image "progress-wip.png"\] Alt text: Triage icon

</td><td>

Triage alerts

</td></tr><tr><td>

Phase 3

</td><td align="justify">

\[Omitted image "progress-not-started.png"\] Alt text: Close alert icon

</td><td>

[Close an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-close-alert.md)

</td></tr></tbody>
</table>Role required: evt\_mgmt\_operator

## Procedure

1.  From the Service Operations Workspace dashboard, open the alert that you acknowledged in Phase 1: Analyze and acknowledge an alert.

2.  Select the **Maintenance** check box and click **Update**, or click the **Maintenance** button at the top of the list.

3.  Click **Update**.

4.  Navigate to **Event Management** &gt; **Operators Workspace**.

    Notice that alerts in maintenance are not visible in the list by default. The filter excludes alerts where `Maintenance` \| `=` \| `true`.

    \[Omitted image "alerts-console.png"\] Alt text: filter


## What to do next

If the issue that led to the alert still needs further attention later, navigate to **Event Management** &gt; **All Alerts**, open the alert, and then clear the **Maintenance** check box and click **Update**. From there you can perform other triage actions.

There are other tasks you can take as part of the triage stage:

-   [Run a remediation workflow on an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-run-remdiation.md) if your Event Management administrator already set up a workflow in your ServiceNow instance and your policies allow you to trigger it from the alert.
-   [Launch a web application from an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-launch-web-app.md) to open a website or an event monitoring tool that provides more information about the alert.
-   [Associate a knowledge base article with an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-associate-kb.md) if there is existing information about the alert that might help resolve the underlying issue.

If you do not need to perform any other triage actions, proceed to [Phase 3: Close an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-close-alert.md).

**Parent Topic:**[Operator phase 2: Triage an alert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/event-management/operator-phase-triage-incident.md)

