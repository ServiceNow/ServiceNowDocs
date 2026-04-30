---
title: Create configurations for an approval rule in Configuration Compliance
description: Define the conditions to filter out matching remediation tasks for an approval level.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure approval rules for Exception Management in Configuration Compliance, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create configurations for an approval rule in Configuration Compliance

Define the conditions to filter out matching remediation tasks for an approval level.

## Before you begin

Role required: sn\_vulc.admin

## About this task

In the Approval Configurations module, you can configure multiple levels of approval for different configurations. Define condition-based rules, with each rule containing multiple levels of approval.

**Note:** Use the Approval rules module to configure approval rules for the exception management workflows. For information on configuring approval rules, see [Create approval levels for Exception Management in Configuration Compliance](cc-exception-mgt-config-approval-rule.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Approval Rules**.

2.  Select an approval rule and navigate to the **Approval Configurations** tab.

3.  Select a configuration.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Approval configuration name.|
    |Approval rule|Contains the table and type details for the approval rule.|
    |Order|Execution order of various configurations within a rule. For example, a configuration with an order entry of 100 is run before a configuration with an order entry of 200.|
    |Active|Enabled by default, signifying that the approval configuration is in use.|
    |Description|Short description of the approval configuration levels.|

5.  Set a condition for the test results or remediation tasks in one of the following ways:

<table id="table_q1y_hks_gbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition

</td><td>

Identifies the matching test results or remediation tasks.

</td></tr><tr><td>

Advanced condition

</td><td>

Script that defines the condition for the test results or remediation tasks.**Note:** This field appears when you select the **Advanced** check box.

</td></tr></tbody>
</table>6.  Select **Update**.

    You can define conditions containing multiple levels of approval within a rule. The flow designer automatically inherits the rules created in this module and processes the matching approval workflow. For information on configuring approval levels, see [Create approval levels for Exception Management in Configuration Compliance](cc-exception-mgt-config-approval-rule.md).


## Example

You can define different approval paths for different types of remediation tasks.

