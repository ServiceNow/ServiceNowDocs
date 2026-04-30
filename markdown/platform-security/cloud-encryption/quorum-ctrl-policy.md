---
title: Quorum Control Policy
description: The Quorum Control Policy specifies the minimum number of approvals required among the total number of selected approvers to reach quorum for customer managed key withdrawal.
locale: en-US
release: yokohama
product: Cloud Encryption
classification: cloud-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cloud Encryption with Key Management, Encryption]
---

# Quorum Control Policy

The Quorum Control Policy specifies the minimum number of approvals required among the total number of selected approvers to reach quorum for customer managed key withdrawal.

**Warning:** You must sign a legal addendum to activate the key withdrawal functionality. The Quorum Control Policy Settings option becomes available when the withdrawal feature is enabled, otherwise the module isn’t visible on the app menu. After key withdrawal, your instance is no longer available until the encryption key is resupplied and is active again.

In certain circumstances, you may want to create a key withdrawal. You must first request the key withdrawal functionality from Customer Service and Support.

The Quorum Control Policy specifies the minimum number of approvals required among the total number of selected approvers to reach quorum for customer managed key withdrawal. For instance, there are a total of five approvers, but only four approvals are required to reach quorum. When four approvals are obtained, the withdrawal request is processed and the key withdrawn.

Whenever a withdrawal operation is performed in a group enabled for quorum approval, a workflow for quorum approval is triggered. An email notification is sent to all users who can grant approval. Tasks are also generated in the approvers’ accounts, which they see on the dashboard when they log in to their ServiceNow account.

The users can grant approvals from the Instance, the email, or the Key Management Operations page. The key withdrawal operation is blocked until the quorum is met.

Once the minimum number of approvers is reached, quorum is reached and the key withdrawal will trigger. The withdrawal is performed and is logged, including the names of users who approved the request.

See [Configure Quorum Control Policy Settings](../task/configure-quorum.md) for setup details.

-   **[Configure Quorum Control Policy Settings](../task/configure-quorum.md)**  
Follow these steps to configure Quorum Control Policy Settings.
-   **[Manage Quorum Control](../task/quorum-ctrl-mgmt.md)**  
After a withdrawal operation workflow is triggered, quorum actions can be managed from the Key Management Operations page. The key withdrawal operation is blocked until the quorum is met.

**Parent Topic:**[Cloud Encryption with Key Management](dare-overview.md)

