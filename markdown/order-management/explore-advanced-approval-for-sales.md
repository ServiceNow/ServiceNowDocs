---
title: Advanced Approval Management
description: The Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes, in your sales organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Advanced Approval Management

The Advanced Approval Management application enables you to define workflows for approving Sales Customer Relationship Management entities, such as customer quotes, in your sales organization.

## Advanced Approval Management overview

Sales agents use workflows created by approval admins in Advanced Approval Management to preview and submit approval requests for entities such as quotes. Authorized approvers review approval requests to verify that the items meet legal guidelines and company pricing policies. They can either approve or requests. These workflows provide oversight of the approval process, which helps prevent financial errors and delays in approvals, particularly for high-value or high-risk deals. During the approval process, sales agents and approvers receive notifications informing them of the approval status and approval tasks.

## Advanced Approval Management users

<table id="table_mmc_stx_zhc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval rule admin, approval rule writer\(For example, sales or business operation managers\)

</td><td>

Creates approval configurations for Sales Customer Relationship Management entities, approval chains, approval trigger conditions, approval rules, approval users, and approval groups.

</td></tr><tr><td>

Approval rule viewer\(For example, business stakeholders, operations managers\)

</td><td>

Views approval entities, approval chains, approval trigger conditions, approval rules, approval users, and approval groups.

</td></tr><tr><td>

Approval requester\(For example, sales representatives\)

</td><td>

Creates, previews, and submits approval requests for entities, such as quotes. Tracks status, recalls approval requests if needed, and views approval history.

</td></tr><tr><td>

Approvers\(For example, members of Sales, Finance, and Legal teams\)

</td><td>

Reviews, approves or rejects, and delegates approval requests. Can act on requests using different notification channels, such as email, CSM Configurable Workspace, and approval centers.

</td></tr><tr><td>

Approval request viewer

</td><td>

Views approval requests and approval steps.

</td></tr></tbody>
</table>For a complete list of user roles, see [Components installed with Advanced Approval Management](../reference/components-installed-advanced-approval-management-for-sales.md).

## Advanced Approval Management workflow

This section describes the tasks involved in configuring and using Advanced Approval Management.

1.  As an approval rule admin or writer, create an approval configuration for a Sales Customer Relationship Management entity, such as quotes.
2.  Build approval workflows by creating:
    -   Conditions that trigger the rules in the workflow
    -   Approval rules that control the steps in the workflow
    -   Approval chains for organizing workflow steps and the type of approval work
    -   Approval users and groups \(approvers and approver groups\)
3.  As a requester \(sales rep\), create and preview an approval request, then submit the request. The approval engine routes the approval request to authorized approvers.
4.  As a requester, monitor and track the approval process using the advanced approval interface.
5.  As an approver, review and either accept or reject an approval request based on conditions and rules.
6.  As a requester, update rejected requests and resubmit the requests.
7.  As a requester, when the request is approved, proceed with the transaction.

## Advanced Approval Management benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Build and automate workflows that can handle sequential or parallel approvals or a combination of both|[Create approval rules](../task/create-approval-rules.md) and [Create approval chains](../task/create-approval-chain.md)|Approval admins|
|Enforce financial and legal guidelines particularly for high-value deals to reduce financial and legal risk|[Create conditions that trigger approval workflows](../task/set-approval-trigger-conditions.md)|Approval admins and approvers|
|Preview the rules, steps, and approvers before submitting a request|[Submitting approval requests](submitting-approval-requests.md)|Requesters|
|Monitor approval workflow and status|[Tracking approval status and history](tracking-approval-status.md)|Requesters, approvers, and business stakeholders|

## What to explore next

To learn more about configuring and using Advanced Approval Management, see:

-   [Configuring Advanced Approval Management](configuring-advanced-approval-management.md)
-   [Using Advanced Approval Management](using-advanced-approval-management.md)
-   [Advanced Approval Management reference](../reference/advanced-approval-management-reference.md)

