---
title: Key differences between on-call scheduling with NotifyNow and with Notify
description: There are key differences between on-call scheduling with NotifyNow and on-call scheduling with Notify.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/notify/r\_OnCallNotifyNowNotifyDifferences.html
release: yokohama
product: Notify
classification: notify
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Notify with On-Call Scheduling, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Key differences between on-call scheduling with NotifyNow and with Notify

There are key differences between on-call scheduling with NotifyNow and on-call scheduling with Notify.

## Tracking responses to questions

The On call:Assign by Acknowledgement workflow no longer uses the Notify Question tables to track assignment responses. When you install On-Call Scheduling with Notify, the message\_number column is added to the Notify Messages \[notify\_messages\] table to track responses to on-call assignment requests. This column indicates if the contacted user accepted or rejected the assignment.

**Parent Topic:**[Using Notify with On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/notify/c_NotifyWithOnCall.md)

**Related topics**  


[Set up Notify with On-Call Scheduling]()

[Controlling the on-call communication channel with Notify]()

[Call a user from the WebRTC UI]()

