---
title: Associate a knowledge base article with an alert
description: As an Event Management operator, you can associate a knowledge base \(KB\) article with the alert to capture additional information about the alert. This might include a procedure that someone has to follow to resolve the underlying issue on your network, or a best practice to prevent the issue from reoccurring.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Operator phase 2: Triage an alert, What Event Management operators do, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Associate a knowledge base article with an alert

As an Event Management operator, you can associate a knowledge base \(KB\) article with the alert to capture additional information about the alert. This might include a procedure that someone has to follow to resolve the underlying issue on your network, or a best practice to prevent the issue from reoccurring.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

<table id="table_ss3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![Analyze icon](../image/progress-complete2.png)

</td><td>

[Analyze and acknowledge an alert](operator-phase-acknowledge-analyze.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Operator icon](../image/progress-wip.png)

</td><td>

Triage alerts

</td></tr><tr><td>

Phase 3

</td><td align="justify">

![Operator do icon](../image/progress-not-started.png)

</td><td>

[Close an alert](operator-close-alert.md)

</td></tr></tbody>
</table>This task assumes that your organization uses the Knowledge Base application in your ServiceNow instance.

Role required: evt\_mgmt\_operator

## Procedure

1.  From the Service Operations Workspace dashboard, open the alert that you acknowledged in Phase 1: Analyze and acknowledge an alert.

2.  On the Alert form, click the lookup icon \(![Lookup icon](../image/lookup-icon.png)\) next to the **Knowledge article** field.

3.  Filter the list of existing KB articles by first selecting a field, such as **Short Description**, and then entering related text into the search text field.

    You can use the `contains` \(**\***\) operator to search for articles that contain keywords. For example, entering `*oracle` in the short description filters the KB articles that contain the word `oracle` somewhere in the short description.

    ![Search the KB](../image/search-kb.png)

4.  If you cannot find any related KB articles, you can click **New**, create a new one, and then click **Submit**.

    The KB article number appears in the **Knowledge article** field on the Alert form. ![KB number](../image/knowledge-article-number.png)

5.  Click **Update** on the Alert form to save the information.


## What to do next

There are also other tasks you can take as part of the triage stage:

-   [Run a remediation workflow on an alert](operator-run-remdiation.md) if your Event Management administrator already set up a workflow in your ServiceNow instance and your policies allow you to trigger it from the alert.
-   [Launch a web application from an alert](operator-launch-web-app.md) to open a website or an event monitoring tool that provides more information about the alert.
-   [Put an alert into maintenance](operator-put-alert-into-maintenance.md) to temporarily hide it from the Service Operations Workspace dashboard if the alert does not require action at this time.

If you do not need to perform any other triage actions, proceed to [Phase 3: Close an alert](operator-close-alert.md).

**Parent Topic:**[Operator phase 2: Triage an alert](operator-phase-triage-incident.md)

