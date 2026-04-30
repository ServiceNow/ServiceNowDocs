---
title: Setting up scheduling in Workforce Optimization for Field Service
description: Setting up scheduling enables you to manage events using the team calendar. You can create different types of event categories. Use scripted extension points to customize event types.Create multiple events from the same category and add them to the team calendar with Workforce Optimization for Field Service.Configure and adjust the schedule adherence and conformance formulas using scripted extension points so that you can customize their calculations for your organization.Use extension points to call scripts for event categories such as meeting, time off, or work time.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Workforce Optimization for Field Service, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Setting up scheduling in Workforce Optimization for Field Service

Setting up scheduling enables you to manage events using the team calendar. You can create different types of event categories. Use scripted extension points to customize event types.

Configuring schedule adherence properties enables you to calculate the adherence and conformance of your agents so you can improve the operational efficiency of your organization.

The threshold settings for adherence and conformance indicate how many minutes early or late an agent can clock in or clock out to a scheduled work shift without being considered non-adherent. For more information about the adherence and conformance properties introduced with the Scheduling application, see [Workforce Optimization for Field Service components](../reference/components-wfo-fsm.md).

**Related topics**  


[Scheduling in Workforce Optimization for Field Service](scheduling-wfo-fsm.md)

## Create event types to display on the team calendar with Workforce Optimization for Field Service

Create multiple events from the same category and add them to the team calendar with Workforce Optimization for Field Service.

### Before you begin

Role required: sn\_shift\_planning.admin

### About this task

The following event category configurations are available by default:

-   Work
-   Meeting
-   Training
-   Break
-   Time Off
-   Actual Work
-   Personal

### Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for Field Service** &gt; **Scheduling** &gt; **Event Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

4.  <table id="table_rbj_ymv_1wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the event type.

</td></tr><tr><td>

Category

</td><td>

Type of event, for example, meeting, break, or time off.

</td></tr><tr><td>

Priority Order

</td><td>

Priority of the event type that you want to exclude from the coverage. The higher the number the higher the priority.For example, say you are attending a work event for four hours in a day. You have marked that time window both as time off and as a meeting event type. If time off has a higher order of priority, then the application excludes that event type from coverage.

</td></tr><tr><td>

Color

</td><td>

Color that identifies this type of event in the team calendar.

</td></tr></tbody>
</table>5.  Click **Submit**.


## Modify schedule adherence and conformance formulas by using extension points

Configure and adjust the schedule adherence and conformance formulas using scripted extension points so that you can customize their calculations for your organization.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_shift_planning.ScheduleAdherenceExtPt`.

3.  On the form banner, click the link here to edit the record.

4.  To create your extension point script, click Create Implementation in the related links.

5.  To create your extension point script, click **Create Implementation** in the related links.

6.  Modify the formulas for calculating the schedule adherence and conformance in the `getAdherencePercentage` and `getConformancePercentage` methods.

7.  Click **Update**.


### Result

The schedule adherence and conformance calculations are based on the formulas in the implementation.

## Event type extension point in Workforce Optimization for Field Service

Use extension points to call scripts for event categories such as meeting, time off, or work time.

Use scripted extension points to integrate customizations without altering the core components in the application code. When customizing a base application, you implement the scripted extension points by creating the custom script includes and registering them against the scripted extension points.

You can use extension points to create events such as meeting, training, and time-off requests. For example extension point implementations, see the following extension instances in the Implementations related list:

|Category|Extension Script|
|--------|----------------|
|Meeting|AgentScheduleMeetingEventManager|
|Break|AgentScheduleBreakEventManager|
|Training|AgentScheduleBreakEventManager|
|Time off|AgentScheduleBreakEventManager|
|Work|AgentScheduleWorkEventManager|
|Actual Work|AgentScheduleActualWorkEventManager|
|Personal|AgentSchedulePersonalEventManager|

