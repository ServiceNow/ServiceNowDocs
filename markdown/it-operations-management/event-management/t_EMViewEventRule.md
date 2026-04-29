---
title: View event rules
description: You can view all event rules on the Event Rules list.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View event rules

You can view all event rules on the Event Rules list.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

<table><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The event rule name.

</td></tr><tr><td>

Override default binding

</td><td>

Legacy binding criteria. If, in the **Bind** section criteria have not been specified or if the specified bind criteria are not matched, then the legacy binding criteria are considered.

</td></tr><tr><td>

Order

</td><td>

Order in which an event rule is evaluated when multiple rules are defined for the same type of event. Event rules are evaluated in ascending order.

</td></tr><tr><td>

Source

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Updated

</td><td>

Update date and time for the rule.

</td></tr></tbody>
</table>    **Note:** You can filter the Event Rule list to display the required subset of the information. However, if you create a favorite link after filtering, when the link is clicked the Event Rule list does not display the correct filter.


**Parent Topic:**[Event rules](../concept/create-event-rules.md)

**Related topics**  


[View events](t_EMManageEvent.md)

