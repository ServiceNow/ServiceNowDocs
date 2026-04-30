---
title: Alert correlation rule form
description: Manage the fields that define how alerts are correlated and grouped.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert correlation rule form

Manage the fields that define how alerts are correlated and grouped.

<table id="table_v22_jmg_s5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the correlation rule.

</td></tr><tr><td>

Order

</td><td>

The evaluation priority for the rule. Rules with lower numerical values are given higher priority. An alert is evaluated against each alert action rule until a match is found.For example, if you have two alert correlation rules with priorities 10 and 20, respectively, the rule with priority 10 will be evaluated first. If an alert matches the criteria of the rule with priority 10, no further rules will be checked. If it doesn’t match, the alert will then be evaluated against the rule with priority 20.

</td></tr><tr><td>

Active

</td><td>

Option to activate or deactivate the rule.

</td></tr><tr><td>

Advanced

</td><td>

Option to switch to advanced mode, which lets you use custom scripts to define your own logic. The sample correlation rule, **Alert correlation rule SAMPLE**, is provided out-of-the-box for reference. You can use the available script as a guide.**Note:** The **Filter** condition specifies which alerts the rule will apply to. Ensure that the same condition is used in the advanced script to identify alerts to be included in the group.

</td></tr><tr><td>

Description

</td><td>

Description of the rule.

</td></tr><tr><td>

Primary Alert

</td><td>

The filter condition to identify the alert that is the primary alert, or most important alert, in a set of related alerts. This field does not appear when **Advanced** is selected.

</td></tr><tr><td>

Secondary Alert

</td><td>

The filter condition to identify the alert that is related to the primary alert, however it is of lesser importance.This field does not appear when **Advanced** is selected.

</td></tr><tr><td>

Filter

</td><td>

The filter condition to identify the alert on which the script is run. **Filter** is available only when **Advanced** is selected.

 Filter parameters are case sensitive by default. To disable case sensitivity, set the **sa\_analytics.correlation\_case\_sensitive** parameter to **false**.

</td></tr><tr><td>

Relationship Type

</td><td>

Specify the type of relationship between the primary and secondary alert:-   **No Relationship**: Ignore the relationship when looking for a match.
-   **Same CI or Node**: Relate both alerts with the same CI. If the CI field is blank, the alerts must have the same Node value.
-   **Primary is Parent**: Relate the alerts where the primary alert is the parent in a parent-child relationship, as described in the CI Relationship Types table \[cmdb\_rel\_ci\].
-   **Primary is Child**: Relate the alerts where the primary alert is the child in a child-parent relationship, as described in the CI Relationships table \[cmdb\_rel\_ci\].

 This field does not appear when the **Advanced** check box is selected.

</td></tr><tr><td>

Time Difference in Minutes

</td><td>

The minutes between which the primary and secondary event must occur to match this rule. The default value is 60 minutes.**Note:** The value for this entry cannot exceed 1440 minutes \(one day\).

 This field does not appear when **Advanced** is selected.

</td></tr><tr><td>

Script

</td><td>

Custom script that you can modify to return a JSON string that specifies the primary and secondary alerts. Select **Advanced** to display the script field.

 ```

(/* The function needs to return a JSON- {correlationType:[correlatedAlerts]}
 for example: if your filter matches the alert, set the alert as the primary alert and set alerts 1, 2 and 3 each as secondary alerts.
 
 You can use both multiple primary alerts and multiple secondary alerts.
 The correlationType can be PRIMARY or SECONDARY, and the alerts ID must be in an array. 
 CurrentAlert is the GlideRecord of the currentAlert on which that rule runs.  
 The system supports only one primary per alert, so: 
   Do not correlate more than one alert under the PRIMARY array. 
   Do not correlate alerts that already have a primary under the SECONDARY array. 
  The system supports open alerts only, so do not correlate alerts that have been closed under either one of the arrays. 
  */
 
 (function findCorrelatedAlerts(currentAlert){
 
       var result = {};   //Insert your code here
       result = {'SECONDARY':['alertID1','alertID2','alertID3']};         
       return JSON.stringify(result);  
 
 })(currentAlert);

```

</td></tr><tr><td>

Relationship

</td><td>

Description of the CI relationship between primary and secondary, for example, *Allocated from::Allocated to* or *Allocated to::Allocated from*. This field displays only if either **Primary is Parent** or **Primary is Child** is selected for the **Relationship Type**.

 ![Relationship](../image/alert-relationship-type.png)

This field does not appear when **Advanced** is selected.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

