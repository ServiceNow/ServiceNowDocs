---
title: Create conditions that trigger approval workflows
description: Define one or more conditions that apply company policies, such as legal guidelines or pricing rules, to trigger an approval workflow. Also enable the smart reapprovals feature, which allows previous approvals to be used for a resubmitted approval.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create conditions that trigger approval workflows

Define one or more conditions that apply company policies, such as legal guidelines or pricing rules, to trigger an approval workflow. Also enable the smart reapprovals feature, which allows previous approvals to be used for a resubmitted approval.

## Before you begin

Before creating conditions, consider the business thresholds that determine when an approval is required, such as a certain discount percentage for quote line items or a minimum deal size amount.

Verify that you have the associated items \(fields\) that represent the business thresholds in the entity table for the approval configuration, such as the Quote \[sn\_quote\_mgmt\_core\_quote\] table or through dynamic attributes defined in a Dynamic Schema. For more information on dynamic attributes, see Dynamic Schema.

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin, sn\_adv\_appr\_mgmt.approval\_rule\_writer

**Note:** If you have the admin role, you can use scripts to specify approval conditions if the **Advanced condition** option is turned on. Only users with the admin role can enter scripted conditions.

## About this task

Use conditions to define company policies or guidelines for certain functional areas such as finance or legal departments. The advanced approval engine evaluates these conditions and if applicable, triggers the appropriate approval workflow.

Conditions are based on attributes for a Sales Customer Relationship Management entity or dynamic attributes defined in a Dynamic Schema. For example, quote attributes are derived from the Quote \[sn\_quote\_mgmt\_core\_quote\] table and can include items such as discount percentage, total quote value \(ACV or ARR\), total margin, payment terms, contract term length, country or geographic location, currency, product SKUs, customer risk flags, ramp pricing indicators, and custom fields.

**Note:** If you have the admin role, you can turn on the **Advanced condition** option to specify trigger conditions using scripts. If you use the advanced condition feature, you can't enter conditions using the condition builder.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **Approval Trigger Conditions**.

4.  In the **Name** field, enter the name for the conditions that trigger an approval.

    For example, if you want to trigger approvals for quotes that have low margins, you might name the condition `Low Margin Quote`.

5.  In **Approval configuration**, select the configuration for the Sales and Order Management entity, such as Quote.

    The Condition section opens for adding trigger conditions.

6.  If you don't want the trigger condition to be active, unselect the **Active** field.

    By default, the trigger condition is Active.

7.  In the Condition section, add one or more conditions that must be met to trigger approvals.

    Specify a condition by selecting the **Field** and **Operator**, and entering a value for the operator. For example, you can specify a condition that requires approvals when the discount for a quote line item is 20% or higher: **\[Discount percentage\] \[greater than or is\] \[20\]**

    For basic information on setting conditions, see Condition builder. For more information on the available operators, see Operators available for filters and queries.

8.  If you have the admin role and want to specify trigger conditions using scripts, turn on the **Advanced condition** field.

    The Condition section is replaced by the following fields for entering scripted conditions:

    -   **Description**: Enter the name of the scripted condition.
    -   **Scripted condition**: Use the JavaScript Syntax Editor to enter the script with the trigger conditions.
9.  For approval resubmissions, indicate whether approvals granted previously for an approval request can be used by selecting **Smart re-approval**.

    The Smart condition section opens for specifying any conditions that must be met for previous approvals to be reused for resubmitted approval requests.

10. In the Smart condition section, add one or more conditions for Smart approval resubmissions that must be met to control whether previous approvals can be reused for the approval request.

    For example, you could specify a condition that reapproval is required only if the discount increases by more than 2% from the last approved value.

11. If you have the admin role and want to specify trigger smart conditions using scripts instead of using the condition builder, turn on the **Advanced condition** field.

    The Smart condition section is replaced by the following fields for entering scripted conditions:

    -   **Description**: Enter the name of the scripted condition for Smart re-approvals.
    -   **Scripted condition**: Use the JavaScript Syntax Editor to enter the script with the conditions for the re-approvals.
12. Select **Save**.


## What to do next

[Create approval rules](create-approval-rules.md).

