---
title: Bind alerts to non-host CIs
description: Bind an incoming event from a discovered application services or alert group to an alert, based on an event rule and the corresponding event field mapping. The event field mapping requires a URL or the port number and corresponding IP address for each service or alert group.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Bind alerts to non-host CIs

Bind an incoming event from a discovered application services or alert group to an alert, based on an event rule and the corresponding event field mapping. The event field mapping requires a URL or the port number and corresponding IP address for each service or alert group.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

If the event is specific to a non-host CI, for example an application services or alert group, use these steps to bind alerts to a non-host CI:

-   Leave the **Node** field empty.
-   Populate the **CI Type** with the CI type you want to bind.
-   Make sure the **additional\_info** field has enough information to uniquely identify the CI. The algorithm matches all **additional\_info** attributes that have the same name as CI fields for that **Event Type**. If the match is successful, the event will be bound to the CI.

Optional method:

-   Leave the **Node** field empty.
-   Populate the **CI Identifier** \(ci\_identifier\) field with attributes, as described above, that uniquely identify the CI.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Select **New** and fill in the appropriate fields of the event rule.

3.  Select the **Binding** tab.

4.  From the **CI type** list, select **cmdb\_ci\_service\_auto**.

5.  In the Event Match Fields section, insert a new row with these parameter values:

    |Field|Value|
    |-----|-----|
    |Field|node|
    |Regular Expression|\(.\*\)|
    |Mapping|temp node|

6.  In the Event Compose Fields section, insert a new row with these parameter value:

    |Field|Value|
    |-----|-----|
    |Field|node|
    |Composition|\(empty\)|

7.  Select **Submit**.

8.  Navigate to **Event Management** &gt; **Rules** &gt; **Event Field Mapping**.

9.  Create the corresponding event field mapping with these parameter values:

    |Field|Value|
    |-----|-----|
    |Source|Specify the event monitor software that generated the event.|
    |Mapping type|Select **Single field**.|
    |From field|Specify `temp node`.|
    |To field|Specify `name`.|

10. In the Transform Value Pairs section, insert new rows for each event mapping pair.

    1.  Set the **Key** with the URL or an IP address with corresponding port value.

    2.  Set the **Value** with the discovered application services, technical service, or alert group name.

    For example, you can add an event mapping pair for each service.

    ![event mapping pair](../image/EMBindServiceCI_2.png)

11. Select **Submit**.


**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

**Related topics**  


[Create event field mappings](t_EMCreateEventFieldMapping2.md)

[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

