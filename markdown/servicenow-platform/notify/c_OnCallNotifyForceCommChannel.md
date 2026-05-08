---
title: Controlling the on-call communication channel with Notify
description: Configure On-Call Scheduling with Notify to always use a user's preferred communication channel.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Notify with On-Call Scheduling, Using Notify, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Controlling the on-call communication channel with Notify

Configure On-Call Scheduling with Notify to always use a user's preferred communication channel.

If **Force communication channel** is specified in the **Escalation settings** for rosters, the preferred user device is used: SMS, voice, or email.

For example, if the preferred device is SMS and the on-call member does not have an SMS device defined, the user is not contacted even if the user has an email address. When forcing a communication channel on an escalation level does not succeed, no further communication attempts are made. The fact that the user could not be reached is logged.

-   **[On-Call Assign by Acknowledgement workflow](c_OnCallAssignByAckWorkflow.md)**  
The **On-Call: Assign by Acknowledgement** workflow is provided with Notify.

**Parent Topic:**[Using Notify with On-Call Scheduling](c_NotifyWithOnCall.md)

**Related topics**  


[Set up Notify with On-Call Scheduling](../task/t_SetUpNotifyWithOnCall.md)

[Call a user from the WebRTC UI](../task/t_CallfromWEBRTCUI.md)

[Key differences between on-call scheduling with NotifyNow and with Notify](../reference/r_OnCallNotifyNowNotifyDifferences.md)

[bundle-platadm.c_SubscriptionBasedNotifications]

