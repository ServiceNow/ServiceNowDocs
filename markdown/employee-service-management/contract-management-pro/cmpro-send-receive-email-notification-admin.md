---
title: Configure email notifications for approval workflow in Contract Management Pro
description: Activate the notifications for Contract Management Pro to notify users when approval for contract revision is initiated, approved, rejected, or cancelled.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage notifications in Contract Management Pro, Configure additional features in CM Pro, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure email notifications for approval workflow in Contract Management Pro

Activate the notifications for Contract Management Pro to notify users when approval for contract revision is initiated, approved, rejected, or cancelled.

## Before you begin

Role required: Admin

## About this task

The platform notifications, Approval Request and Approval Rejected, are triggered when approval is initiated for contract revision in a contract request.

To avoid duplicate notifications for an event, the following notifications are not activated by default:

-   Contract document - Approval requested
-   Contract document - Approved
-   Contract document - Approval cancelled

You can activate the notifications specific to Contract Management Pro approval workflow and then set up a condition to stop the default platform notifications.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  In the **Category** column, search for `contracts support`.

3.  Select the contract document approval notification that you want to activate.

    The available notifications are:

    -   Contract document - Approval requested
    -   Contract document - Approved
    -   Contract document - Approval cancelled
4.  On the Notification form, select the **Active** check box.

5.  Select **Update**.

    **Note:** You must configure the **ApprovalNotificationWorkspaceURLExt** extension point to enable the notifications for Legal Counsel Center.

    For more information, see [Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md).

6.  Ensure that default notifications will not be triggered for approval workflow related to Contract Management Pro.

    1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

    2.  Search for the default notifications that are triggered when approval is initiated for a contract revision.

        The default notifications are **Approval Request** and **Approval Rejected**.

        ![Default platform approval notifications in the notifications page](../image/cmpro-ptfm-apprvl-notf.png "Default platform notifications for approval workflow")

    3.  Select the notification.

    4.  Select the **When to send** tab.

    5.  In the **Conditions** field, set the following condition to ensure that the selected notification will not be triggered for contract revision approval workflow: **\[Source table\] \[is not\] \[sn\_cm\_core\_document\_revision\]**.


## Result

The Contract Management Pro specific approval notifications are activated and the default system notifications are stopped for contract revision approval.

**Parent Topic:**[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

