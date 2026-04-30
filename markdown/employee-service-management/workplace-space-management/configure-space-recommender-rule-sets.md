---
title: Configure a Space Recommender Rule set
description: Create a space recommender rule set consisting multiple rules. The rule set calculates the qualifying spaces when a user submits a space assistance request using the Workplace Service Portal. You must have Workplace Central plugin.
locale: en-US
release: zurich
product: Workplace Space Management
classification: workplace-space-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a Space Recommender rule, Manage, Workplace Space Management, Workplace Service Delivery, Employee Service Management]
---

# Configure a Space Recommender Rule set

Create a space recommender rule set consisting multiple rules. The rule set calculates the qualifying spaces when a user submits a space assistance request using the Workplace Service Portal. You must have Workplace Central plugin.

## Before you begin

Ensure the following:

-   Workplace Central plugin is installed.
-   Workplace Case Management is installed.
-   Workplace Core is installed.

Role required: sn\_wsd\_core.admin

## About this task

The Space Recommender Rule Set is a collection of space recommender rules based on which the spaces are qualified. By default, the **Space Recommendations Default Rule Set** is used to result qualifying spaces when a space assistance request is submitted.

If you are creating a new rule set, in order for the exact match action to work on the space assistance request, the rules that you add in the new rule set must also have the rules that are added in the **Space Recommendations Default Rule Set**. The **Rule type** of the rules must be **Advanced script**. You can refer to existing default rule set for more information on how the advanced script is configured to work with the exact match action.

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Space Recommender Rule sets**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Rule Set Name|Name of the rule set.|
    |Description|Description of the rule set.|
    |Result Configuration|Option to specify based on which location level the resultant spaces must be displayed. Specify whether spaces of same floor, same building or same campus must be displayed.|
    |Active|Option to activate the rule set.|
    |Order|Order of implementation. The rule set with the lowest order is applied.|
    |Condition table|Table on which you want to apply the conditions. By default, the Workplace Case table is selected.|
    |Condition|Conditions that you want to apply on the selected **Condition table**. To add conditions, select **New Criteria**.|

4.  Click **Submit**.


## Result

The Space Recommender Rule set is created.

## What to do next

[Create a Space Recommender rule](create-a-space-recommender-rule.md)

**Parent Topic:**[Create a Space Recommender rule](create-a-space-recommender-rule.md)

