---
title: Timing functionality
description: Timing functionality are tools that exist to answer the question "How Long?"Defined metrics can track how long an audited field holds a certain value.Service Level Agreements time how long a task meets a certain condition, and is primarily used to ensure that tasks are handled within a pre-determined time limit.The Task \[task\] table provides a time-tracking field called Time worked. This field measures how long a record has been viewed in order to measure work time on a ticket.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Timeline pages, Viewing record information over time, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Timing functionality

Timing functionality are tools that exist to answer the question "How Long?"

**Parent Topic:**[Timeline pages](c_TimelinePages.md)

**Related topics**  


[Time worked fields](c_TimingFunctionality.md#)

[Time configuration SLAs](c_TimingFunctionality.md#)

[Metric definitions](c_TimingFunctionality.md#)

## Metric definitions

Defined metrics can track how long an audited field holds a certain value.

For instance, a metric can track how long an incident is assigned to an individual, or how long an incident is in the state Active.

See [Metrics](../../../use/reporting/concept/c_MetricDefinitionSupport.md) for more information.

## Time configuration SLAs

Service Level Agreements time how long a task meets a certain condition, and is primarily used to ensure that tasks are handled within a pre-determined time limit.

SLAs define the following conditions:

-   Start Conditions
-   Pause Conditions
-   Stop Conditions

Once a task meets the Start Conditions, the SLA will time how long the task remains in that condition \(unless it meets Pause Conditions\). The timer will end if the Stop Conditions are met. If the time-limit is passed, the SLA will be marked breached.

Notifications can be driven off of the SLA to warn interested parties as the time limit approaches.

## Time worked fields

The Task `[task]` table provides a time-tracking field called **Time worked**. This field measures how long a record has been viewed in order to measure work time on a ticket.

![](../image/TimeTimeworked.png "Time Worked")

Any table that extends Task can use this field. To add the field, [Personalize a form](https://www.servicenow.com/docs/access?context=t_PersonalizeAForm&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

As the record is viewed, the timer counts upward. To pause the timer, click the stop icon \(![Stop icon](../image/TimerStop.png)\)

To resume the timer, click the start icon \(![Start icon](../image/TimerStart.png)\).

When the task is saved, the amount of new time in the timer is used to generate a record on the Time Worked \[`task_time_worked`\] table. This table can be viewed as a related list on the task form.

By default, the time displayed in the **Time worked** field displays a cumulative value stored in the task record. If you modify a Time Worked record, the changes will not be reflected in the task timer.

You can set the property `com.snc.time_worked.update_task_timer` to enable updating of the task timer value based on changes to the time worked records. This is accomplished through the **Update task timer** business rule.

**Note:** Timer fields, such as Time Worked, do not display correctly in Service Portal. For more information and a workaround, see the [Timer fields do not display the correct data in Service Portal \[KB0752404\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0752404) article in the Now Support Knowledge Base.

**Related topics**  


[Timing functionality](c_TimingFunctionality.md#)

