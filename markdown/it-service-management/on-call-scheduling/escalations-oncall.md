---
title: Escalations in On-Call Scheduling
description: An escalation is a mechanism that ensures that important issues are addressed in a timely manner.
locale: en-US
release: australia
product: On-Call Scheduling
classification: on-call-scheduling
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Defining On-Call Scheduling escalation process, On-Call Scheduling, IT Service Management]
---

# Escalations in On-Call Scheduling

An escalation is a mechanism that ensures that important issues are addressed in a timely manner.

On-Call Scheduling monitors response time for a task. You can define the actions to take when a task is not acknowledged. The actions, like sending out an email or an SMS, are fired by trigger rules. You define a trigger rule by specifying the conditions that trigger the actions and the actions to take when the conditions are met.

For example, a critical incident is raised for Acme Pharmaceuticals regarding a problem with their network access. An SMS task notification is sent to Ken, the third-line support engineer who is on call for this type of incident. Ken is unavailable, however, and does not respond within the specified 30-minute response time.

A trigger rule that is defined for Acme Pharmaceuticals critical incidents starts an escalation if a task goes 30 minutes without a response. The person specified as the next point-of-contact is Nakul, Ken's line manager, so an SMS notification is sent to Nakul. Settings in the escalation policy specify how many notifications to send, how long to wait, and so on.

Shift administrators and shift managers can define trigger rules and configure escalation policies.

**Note:** If an escalation trigger rule is defined for the On-Call: Conference Call Escalation workflow, then the time between reminders is set to 60 seconds irrespective of the **Time between reminders** field value in the associated escalation policy.

For information about escalation policy, see [Create an escalation policy](../task/create-custom-esc-policy-oncall.md).

For information about escalation trigger rule, see [Create an escalation trigger rule](../task/create-trigger-rule-oncall.md).

-   **[Designing an escalation process](designing-escalation-process-oncall.md)**  
To design an escalation process for a task, you define a trigger rule and configure one or more escalation policies.
-   **[Track the progress of an escalation](../task/track-escalation-progress-oncall.md)**  
Use the On-Call Escalation Tracking page for full visibility into the time line of an active or closed escalation as it progresses through its on-call escalation path.
-   **[View details in an escalation log](../task/view-escalation-logs-oncall.md)**  
View the escalation log record for full details on the time line and actions for an on-call escalation as it progressed through the on-call escalation path. You can also access escalation and escalation notification information from reports.

**Parent Topic:**[Defining On-Call Scheduling escalation process](../../user-administration/concept/defining-escalation-process-and-template.md)

**Related topics**  


[Legacy: Viewing Escalation Overview reports](viewing-esc-oview-report-oncall.md)

[Legacy: Viewing the Performance reports for escalations](viewing-performance-report-oncall.md)

