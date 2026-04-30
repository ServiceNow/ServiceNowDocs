---
title: Spotlight group copy logs
description: When a Spotlight group is copied, the steps of the copying process are recorded in logs. Use these logs to debug any issues.
locale: en-US
release: zurich
product: Spotlight
classification: spotlight
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Spotlight group copy logs

When a Spotlight group is copied, the steps of the copying process are recorded in logs. Use these logs to debug any issues.

Users with the pa\_spotlight or admin roles can read and delete Spotlight job logs.

The logs are listed at the following locations:

-   At **Spotlight** &gt; **Spotlight Group Copy Logs**.
-   As the Spotlight Group Copy Logs related list on the relevant Spotlight Group record.

The same Spotlight Group Copy Logs list opens in both places, but in the Spotlight Group form, the list is filtered by that Spotlight group.

To debug a Spotlight group copying job, open the group copy log from the list and examine the log row fields. You can also open a group copy log from the notifications that appear at the end of a copying job.

## Group copy log with errors

In this example, the Incident Spotlight group was copied for the Assignment Group breakdown elements Database, Field Services, Hardware, and US Presidents Group 1. However, after the copying job has completed, a notification shows that copying failed for three of those elements.![Notifications after a Spotlight group copying job, showing three failures and one success](../image/spotlight-copy-fail-note.png)

Clicking **Check the logs for details** opens the Spotlight group copy log for this copying job. In this log, you can find the errors that caused each failure. In the following example, a business rule violation prevented the copy from being created. The error message instructs you to contact the System Administrator.![Spotlight group copy log showing one of three errors](../image/spotlight-group-copy-log.png)

**Parent Topic:**[Ranking records with Spotlight](spotlight.md)

