---
title: Legacy: Viewing Escalation Overview reports
description: Run Escalation Overview reports to view count and rate information on escalations currently in progress, acknowledged and unacknowledged escalations, and Mean Time to Acknowledge \(MTTA\). You can view data for all groups or for one or more selected groups.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Viewing On-Call Scheduling reports, On-Call Scheduling, IT Service Management]
---

# Legacy: Viewing Escalation Overview reports

Run Escalation Overview reports to view count and rate information on escalations currently in progress, acknowledged and unacknowledged escalations, and Mean Time to Acknowledge \(MTTA\). You can view data for all groups or for one or more selected groups.

**Important:** Starting in Xanadu release, the On-Call dashboard is deprecated. Users can use [On-call dashboard](../../../use/dashboards/application-content-packs/performance-analytics/oncall-scheduling.md) to view, maintain, and track the escalation reports.

## Opening the reports

Any user with the itil role can view the reports. Use one of the following methods to open the reports:

-   Click **Self-Service** &gt; **Dashboards** and select **On-Call Overview**. If you have licensed the premium version, then click **On-Call Overview - Premium**.
-   Click **On-Call Scheduling** &gt; **Reports** &gt; **Overview**.

Click the **Escalations Overview** tab.

## Escalations Overview reports

-   Acknowledged escalations are accepted by at least one user. The "true" value indicates acknowledged escalations.
-   Unacknowledged escalations are not accepted by any user or are rejected by all users. The "false" value indicates unacknowledged escalations.

![Escalations Overview reports](../image/escalations-overview-tab.png "Escalations Overview reports")

-   **My On-Call Groups**

    Select one or more groups. Only data for selected groups appears in the reports. If no group is specified, then data for all groups appears.

-   **Active Escalations - 7 days**

    The number of escalations that are currently in progress.

-   **Unacknowledged Escalations - 7 days**

    The number of escalations that nobody has yet acknowledged during the most recent seven-day period.

-   **Acknowledged Escalations**

    The number of escalations that escalatees have acknowledged during the most recent seven-day period.

-   **Acknowledged Escalations by Level - 7 days**

    The number of acknowledged escalations during the most recent seven-day period.

    -   The Y axis indicates groups.
    -   The X axis indicates escalation level.
    -   The color shade indicates the count of escalations in the box.
-   **Acknowledged and Unacknowledged Escalations by Group - 7 days**

    The number of escalations by group during the most recent seven-day period.

    -   The "true" value indicates acknowledged escalations.
    -   The "false" value indicates unacknowledged escalations.
-   **Escalations per Day**

    The number of escalations for the specified date.

    -   The Y axis represents the count of escalations.
    -   The X axis represents time by date.
-   **Mean Time to Acknowledge \(MTTA\) - 7 days**

    The average time that it took a user to acknowledge an escalation during the most recent seven-day period.

    -   The Y axis indicates the time it took a user to acknowledge an escalation.
    -   The X axis indicates the group.

**Parent Topic:**[Viewing On-Call Scheduling reports](../../user-administration/concept/viewing-reports.md)

