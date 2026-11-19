---
title: Spotlight job logs
description: The steps of Spotlight jobs are recorded in logs. Use these logs to debug any issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/spotlight/spotlight-logs.html
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

Consider the Incident Spotlight group, which evaluates real-time data from the Incident \[incident\] table. This table is the table that the indicator source of the Number of open incidents indicator uses. A Spotlight job runs on this Spotlight group every day at 15:00 hours. \[Omitted image "incident-spotlight-group.png"\] Alt text: Details of the Incident Spotlight group

The Spotlight jobs for this group generate the following list of Spotlight job logs, where the most recent job completed with errors:

\[Omitted image "spotlight-job-logs.png"\] Alt text: List of spotlight job logs

Clicking the timestamp of the 04:02:03 job shows a successful job with only informational messages.

\[Omitted image "spotlight-job-log-successful.png"\] Alt text: Successful Spotlight job log.

Returning to the list and opening the log for the job that had errors, you see that the Spotlight criterion **Incident more than 30 days old** is invalid.

\[Omitted image "spotlight-job-log-errors.png"\] Alt text: Spotlight job log with an error.

Navigating to the Spotlight criteria, you see that **Incident more than 30 days old** is an indicator-based criterion that uses the Age breakdown.

\[Omitted image "spotlight-invalid-criterion.png"\] Alt text: Spotlight criterion that uses the Age breakdown.

Viewing the Age breakdown shows that it uses a script in a breakdown mapping. \[Omitted image "spotlight-scripted-bkdown.png"\] Alt text: Breakdown record for Age showing the Incident.Age.Days script used for a mapping

As shown at the top, the Incident Spotlight group evaluates real-time data. Therefore, the group cannot support criteria that use scripted breakdowns. For the job to run without errors, replace this criterion with a criterion that uses a query instead of an indicator and a breakdown. For example, create a criterion that queries the Incident \[incident\] table with the following conditions:

-   \[\[Opened\]\[relative\]\[on or before\]\[30\]\[Days\]\[ago\]\]
-   \[\[Opened\]\[relative\]\[on or after\]\[90\]\[Days\]\[ago\]\]

For more information, see [Create Spotlight criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/spotlight/create-spotlight-criteria.md).

**Parent Topic:**[Ranking records with Spotlight](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/spotlight/spotlight.md)

