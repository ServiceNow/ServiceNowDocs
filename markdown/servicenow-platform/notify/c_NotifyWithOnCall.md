---
title: Using Notify with On-Call Scheduling
description: When using both Notify and On-Call Scheduling, you can send On-call escalation notifications as SMS messages, in addition to emails.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/notify/c\_NotifyWithOnCall.html
release: zurich
product: Notify
classification: notify
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Notify with On-Call Scheduling

When using both Notify and On-Call Scheduling, you can send On-call escalation notifications as SMS messages, in addition to emails.

Configure the following items to use Notify with On-Call Scheduling:

-   You must add at least one Notify phone number to the On-Call Group number group. This group is configured by default to handle inbound SMS responses \(via On-Call: Check Assignment Response\) that accepts or rejects an on-call assignment and to handle outbound voice calls \(via On-Call: Assign by Acknowledgement Voice\) to accept or reject assignments.
-   You must configure workflows, such as the On-Call: Assign by Acknowledgement to drive escalations via SMS and Voice.

-   **[Set up Notify with On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/notify/t_SetUpNotifyWithOnCall.md)**  
You can configure on-call scheduling to use Notify functionality to send SMS alerts and assign users to tasks based on the SMS responses.
-   **[Controlling the on-call communication channel with Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/notify/c_OnCallNotifyForceCommChannel.md)**  
Configure On-Call Scheduling with Notify to always use a user's preferred communication channel.
-   **[Call a user from the WebRTC UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/notify/t_CallfromWEBRTCUI.md)**  
Make outbound calls and receive a voice call in the browser through the WebRTC interface from On-Call Schedules landing page, Roster and Escalation Details dialog box and on-call calendar.
-   **[Key differences between on-call scheduling with NotifyNow and with Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/notify/r_OnCallNotifyNowNotifyDifferences.md)**  
There are key differences between on-call scheduling with NotifyNow and on-call scheduling with Notify.

**Parent Topic:**[Using Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/notify/using-notify.md)

