---
title: Spotlight job logs
description: The steps of Spotlight jobs are recorded in logs. Use these logs to debug any issues.
locale: en-US
release: zurich
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Spotlight job logs

The steps of Spotlight jobs are recorded in logs. Use these logs to debug any issues.

Users with the pa\_spotlight or admin roles can read and delete Spotlight job logs.

The logs are listed at the following locations:

-   At **Spotlight** &gt; **Spotlight Logs**.
-   As the Spotlight Job Logs related list on the relevant Spotlight Group record.

The same Spotlight Job Logs list opens in both places, but in the Spotlight Group form, the list is filtered by that Spotlight group.

To debug a Spotlight job, open the job log from the list and examine the job log row fields.

## Debugging Spotlight jobs

Consider the Incident Spotlight group, which evaluates real-time data from the Incident \[incident\] table. This table is the table that the indicator source of the Number of open incidents indicator uses. A Spotlight job runs on this Spotlight group every day at 15:00 hours. ![Details of the Incident Spotlight group](../image/incident-spotlight-group.png)

The Spotlight jobs for this group generate the following list of Spotlight job logs, where the most recent job completed with errors:

![List of spotlight job logs](../image/spotlight-job-logs.png "Spotlight job logs")

Clicking the timestamp of the 04:02:03 job shows a successful job with only informational messages.

![Successful Spotlight job log.](../image/spotlight-job-log-successful.png)

Returning to the list and opening the log for the job that had errors, you see that the Spotlight criterion **Incident more than 30 days old** is invalid.

![Spotlight job log with an error.](../image/spotlight-job-log-errors.png)

Navigating to the Spotlight criteria, you see that **Incident more than 30 days old** is an indicator-based criterion that uses the Age breakdown.

![Spotlight criterion that uses the Age breakdown.](../image/spotlight-invalid-criterion.png)

Viewing the Age breakdown shows that it uses a script in a breakdown mapping. ![Breakdown record for Age showing the Incident.Age.Days script used for a mapping](../image/spotlight-scripted-bkdown.png)

As shown at the top, the Incident Spotlight group evaluates real-time data. Therefore, the group cannot support criteria that use scripted breakdowns. For the job to run without errors, replace this criterion with a criterion that uses a query instead of an indicator and a breakdown. For example, create a criterion that queries the Incident \[incident\] table with the following conditions:

-   \[\[Opened\]\[relative\]\[on or before\]\[30\]\[Days\]\[ago\]\]
-   \[\[Opened\]\[relative\]\[on or after\]\[90\]\[Days\]\[ago\]\]

For more information, see [Create Spotlight criteria](../task/create-spotlight-criteria.md).

**Parent Topic:**[Ranking records with Spotlight](spotlight.md)

