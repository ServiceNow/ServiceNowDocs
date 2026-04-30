---
title: Suspend a Cloud account
description: Suspend an account when there’s a budget constraint or the account owner isn’t available in the organization. Only admins and account owners can see the suspended accounts.
locale: en-US
release: zurich
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing cloud accounts, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Suspend a Cloud account

Suspend an account when there’s a budget constraint or the account owner isn’t available in the organization. Only admins and account owners can see the suspended accounts.

## Before you begin

An account requires a suspend profile to be suspended. For more information, see [Set up suspension of an AWS account using service control policy](../task/configure-suspension-policy.md).

Role required: sn\_itom\_cam.cw\_admin or sn\_itom\_cam.cw\_requestor

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace** &gt; **Home**.

2.  Select **Subscription Accounts**.

3.  Under the **Managed Accounts** section, select **Active**.

4.  Select an account check box and select **Suspend**.

5.  In the confirmation dialog box, enter the reason for suspension and select **Yes**.

    -   Once you have created a suspension request, the request is sent to the admin for approval.
    -   Suspended accounts are listed under the **Managed Accounts** &gt; **Suspended** section.

