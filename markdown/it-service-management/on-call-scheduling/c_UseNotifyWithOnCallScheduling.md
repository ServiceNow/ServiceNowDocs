---
title: Setting up SMS and voice messaging as contact methods
description: To send On-call escalation notifications as SMS or voice messages, you must configure Notify.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring On-Call Scheduling, On-Call Scheduling, IT Service Management]
---

# Setting up SMS and voice messaging as contact methods

To send On-call escalation notifications as SMS or voice messages, you must configure Notify.

Configure the following items to use Notify with On-Call Scheduling:

-   You must add at least one Notify phone number to the On-Call Group number group. This group is configured by default to handle inbound SMS responses \(via On-Call: Check Assignment Response\) that accepts or rejects an on-call assignment and to handle outbound voice calls \(via On-Call: Assign by Acknowledgement Voice\) to accept or reject assignments.
-   You must configure workflows, such as the On-Call: Assign by Acknowledgement to drive escalations via SMS and Voice.

To set up SMS and voice message as contact methods, see Set up Notify with On-Call Scheduling

**Parent Topic:**[Configuring On-Call Scheduling](configuration.md)

**Related topics**  


[bundle-platcap.c_OnCallAssignByAckWorkflow]

[bundle-platcap.c_OnCallNotifyForceCommChannel]

