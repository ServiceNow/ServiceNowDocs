---
title: Approve an exception rule request
description: Assess exception rule requests from users so that you can approve or reject these requests.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Configuring an exception rule, Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Approve an exception rule request

Assess exception rule requests from users so that you can approve or reject these requests.

## Before you begin

Role required: sn\_vul.exception\_approver

## About this task

Exception approver level 1 user group members can approve the level 1 exception rule requests. Similarly, exception approver level 2 user group members can approve the level 2 exception rule requests. Both the user groups inherit the exception approver role by default.

**Note:**

If you are deploying the VR application for the first time, the flow designer for exception management is enabled by default. If you are already using the workflow, you can update to the flow designer. In both cases, you cannot change it back to workflow. To configure approval rules for exception management and false positive, see [Configure approval rules for Exception Management](../../vulnerability-response/task/exception-mgt-approval-rules.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Exception rules** tile.

4.  Select a request from your queue.

5.  Approve or reject the request with and explain why you approved or rejected the request.


**Parent Topic:**[Configuring an exception rule](../concept/sem-configure-exception-rule.md)

