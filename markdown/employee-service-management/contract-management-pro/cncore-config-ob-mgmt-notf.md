---
title: Configure Obligation Management notifications
description: Activate Obligation Management notifications to notify users when an obligation task is created, assigned, submitted, approved, or rejected.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-10-18"
reading_time_minutes: 2
breadcrumb: [Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure Obligation Management notifications

Activate Obligation Management notifications to notify users when an obligation task is created, assigned, submitted, approved, or rejected.

## About this task

The Approval Request and Approval Rejected, notifications are triggered when an obligation task is submitted for approval and the obligation task is approved or rejected.

To avoid duplicate notifications for an event, the following notifications are not activated by default:

-   Obligation task submitted
-   Obligation task approved
-   Obligation task rejected

You can activate the notifications specific to obligation tasks and then set up a condition to stop the default system notifications.

For more information about obligation-related notifications, see [Obligation Management notifications](../reference/cncore-ob-mgmt-notification.md).

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  In the **Name** column, search for `Obligation`.

3.  Select the obligation notification that you want to activate.

4.  On the Notification form, select the **Active** check box.

5.  Select **Update**.

6.  Ensure that default notifications will not be triggered for any events related to obligation tasks.

    1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

    2.  Search for the default notifications that are triggered when an obligation task is submitted for approval and the obligation task is approved or rejected.

        The default notifications are **Approval Request** and **Approval Rejected**.

    3.  Select the notification.

    4.  Select the **When to send** tab.

    5.  In the **Conditions** field, set the following condition to ensure that the selected notification will not be triggered for any events related to obligations tasks: **\[Source table\] \[is not\] \[sn\_cm\_obligation\_obligation\_task\]**.


## Result

The obligation task-specific notifications are activated and the default system notifications are stopped for obligation events.

**Parent Topic:**[Configure Contract Management Pro](../concept/cncore-config-cmpro.md)

**Related topics**  


[Install Contract Management Pro](cncore-install-cmpro.md)

[Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

[Configure contract templates for a contract request](../concept/cncore-document-templates.md)

[Configure document templates for standard letters or documents](cncore-wdt-other-bu.md)

[Add and configure contract request functionality](../concept/cncore-uptake-steps.md)

[Configuring Contract Workspace with UI Builder components](../concept/cncore-conf-cntrct-wrkspc.md)

