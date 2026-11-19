---
title: Suspend a Cloud account
description: Suspend an account when there’s a budget constraint or the account owner isn’t available in the organization. Only admins and account owners can see the suspended accounts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/suspend-account.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Managing cloud accounts, Use, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Suspend a Cloud account

Suspend an account when there’s a budget constraint or the account owner isn’t available in the organization. Only admins and account owners can see the suspended accounts.

## Before you begin

To suspend an account, it must have a suspend profile and be managed by CAM. For more information, see [Set up suspension of an AWS account using service control policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configure-suspension-policy.md).

Role required: sn\_itom\_cam.cw\_admin or sn\_itom\_cam.cw\_requester

## Procedure

1.  Navigate to **All** &gt; **Cloud Workspace**.

2.  Select **Manage and Configure** &gt; **Cloud accounts** &gt; **Accounts** and select the account name.

    If the account is unmanaged, you must onboard it before you can suspend it. For more information, see [Add an unmanaged cloud account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/add-unmanaged-account-cam.md)

3.  Select **Suspend**.

4.  In the confirmation dialog box, enter the reason for suspension and select **Yes**.

    -   After you submit a suspension request, it is sent to the admin for approval.
    -   The Suspend Request Notify email notification is sent to the requester and approvers of the request.
5.  To view suspended accounts, go to **Manage and Configure** &gt; **Cloud accounts** &gt; **Accounts** and set the **Account status** filter to **Suspended**.


**Parent Topic:**[Managing cloud accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/managing-an-account.md)

