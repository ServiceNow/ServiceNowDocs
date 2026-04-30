---
title: Legacy: Viewing Group Overview reports
description: Run My Groups Overview reports to view the activities of a selected group: Count information on acknowledged and unacknowledged escalations by shift, acknowledged escalations by user, and the hours for each user over seven days.
locale: en-US
release: yokohama
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Generate and view reports, On-Call Scheduling, IT Service Management]
---

# Legacy: Viewing Group Overview reports

Run My Groups Overview reports to view the activities of a selected group: Count information on acknowledged and unacknowledged escalations by shift, acknowledged escalations by user, and the hours for each user over seven days.

**Important:** Starting in Xanadu release, the On-Call dashboard is deprecated. Users can use [On-call dashboard](../../../use/dashboards/application-content-packs/performance-analytics/oncall-scheduling.md) to view, maintain, and track the escalation reports.

## Opening the reports

Any user with the itil role can view the reports. Use one of the following methods to open the reports:

-   Click **Self-Service** &gt; **Dashboards** and select **On-Call Overview**. If you have licensed the premium version, then click **On-Call Overview - Premium**.
-   Click **On-Call Scheduling** &gt; **Reports** &gt; **Overview**.

Click the **My Groups Overview** tab and then specify the group in the **My On-Call Groups** list.

-   Acknowledged escalations are accepted by at least one user. The "true" value indicates acknowledged escalations.
-   Unacknowledged escalations are not accepted by any user or are rejected by all users. The "false" value indicates unacknowledged escalations.

## My Groups Overview reports

![My Groups Overview reports](../image/my-groups-overview-tab.png "My Groups Overview reports")

-   **On-Call Hours - 7 days**

    The sum for each day over the last seven days: \(Number of hours / roster member\) \* \(number of roster members that worked on an escalation\)

-   **Acknowledged and Unacknowledged Escalations by Shift - 7 days**

    The number of escalations by shift during the most recent seven-day period.

    -   The Y axis represents the count of escalations.
    -   The X axis represents the shift.
    -   The "true" value indicates acknowledged escalations.
    -   The "false" value indicates unacknowledged escalations.
-   **Hours Distribution by User - 7 days**

    Pie chart that displays the number of hours that each user in the group worked on escalations during the most recent seven-day period.

-   **Acknowledged Escalations by User - 7 days**

    Pie chart that displays the number of acknowledged escalations that each user in the group worked on during the most recent seven-day period.


**Parent Topic:**[Viewing On-Call Scheduling reports](../../user-administration/concept/viewing-reports.md)

