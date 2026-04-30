---
title: Configure resource rooms in Microsoft Exchange Online
description: Specify your delegated user email in the Microsoft portal to access the resource calendar.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure resource rooms in Microsoft Exchange Online

Specify your delegated user email in the Microsoft portal to access the resource calendar.

## Before you begin

Role required: Microsoft admin

## Procedure

1.  Go to [https://admin.exchange.microsoft.com/](https://admin.exchange.microsoft.com/).

2.  From the Navigation menu, select **Resources** **Rooms &amp; equipments**.

3.  Select a resource of **Type** - **Room** to configure strict mode to.

4.  In the room details, under the **Delegation** tab, edit the **Read and manage \(Full Access\)** permission.

5.  Select **Add members** and add read and manage permissions.

    This permission allows a delegate to open this mailbox and behave as the mailbox owner, with full access to the mailbox.

6.  Specify the users or the delegated user email address.

7.  Select **Save**.

    **Important:** Repeat steps 3 through 6 for every resource of the type **Room** that you want to configure the strict mode on.


## Result

The user is configured as the delegated user.

## What to do next

Create a personal authentication mode application registry for Microsoft Exchange Online with ServiceNow instance for OAuth authorization. For more information, see [Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md).

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

[Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md)

[Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md)

[Configure your own connection and credential alias for personal authentication mode](configure-your-own-connection-and-credential-alias-for-personal-auth.md)

[Configure the Microsoft Exchange Online calendar provider in personal authentication mode](configure-calendar-provider-in-personal-auth-mode.md)

