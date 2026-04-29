---
title: Create an approval configuration
description: Create an approval configuration for a Sales and Order Management entity, such as quotes.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-20"
reading_time_minutes: 1
breadcrumb: [Advanced Approval Management, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create an approval configuration

Create an approval configuration for a Sales and Order Management entity, such as quotes.

## Before you begin

Role required: sn\_adv\_appr\_mgmt.approval\_rule\_admin or sn\_adv\_appr\_mgmt.approval\_rule\_writer

## About this task

An approval configuration is a container for the workflow elements that you define for a specified entity, such as the conditions that trigger approval workflows for related approval rules. You can also enable certain features for the configuration:

-   **Allow email consolidation**: Option that consolidates multiple, separate approval request emails for the same approver \(or group\) into a single approval request email, instead of sending multiple individual approval request emails. Consolidated email approval requests are held until the final relevant approval sequence for that approver is ready. The approval engine then routes the consolidated request to the approver \(or group\).
-   **Escalations**: Enable escalations, which is a mechanism for reassigning an approval request to another approver when the original approver does not take action within a defined time. If you enable this feature, you also define the escalation details in approval rules, such as the escalation assignee and length of time allowed for approval completion before the request is reassigned.
-   **Auto reminders for approval tasks**: Option that enables approval reminder notifications to be sent automatically to approvers, based on a reminder schedule that you set.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Advanced Approvals** &gt; **All Approval Configurations**.

4.  Select **New**.

    On the Approval Configuration form, fill in the fields to create a configuration for an entity, such as quotes. For field descriptions, see the [Approval Configuration form](../reference/approval-configuration-form.md).

5.  Select **Save**.

    The approval configuration for the specified entity is created.

    **Note:** A Sales and Order Management entity can have only one approval configuration.


## What to do next

[Create conditions that trigger approval workflows](set-approval-trigger-conditions.md)

