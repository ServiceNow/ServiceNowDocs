---
title: Bind alerts to CIs using event field mapping
description: Instead of creating separate event rules for each CI you want to bind to an alert, you can use event field mapping to bind an alert to multiple event CIs.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Bind alerts to CIs using event field mapping

Instead of creating separate event rules for each CI you want to bind to an alert, you can use event field mapping to bind an alert to multiple event CIs.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

2.  On the **Event Field Mapping** page, fill in the fields as follows:

    |Field|Description|
    |-----|-----------|
    |Name|Event field mapping name.|
    |Source|Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.|
    |Order|Number to define the order in which this action should be processed. Actions with lower numbers are processed first.|
    |Mapping type|Select **Single field**.|
    |From field|The field name of the value to replace, taken either from the event's **Event** field or **Additional info** field.|
    |To field|Enter **ci\_type**.|
    |Active|Select to activate the event field mapping.|

3.  In the **Transform Value Pairs** section, insert the following:

    |Field|Description|
    |-----|-----------|
    |Key|The values of the field specified in the **From field** field. Enter a separate entry for each value.|
    |Value|The ci type to which you want to bind the alert.|


## Example

Following is an example of event field mapping which binds the value of the **Ethernet** field in an alert to the CI **dscy\_switchport**:

![Bind alert to CI](../image/event-field-mapping-ci-type.png)

**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

**Related topics**  


[Create event field mappings](t_EMCreateEventFieldMapping2.md)

