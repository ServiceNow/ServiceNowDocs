---
title: Set an inactivity monitor
description: You can set an inactivity monitor that triggers an event for a task record when the task has been inactive for a certain amount of time.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Event scheduling, System scheduler, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Set an inactivity monitor

You can set an inactivity monitor that triggers an event for a task record when the task has been inactive for a certain amount of time.

## Before you begin

Role required: system\_scheduler\_admin

## About this task

If the task remains inactive, the monitor repeats at regular intervals. User updates to the task record restart the monitor. If reset conditions you defined for it have not been met, the monitor does not restart when you update the task record. Inactivity monitors only apply to records on tables that extend the `Task` table, or the `Task` table itself.

When an inactivity monitor triggers, it generates an event in the form `<tablename>.inactivity` \(for example, `incident.inactivity`\). Define an [Email and SMS notifications](../../notification/concept/c_EmailNotifications.md) or script action to drive further action for the inactivity monitor.

A record's activity is only based on user updates. System updates do not count as activity.

Inactivity monitors only support one matching inactivity monitor per task.

If multiple inactivity monitors do match a task record, one of the inactivity monitors will delete all other sys\_trigger jobs, leaving only its own, preventing the others from triggering. Since inactivity monitors are driven by condition builder, the definition time can't identify inactivity monitors from intersecting with each other per task record.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **SLA** &gt; **Inactivity Monitors** and click **New**.

2.  Give the inactivity monitor a name.

3.  Specify the type of record to monitor in the **Table** field.

4.  Specify how long the inactivity monitor should wait before sending each notification in the **Wait** field.

5.  Specify any additional conditions in the **Condition** field.

    At least one condition must be specified for the inactivity monitor to work.

    -   If you are using incident auto-close, add a Reset condition because, if you don't, auto-close won't work properly. To prevent this reset, set a **Reset Condition** on your inactivity monitor. To learn more about Incident auto-close, see Configure incidents to close automatically.
    -   All conditions need to be True per user update for the Inactivity Monitor to start running. For example, Set this condition only works if the due date is earlier than the current date when user updates the task.
6.  Specify an Order if multiple inactivity monitors might have their conditions met for a given record - the one with the lowest order is used.

7.  Click **Save**.

    **Note:** If you change conditions on an inactivity monitor, the monitor stops tracking previously tracked records. It does not track records that you created before the inactivity monitor, even if the record meets all other conditions.


-   **[Escalation intervals and pause conditions](../concept/c_EscalationIntervsAndPauseConds.md)**  
Escalation Intervals and Pause Conditions are not relevant to an inactivity monitor.

**Parent Topic:**[Event scheduling](../concept/c_ScheduleEvents.md)

**Related topics**  


[Event registry](../../platform-events/reference/r_EventRegistry.md)

