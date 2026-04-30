---
title: Reactivate a cloud account
description: Reactivate an account that was previously suspended if there is a need retrieve the account. After reactivating an account, the account status changes from suspended to active. Only Cloud Account Management managed accounts can be reactivated.
locale: en-US
release: yokohama
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2024-04-08"
reading_time_minutes: 1
breadcrumb: [Managing cloud accounts, Using Cloud Account Management in Cloud Workspace, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Reactivate a cloud account

Reactivate an account that was previously suspended if there is a need retrieve the account. After reactivating an account, the account status changes from suspended to active. Only Cloud Account Management managed accounts can be reactivated.

## About this task

Only an admin or account owner can view the reactivated account.

## Before you begin

A suspend profile must exist for an account to be reactivated. For more details, see [Set up suspension of an AWS account using service control policy](configure-suspension-policy.md).

Role required: sn\_itom\_cam.cw\_admin or sn\_itom\_cam.cw\_requestor

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Home**.

2.  Select **Subscription Accounts**.

3.  In the **Managed Accounts** section, select **Suspended**.

4.  Select an entry in the list of suspended accounts and select **Reactivate**.

5.  Enter a reason for reactivation in the **Reason** field and select **Yes**.

    The reactivation request is sent for approval. Reactivated accounts are listed in the **Managed Accounts** section.


