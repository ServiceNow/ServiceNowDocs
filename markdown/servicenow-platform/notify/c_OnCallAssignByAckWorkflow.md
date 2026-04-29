---
title: On-Call Assign by Acknowledgement workflow
description: The On-Call: Assign by Acknowledgement workflow is provided with Notify.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Controlling the on-call communication channel with Notify, Using Notify with On-Call Scheduling, Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# On-Call Assign by Acknowledgement workflow

The **On-Call: Assign by Acknowledgement** workflow is provided with Notify.

The workflow uses data from the escalation settings, including overlapping shifts and custom escalation settings, of shifts and rosters. Depending on these escalation settings, the workflow iterates through the defined escalation chain and sends notifications by SMS, email, or voice to users asking them for incident assignment. The workflow respects time-off as specified in the rosters. People who have time-off are not included in the escalation chain and no notifications are sent to them.

When you install both On-Call Scheduling and Notify, the message\_number column is added to the Notify Messages \[notify\_messages\] table to track responses to on-call assignment requests. This column indicates if the contacted user accepted or rejected the assignment. Before you can send notifications, you must define trigger rules. Trigger rules determine the conditions that must be met before a notification is sent and what action must be taken.

**Parent Topic:**[Controlling the on-call communication channel with Notify](c_OnCallNotifyForceCommChannel.md)

