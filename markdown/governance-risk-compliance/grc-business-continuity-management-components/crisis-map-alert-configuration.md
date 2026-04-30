---
title: Configure alert rules to display alerts in crisis map
description: Set alert rules to specify conditions under which a feed has to be bubbled up and displayed in the dashboard as an alert. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure search for places in crisis map, Setting up the crisis map, Crisis Management map, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Configure alert rules to display alerts in crisis map

Set alert rules to specify conditions under which a feed has to be bubbled up and displayed in the dashboard as an alert. You can also specify the conditions under which an alert is no longer valid and dismiss it from the dashboard.

## Before you begin

Role required: Administrator

## About this task

Configure an alert to notify the crisis manager of an impending danger, potential harm, or risk that can cause business disruption. Set up filter conditions to notify events or feeds that can happen within a boundary from the location of your assets.

Configuring an alert rule: Define simple conditions to evaluate an alert rule and determine the feed items that generate an alert. These alerts are displayed on the Crisis Management map.

-   **Feed condition filters**

    Use these filter conditions to set your rules for a feed alert. Setting filter conditions help you to filter those alerts that are critical to your business locations from the thousands of feeds that come from the feed resources you have subscribed. Business locations can be corporate offices, employee locations, data centers, suppliers, and others.

    ![Setting up filter for feed condition](../image/AlertTriggerCondition.png "Feed conditions")

-   **Advanced condition script filters**

    Use the advanced rules option to set a filter rule with a condition script. For example, you can set a condition based on the proximity of the crisis to your asset locations. You can also make the rule active.


## Procedure

1.  Navigate to **Threat and Alert Data Feeds** &gt; **Administration** &gt; **Alert Rules**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the alert rule.|
    |Active|Option to set the rule active.|
    |Application|Read-only field. The field helps distinguish items relevant to the crisis map.|
    |Order|Display order of the alert rule. By default it is 100.|
    |Description|Details about the alert.|
    |Create Condition|
    |If Resource Impacted|Option for enabling an alert rule if a resource is impacted.|
    |Advanced|Option for enabling advanced filter rules with a condition script for the alert rule.|
    |Optimize Impact Area|Option to indicate if the map area is to be optimized. Select the check box for optimal performance.|
    |Feed Condition|Conditions to filter alerts based on the set rule.|
    |Advanced Condition Script|This field appears if the **Advanced** option is selected. Enter a script to filter feeds based on a criteria, for example, active alerts.|
    |Dismiss Condition|
    |When Feed Deleted|Option to indicate that the alert must be dismissed from the dashboard, if the feed is deleted.|
    |When Resources Not Impacted|Option to indicate that the alert must be dismissed from the dashboard, if there are no resources impacted.|

4.  Click **Submit**.


**Parent Topic:**[Configure search for places in crisis map](crisis-map-place-api-configuration.md)

