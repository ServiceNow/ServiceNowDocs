---
title: Configure approval rules for Exception Management in Configuration Compliance
description: Use the flow designer to approve exception requests for exception management, and exception rules. If you are deploying Configuration Compliance for the first time, the flow designer is enabled by default.
locale: en-US
release: yokohama
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configure approval rules for Exception Management in Configuration Compliance

Use the flow designer to approve exception requests for exception management, and exception rules. If you are deploying Configuration Compliance for the first time, the flow designer is enabled by default.

## Before you begin

Role required: sn\_vulc.admin

## About this task

If you are an existing Configuration Compliance user, the default option is workflow.

The value of the system property **sn\_vulc.flow\_designer\_activation** is set to true. This means that the flow designer is activated by default.

**Note:** You cannot revert to using the workflow after activating the flow designer. For a detailed comparison between the workflow and flow designer, see [Exception management workflow versus flow designer in Configuration Compliance](../reference/cc-ex-mgt-flow-designer-vs-workflow.md).

To use the flow designer, create rules using the Approval Rules module. Using this module, you can configure approval rules for each of the following exception management workflows.

-   Exception approval rules for remediation task
-   Approval rule for auto-exception rules

**Note:** You can also define conditions containing multiple levels of approval within a rule. The flow designer automatically inherits the rules created in this module and processes the matching approval workflow. For information on configuring approval levels, see [Create approval levels for Exception Management in Configuration Compliance](cc-exception-mgt-config-approval-rule.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Approval Rules** &gt; **Exception approval rules for Remediation Task**.

2.  On the Approval Rules page, select the group for which you want to set the approval rule.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Approval configuration name.|
    |Table|Table on which the rule is applied.|
    |Application|Default value is Configuration Compliance.|
    |Rule type|Specifies the rule type. For example, exception management, or exception rule.|
    |Active|Enabled by default, signifying that the approval rule is in use.|
    |Description|Short description of the approval rules.|
    |Approval expiry \(days\)|Date until when the approver can approve the request.|
    |Notify approver \(days\)|Date after which the approver is notified to take action.|

4.  Select **Update**.

    In the Approval Configurations tab, there are two levels of approvers set up by default. You can select a rule to define the conditions based on different use cases within a rule. For more information, see [Create configurations for an approval rule in Configuration Compliance](cc-exception-mgt-approval-config.md) .

    **Note:** In each configuration page, you can create multiple approval levels. For more information, see [Create approval levels for Exception Management in Configuration Compliance](cc-exception-mgt-config-approval-rule.md) .


## Example

Based on different use cases, you can define different approval processes for the same test results found on different remediation tasks.

