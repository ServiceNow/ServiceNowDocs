---
title: Create a strict mode configuration in Microsoft Exchange Online
description: Specify your delegated user email in the Microsoft portal.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a strict mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Create a strict mode configuration in Microsoft Exchange Online

Specify your delegated user email in the Microsoft portal.

## Before you begin

[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

Role required: Microsoft admin

## Procedure

1.  Go to [https://admin.exchange.microsoft.com/](https://admin.exchange.microsoft.com/).

2.  On the left panel, select **Resources** **Rooms &amp; equipments**.

3.  Select a resource of **Type** - **Room** to which you to configure strict mode.

4.  In the room details, under the **Delegation** tab, edit the **Read and manage \(Full Access\)** permission.

5.  Select **Add members** and add read and manage permissions.

    This permission allows a delegate to open this mailbox and behave as the mailbox owner, with full access to the mailbox.

6.  Specify the users or the delegated user email address.

7.  Select **Save**.

    **Important:** Repeat the steps from Step 3 to Step 6 for every resource of the type **Room** on which you want to configure the strict mode.


## Result

The user is configured as the delegated user.

## What to do next

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

**Parent Topic:**[Create a strict mode connection with Microsoft Exchange Online](../concept/strict-mode-configurations-for-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](auth-mxex-with-azure-strict-mode.md)

[Create connection with Microsoft Exchange Online Spoke in strict mode](create-connection-with-msspoke-strict-mode.md)

[Setup strict mode OAuth connectivity with Microsoft Exchange Online](setup-strict-mode-oauth-connectivity-with-msex.md)

[Configure strict mode Connection and Credential alias for Microsoft Exchange Online](configure-strict-mode-connection-and-credential-alias-for-msex.md)

[Create your own credential and connection alias for strict mode](create-own-credential-and-connection-alias-for-strict-mode.md)

[Configure Microsoft Exchange Online calendar provider in strict mode](configure-msex-strict-mode-calendar-providers.md)

