---
title: Create approval rules
description: Define rules for approval workflows. An approval rule identifies the functional approver for the workflow, such as a Finance Manager or Operations Manager. The rule also associates approvers with the appropriate approval trigger conditions, and defines escalation details for reassiging an approvals to another approver for the rule, when the original approver can't action on the approval step for this rule.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-26"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create approval rules

Define rules for approval workflows. An approval rule identifies the functional approver for the workflow, such as a Finance Manager or Operations Manager. The rule also associates approvers with the appropriate approval trigger conditions, and defines escalation details for reassiging an approvals to another approver for the rule, when the original approver can't action on the approval step for this rule.

## Before you begin

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin or sn\_adv\_appr\_mgmt.approval\_rule\_writer

**Note:** To use the **Advanced rule** option to define the functional approver using a script, you must have the admin role.

## About this task

Approval rules define the approvers for the rule, associate the trigger conditions to the rule, and provide escalation rules for the rule if escalations are enabled in your configuration. The escalation feature enables you to reassign an approval request to another approver when the original approver does not approve or reject a request within a timeframe that you define.

**Note:** If you have the admin role, you can use a script to identify the functional approver for the rule. For details, see the [Create Approval Rule form](../reference/create-approval-rule-form.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **Approval Rules**.

4.  Select **New**.

5.  On the Create New Approval Rule form, fill in the fields.

    For field descriptions, see [Create Approval Rule form](../reference/create-approval-rule-form.md).

6.  Select **Save**.


## Result

The approval rule, when used in an approval workflow, is depicted as a step \(card\) in the workflow interface. The card provides details of the rule and approvers in the approval step. You can also review the steps in an approval configuration by navigating to **Advanced Approvals** &gt; **Approval Steps** in the workspace.

## What to do next

[Create approval chains](create-approval-chain.md) \(optional\).

