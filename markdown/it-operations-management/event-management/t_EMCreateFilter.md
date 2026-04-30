---
title: Filter the events that an event rule applies to
description: Define a filter to restrict to which events the event rule must apply. Configure the filter by providing a set of conditions that each event must match to be either excluded or included from applying to the event rule.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Filter the events that an event rule applies to

Define a filter to restrict to which events the event rule must apply. Configure the filter by providing a set of conditions that each event must match to be either excluded or included from applying to the event rule.

## Before you begin

Ensure that a name is specified for the event rule.

Role required: evt\_mgmt\_admin

## About this task

To construct the required condition statement, you can use event fields as well as additional fields that are defined in the **Additional Information** field of the event. Use these fields to configure conditions that can exclude events. Alternatively, you can filter incoming events to ensure that only those events that meet the required conditions are included.

**Note:** Event rules filter is case-sensitive.

While working in the Event Filter tab:

-   In the Event rule list, if you selected a recommended rule or an existing rule, the filter fields are populated with values from these events. You can use these filter fields to compose filter conditions.
-   You can click another tab \(for example, **Threshold**\), work in that area and then return to work in the Event Filter area without losing information.
-   Use the right-panel as a source of reference for which fields are available to be used when composing filter conditions.

**Note:** Event filters created on additional\_info fields only perform a string comparison and not a numeric comparison, even if the information entered into the value field appears as if it is numeric, as depicted in the following graphic:

![Event filter string comparison](../image/event-rule-string-comparison.png)

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Click **New** or open an event rule.

3.  Click **Event Filter**.

    ![Event Management filter](../image/event-rule-filter.png)

4.  To ignore events, select **Ignore events that match this filter**.

    All events that match this event rule are ignored. You can add more conditions to the filter by clicking either **OR** or **AND**.

    **Note:** Even if an event is ignored by an event rule, the event is still recorded in the Event \[em\_event\] table. Select this option to inhibit an alert from being created and be associated with the event.

5.  To configure conditions to which the event rule must apply, click **New Criteria**.

    You can add further conditions by clicking either **OR** or **AND**.

    **Note:** The **%** character is not supported in filter conditions.

6.  You can add field names to the Event Rule Simple Field Black Lists \[em\_event\_rule\_black\_list\] table to either show or hide fields from the filter.

    ![Event rule exclusion list](../image/event-rule-black-list.png)

    -   To remove fields from the filter and the right panel, add a new black list field with **Show in rule** not selected.
    -   To remove fields only from the filter and still enable it to appear in the right panel, add an exclusion list field with **Show in rule** selected.
7.  Click either **Save** or **Submit**.


## Example

Example showing filter conditions that are specified to run a rule when the metric name starts with the word "disk". For this example, any resource is acceptable, as long as it is not "cpu" and the node name is "MyServer". ![Event Management filter](../image/event-rule-filter-example.png)

Example to filter events using time conditions. In the **Select Field or add New** field, select `Time of event`.

Specify the required time conditions, for example, anytime after yesterday.

![Event rule time condition](../image/event-rule-time-condition.png)

**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[Create or edit an event rule](create-or-edit-event-rule.md)

[Use event input information](../concept/event-input-information.md)

[Configure an event rule to customize alert content](t_EMComposeOuput.md)

[Set a threshold to suppress alert generation](t_EMISetThresholdEvent.md)

