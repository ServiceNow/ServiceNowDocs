---
title: Legacy: Viewing the Performance reports for escalations
description: The Performance reports enable detailed review of how well escalations are being processed. You have precise control of the data that describes escalation progress using filters like group, priority, level, or escalation category.
locale: en-US
release: xanadu
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Generate and view reports, On-Call Scheduling, IT Service Management]
---

# Legacy: Viewing the Performance reports for escalations

The Performance reports enable detailed review of how well escalations are being processed. You have precise control of the data that describes escalation progress using filters like group, priority, level, or escalation category.

**Important:** Starting in Xanadu release, the On-Call dashboard is deprecated. Users can use [On-call dashboard](../../../use/dashboards/application-content-packs/performance-analytics/oncall-scheduling.md) to view, maintain, and track the performance reports.

## Opening the reports

You must have the Premium Dashboard user \[rota\_prem\_dashboard\_user\] role to view the Performance reports. Use one of the following methods to open the reports:

-   Click **Self-Service** &gt; **Dashboards** and select **On-Call Overview - Premium**.
-   Click **On-Call Scheduling** &gt; **Reports** &gt; **Overview**.

Click the **Performance** tab and then select the date of interest. The time line shows the time of day at which escalations happen. Use the tabs to control the type of data to view:

-   **Breakdowns tab**

    Use the filters to segment the data into categories that suit your need. For example, if you are investigating your SMS costs, you can set filters to display how many notifications of the SMS type are sent and to which groups or users they are being sent. For example, you might notice that you sent 68 SMS messages to users in the Network group. The group, however, did not acknowledge any escalations. You might therefore consider that you can lower SMS costs by not sending SMS notifications to that group.

    -   Groups
    -   Escalation Category
-   **Records tab**

    The **Records** tab lists the individual records that make up the results that you configured on the **Breakdowns** tab. Click a name to view record details.

    **Note:** Each record also appears in the appropriate escalation log. See [View details in an escalation log](../task/view-escalation-logs-oncall.md).


## All Escalations tab

-   Acknowledged escalations are accepted by at least one user.
-   Unacknowledged escalations are not accepted by any user or are rejected by all users.
-   All Escalations: Count of escalations that started on the selected date.
-   Escalation Notifications: Count of notifications that were sent on the selected date. An escalation might have triggered several notifications.

![All Escalations tab](../image/perform-all-esc-reports-tab.png "All Escalations tab")

## Acknowledged Escalations tab

![Performance > Acknowledged Escalations reports](../image/perform-ack-esc-reports-tab.png "Acknowledged Escalations tab")

-   Acknowledged Escalation Notifications: Count of escalations that had any of the following values in the **Response** field for the notification:
    -   Accepted or Accepted from other device
    -   Auto-assigned
-   Acknowledged Escalation %: Percent of escalations that had a valid value in the **Response** field for the notification.
-   Acknowledged Contact Attempt %: Percent of contact attempts that were acknowledged.

## Unacknowledged Escalations tab

Unacknowledged escalations have one of the following values for each member of an escalation path in the **Response** field for the escalation notification:

-   Rejected
-   Rejected from other device
-   Invalid response
-   \[no response\]

![Performance > Unacknowledged Escalations reports](../image/perform-unack-esc-reports-tab.png "Unacknowledged Escalations tab")

**Parent Topic:**[Viewing On-Call Scheduling reports](../../user-administration/concept/viewing-reports.md)

