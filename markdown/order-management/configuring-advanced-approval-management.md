---
title: Configuring Advanced Approval Management
description: Install the Advanced Approval Management application to build workflows that automate the approval process for Sales Customer Relationship Management entities such as customer quotes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configuring Advanced Approval Management

Install the Advanced Approval Management application to build workflows that automate the approval process for Sales Customer Relationship Management entities such as customer quotes.

## Advanced Approval Management configuration overview

1.  [Install Advanced Approval Management](../task/install-advanced-approval-management.md).

    You can install the Advanced Approval Management application \(sn\_adv\_appr\_mgmt\) if you have the admin role.

    **Note:** The plugin for the Sales Customer Relationship Management application for which you are creating workflows, such as Quote Management, must also be installed.

2.  [Create an approval configuration](../task/create-approval-configuration.md)

    Create an approval configuration for a Sales Customer Relationship Management entity, such as quotes. An approval configuration contains the approval elements that you define to automate approval workflows: conditions that trigger approval workflows, approval rules, approval chains, and approval users and groups. Starting with the 1.0.1 release, you can enable certain features for the configuration, namely approval request consolidation, escalations, and email reminder features.

3.  [Create conditions that trigger approval workflows](../task/set-approval-trigger-conditions.md).

    Define one or more conditions that apply company policies, such as legal or pricing guidelines, to trigger an approval workflow. Also enable the smart reapprovals feature, which allows previous approvals to be used for a resubmitted approval.

4.  [Create approval rules](../task/create-approval-rules.md).

    Create approval rules that define the approval criteria and approvers for an approval step.

5.  [Create approval chains](../task/create-approval-chain.md).

    Optionally create approval chains that control the sequence in which two or more approvals are run.

6.  [Define an approval user](../task/create-approval-users.md).

    Define the approver and the associated approval rule that they review during the approval process.

    [Define an approval group](../task/create-approval-groups.md).

    Define the group that can approve requests for a specified approval rule.


**Note:** System notifications are used to deliver approval status to requesters and inform approvers of approval rejections. You can use these notifications and customize them if needed. For more information, see [Notifications in Advanced Approval Management](setting-up-approval-notifications.md).

