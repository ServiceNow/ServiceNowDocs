---
title: Alert Rules form
description: Use the Alert Rules form in BCM UIB Workspace to add details about the alert rules.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure alert rules, Setup for Crisis map, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Alert Rules form

Use the Alert Rules form in BCM UIB Workspace to add details about the alert rules.

For the description of the field values, see the table.

<table id="table_jjj_bmp_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the alert rule.

</td></tr><tr><td>

Order

</td><td>

Display order of the alert rule. By default, it is 100.

</td></tr><tr><td>

Application

</td><td>

Read-only field. The field helps distinguish items relevant to the Crisis map.

</td></tr><tr><td>

Category

</td><td>

Category of the record. The value is **BCM**. It helps to identify the BCM-related resources when multiple applications use the component.

</td></tr><tr><td>

Active

</td><td>

Option to set the rule active.

</td></tr><tr><td>

Description

</td><td>

Details about the alert.

</td></tr><tr><td class="sub-head" colspan="2">

Create Condition

</td></tr><tr><td>

If Resource Impacted

</td><td>

Option for enabling an alert rule if a resource is impacted. When this option is selected, alerts are created only for resources within the feed's impacted area.

</td></tr><tr><td>

Advanced

</td><td>

Option for enabling advanced filter rules with a condition script for the alert rule. Use the advanced condition script as shown in the example.

![Condition script.](../image/alert-rule-create-condition.png)Enabling ECMAScript 2021 \(ES12\) mode allows you to use the latest JavaScript features supported in the script. Disabling it restricts you to the features supported by the application's default JavaScript mode.

</td></tr><tr><td>

Optimize Impact Area

</td><td>

Select this check box to enable optimization for improved performance. When enabled, the feed impact area is optimized for better performance.

</td></tr><tr><td>

Stop On First Match

</td><td>

Option to stop the condition on the first match of the rule. Once a condition or pattern is met, the system stops further evaluation or processing, and the action associated with that first successful match is executed.

</td></tr><tr><td>

Feed Condition

</td><td>

Conditions to filter alerts based on the set rule. Use these filter conditions to set your rules for a feed alert. Setting filter conditions help you to filter those alerts that are critical to your business locations from the thousands of feeds that come from the feed resources you have subscribed. Business locations can be corporate offices, employee locations, datacenters, suppliers, and others.

![Setting up filter for feed condition](../image/AlertTriggerCondition.png "Feed conditions")

</td></tr><tr><td>

Advanced Condition Script

</td><td>

Configuration for Advanced Condition Script. This field appears if the **Advanced** option is selected. Enter a script to filter feeds based on a criteria, for example, active alerts. Use the advanced rules option to set a filter rule with a condition script. For example, you can set a condition based on the proximity of the crisis to your asset locations. You can also make the rule active.

</td></tr><tr><td class="sub-head" colspan="2">

Dismiss Condition

</td></tr><tr><td>

When Feed Deleted

</td><td>

Option to indicate that the alert must be dismissed from the dashboard, if the feed is deleted.

</td></tr><tr><td>

Advanced

</td><td>

Option for enabling advanced filter rules with a condition script for the alert rule.

</td></tr><tr><td>

When Resources Not Impacted

</td><td>

Option to indicate that the alert must be dismissed from the dashboard, if there are no resources impacted.

</td></tr><tr><td>

Feed Condition

</td><td>

Conditions to filter alerts based on the set rule.

</td></tr><tr><td>

Advanced Condition Script

</td><td>

Configuration for Advanced Condition Script. This field appears if the **Advanced** option is selected. Enter a script to filter feeds based on a criteria, for example, active alerts.

</td></tr></tbody>
</table>**Parent Topic:**[Configure alert rules](../task/conf-alert-rule-uib-ws.md)

