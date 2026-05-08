---
title: Create or edit an event rule
description: You can create event rules to generate alerts for tracking and remediation. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to general rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create or edit an event rule

You can create event rules to generate alerts for tracking and remediation. Use team-based integrations in event rules to make sure that connector ownership and execution of rules give precedence to general rules. Teams can maintain consistency and hierarchy while offering flexibility and customization options.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

View the list of available event rules on the **Event Rules** page to determine whether you want to create or edit an event rule.

You can create rules that:

-   Transform information in events to populate specified alert field values and compose alert fields from various values.
-   Configure threshold rules that create or close alerts only when the incoming matching events exceed the specified threshold.
-   Bind alerts to CIs using CI identifiers.

Options to create the rule are:

-   Create an event rule and assign event fields for alert generation.
-   Create a rule from an existing event or group of events that don’t have a rule. In this case, the event fields are copied to the Event Match Fields section of the rule.
-   Edit an existing event rule.
-   For Team-based integrations, select an assignment group.
-   Run multiple sequential rules defined for the same event by selecting the **Apply additional matching rules** check box. The event rules run in ascending order as defined in the **Order** field. Event rules applied to assignment groups only run after the global rules have run.


You can refresh an existing event rule with new event data. For more information see, [Refresh event rules](refresh-event-rule.md).

**Note:**

-   Event rules that aren’t configured to perform any action are skipped. Therefore, if the rule isn’t configured as ignore, threshold, or binding, it’s important to specify either the match or the composed fields.
-   Make sure that you don’t change the **Classification** field value in event \[em\_event\] tables, either manually, by script, or by event rule.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules** and take one of the following actions.

<table id="choicetable_u5d_w1m_zt"><tbody><tr><td id="d543683e154">

**Create an event rule from an existing event**

</td><td>

1.  Select the link for unassociated events or grouped events that aren’t mapped to the rules.

![Example wording of the link: "There are 2 recommended rules, created out of 7 unassociated events of the most recent 50000 events."](../image/EventManagementEventRuleSimple.png)

2.  Select the event that you want to use for creating the rule.

The event fields are copied to the Event Field Rules section of the rule.

</td></tr><tr><td id="d543683e182">

**Edit an existing event rule**

</td><td>

In the event rule list, select the required event rule to be modified. The event rule opens in the event rule designer where you can modify the values of the fields. Select **Save and Upgrade** ![Event Management save](../image/event-rule-save-and-upgrade.png) to modify the rule when the following banner message appears and you want to convert the event rule.

```
Rule cannot be viewed in the
          event rule designer. To modify the rule click 'Save and Upgrade'.
```

</td></tr><tr><td id="d543683e206">

**Create an event rule**

</td><td>

Select **New**.

</td></tr></tbody>
</table>2.  Ensure that **Active** ![Active toggle](../image/active-toggle.png) is selected.

    When the rule is deactivated, Event Management finds and applies another event rule. An alert is still created for the event unless **Ignore** is selected in another applicable rule or when configuring the filter for this event rule.

3.  Enter a unique and meaningful name and fill in the form.

<table id="table_zdm_zwc_sy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Category to which this matching rule applies. The mapping rule only applies to events with the same event class value. If this value is empty, apply the rule to all events.

</td></tr><tr><td>

Order

</td><td>

Order in which an event rule is evaluated when multiple rules are defined for the same type of event. Event rules are evaluated in ascending order.

</td></tr><tr><td>

Description

</td><td>

Type additional information that describes the event rule.

</td></tr><tr><td>

Apply additional matching rules

</td><td>

Select to apply additional event matching rules according to the Order field. The last rule with binding settings sets the CI binding. When selected, the Thresholds tab is inactive.

</td></tr><tr><td>

Assignment group

</td><td>

For team-based integrations, select an assignment group. If no assignment group is defined in the event rule, then this event rule is considered as a global rule.

When the rules are running – first the global rules run and then the rules that belong to the assignment group that the event’s source instance belongs to.

</td></tr></tbody>
</table>4.  Define the event rule using these Event Rule Designer features.

<table id="choicetable_n2q_nks_sy"><tbody><tr><td id="d543683e336">

**Event Filter**

</td><td>

Define a filter to restrict to which events the event rule must apply. See [Filter the events that an event rule applies to](t_EMCreateFilter.md).

</td></tr><tr><td id="d543683e352">

**Transform and compose alert output**

</td><td>

Configure the customization of alert content. See [Configure an event rule to customize alert content](t_EMComposeOuput.md).

</td></tr><tr><td id="d543683e371">

**Threshold**

</td><td>

Create or close alerts according to the specified threshold. See [Set a threshold to suppress alert generation](t_EMISetThresholdEvent.md).

</td></tr><tr><td id="d543683e390">

**Binding**

</td><td>

Configure event rules to automatically bind alerts to CI information from the CMDB. See [Binding alerts to CIs](../concept/ci-binding-alert.md).

</td></tr></tbody>
</table>5.  Select **Save**, **Submit**, or **Update**.


**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[Pattern matching](https://www.servicenow.com/docs/access?context=c_PatternMatching&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Use event input information](../concept/event-input-information.md)

[Configure an event rule to customize alert content](t_EMComposeOuput.md)

[Refresh event rules](refresh-event-rule.md)

[Simulate event processing](simulate-event-processing.md)

[Filter the events that an event rule applies to](t_EMCreateFilter.md)

