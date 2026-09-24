---
title: Create a notification
description: Create notifications for Core Business Suite business units through the Now Assist conversational experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/core-business-suite/create-notification-using-na.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Otto for Core Business Suite \(CBS\), Configure Core Business Suite using Otto, Configure, Core Business Suite]
---

# Create a notification

Create notifications for Core Business Suite business units through the Now Assist conversational experience.

## Before you begin

Ensure that Now Assist in Virtual Agent is installed. For more information, see .

Role required: admin, sn\_cbs.admin

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  On the Core Business Suite card, select **View product overview**.

3.  In the Configuration insights section, select **Configure**.

    The Configure Core Business Suite page opens in the Configuration Console.

4.  Select **Notifications** under the business unit you want to configure \(for example, Human Resources, Legal, Finance, Health and Safety, Workplace Services, or Source-to-Pay\).

5.  Select **Configure with Now Assist**.

    Now Assist opens the conversational panel, detects the current page context, and invokes the Notification Agent.

    **Note:** Now Assist guides you through follow‑up questions and requests confirmation before creating the notification.

6.  Select **Create a new notification**, or enter a natural‑language prompt.

    Example prompts:

    -   `Notify the fulfiller when an [BU name] case is assigned`
    -   `Notify the employee when an [BU name] case is resolved or closed`
    -   `Set up a notification for managers when their direct reports open an [BU name] request`
7.  Respond to the follow‑up questions provided by Now Assist, such as:

    -   The table the notification applies to
    -   The trigger criteria \(on create, update, or both\)
    -   The recipients \(users, groups, or fields\)
    Now Assist processes your responses and prepares the notification details.

8.  Review the notification details.

9.  Select one of the following options:

    -   **No, looks good** to confirm
    -   **Yes, I’d like to make changes** to update the details
10. If you choose to make changes, enter the updates when prompted.

    Now Assist revises the notification and presents the updated details.

11. Review the updated notification details and confirm.

    Now Assist creates the notification and displays a success message.


**Parent Topic:**[ServiceNow Otto for Core Business Suite \(CBS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/core-business-suite/now-assist-cbs.md)

