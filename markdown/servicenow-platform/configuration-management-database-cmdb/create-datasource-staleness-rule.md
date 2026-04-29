---
title: Create a data refresh rule
description: Specify data refresh rules to determine if a CI is stale for a specific discovery source. Such CIs can then be updated by a lower-priority authorized discovery source.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Reconciliation rules, Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a data refresh rule

Specify data refresh rules to determine if a CI is stale for a specific discovery source. Such CIs can then be updated by a lower-priority authorized discovery source.

## Before you begin

Role required: sn\_cmdb\_editor and itil have read access, sn\_cmdb\_admin and itil\_admin \(on top\) have full access

## About this task

Data refresh rules are used in conjunction with static reconciliation rules to determine reconciliation steps for a CI. These rules determine if, when, and by which discovery source a CI can be updated. The precedence order of applying reconciliation rules to a class, remains the same even when there are data refresh rules for that same class.

Data refresh rules have no impact when dynamic reconciliation rules are in effect.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to show the CI Classes list and then select the class for which to create a data refresh rule.

3.  In the class navigation bar, expand **Class Info** and then click **Reconciliation Rules**.

4.  Create a rule by selecting **Add** in the Data Refresh Rules section, or select an existing rule to edit. Then fill out the details in the Create Data Refresh Rules dialog box.

<table id="table_ypd_12f_z1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Discovery source

</td><td>

Discovery source for which staleness is evaluated.

</td></tr><tr><td>

Effective Duration

</td><td>

The time period that is used for the staleness test.

 If the fields specified in the static reconciliation rule for the CI's class weren't updated by **Discovery source** within the specified **Effective Duration** — the CI is determined to be stale for **Discovery source** and a lower priority discovery source is authorized to update the CI.

 When set to 0 \(default\), the CI is determined to be stale for **Discovery source** immediately after an update and therefor, a lower priority discovery source will always be authorized to update the CI.

 If you enter a value with a prefix that is valid and a suffix that is not, such as `15 x` — the valid portion of the value is used \('15'\). If the entire value is invalid — the default value of 0 is used.

</td></tr><tr><td>

Active

</td><td>

Activates the rule.

</td></tr></tbody>
</table>5.  Click **Save**.


**Parent Topic:**[Reconciliation rules](../reference/r_ReconciliationRulesPrinciples.md)

**Related topics**  


[Create a CI reconciliation rule](../concept/create-reconciliation-rule.md#)

