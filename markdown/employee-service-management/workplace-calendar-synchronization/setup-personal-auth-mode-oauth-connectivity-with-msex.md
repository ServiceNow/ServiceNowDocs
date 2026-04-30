---
title: Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online
description: Create a personal authentication mode application registry for Microsoft Exchange Online with your instance for OAuth authorization.
locale: en-US
release: zurich
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a personal authentication mode connection, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online

Create a personal authentication mode application registry for Microsoft Exchange Online with your instance for OAuth authorization.

## Before you begin

Configure Microsoft Azure. For more information, see [Configure Microsoft Azure](configure-azure-personal-auth-mode.md).

Confirm that the application scope is set to **Workplace Calendar Synchronization**.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select the **Microsoft Exchange Online\_personalAuth** OAuth provider created for personal authentication.

3.  On the Third-party OAuth Provider form, fill in the fields:

    For a description of the field values, see [Third-party OAuth Provider form](../reference/wsd-third-party-oauth-provider-form.md).

4.  Right-click in the form header and select **Save**.

    A system-generated OAuth entity profile is created and displayed in the OAuth Entity Profiles related list. For example, Microsoft Exchange Online\_personalAuth default profile.

5.  Select the OAuth Entity Scopes list and verify that the following OAuth scopes are already defined for the OAuth provider profile:

    1.  Calendars.ReadWrite

    2.  Calendars.ReadWrite.Shared

    3.  Offline\_access

6.  Select **Update**.


## Result

The OAuth registration is added for Microsoft Exchange Online with personal authentication mode OAuth entity profiles and OAuth entity scopes.

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

[Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md)

[Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md)

[Configure your own connection and credential alias for personal authentication mode](configure-your-own-connection-and-credential-alias-for-personal-auth.md)

[Configure the Microsoft Exchange Online calendar provider in personal authentication mode](configure-calendar-provider-in-personal-auth-mode.md)

