---
title: Post case review approvals
description: Enable an optional approval process for post case review documents.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Post case reviews, Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Post case review approvals

Enable an optional approval process for post case review documents.

In the case digest configuration, the system administrator can:

-   Enable the approval process by selecting an approval workflow.
-   Use a condition builder to define the conditions that determine the post case review documents that require approval.

One approval workflow, **Post Case Review - Default Approval**, is provided with the Case Digests plugin. This workflow reads the approvers from the **Approval group** and **Approval Users** fields on the Post Case Review form and sends an approval request notification to each user.

Approvers receive an email notification with a link to the post case review document. Approvers can either approve the document or suggest changes by adding them to the **Work notes** field on the Post Case Review form. The agent receives a notification when an approver approves the case review document or suggests changes.

-   If the approver suggests changes, the agent can see the changes in the **Work notes** field.
-   If the approver approves the document, the status of the post case review record changes to **Approved**.

