---
title: Configure the Microsoft Exchange Online calendar provider in personal authentication mode
description: Enhance your workplace reservation experience with the Workplace Calendar Synchronization application to synchronize reservations with your calendar provider. Configure Microsoft Exchange Online to synchronize reservations with your calendar provider using personal authentication mode.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a personal authentication mode connection with Microsoft Exchange Online, Microsoft Exchange Online - Calendar synchronization, Setup Workplace Calendar Synchronization, Configure Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Configure the Microsoft Exchange Online calendar provider in personal authentication mode

Enhance your workplace reservation experience with the Workplace Calendar Synchronization application to synchronize reservations with your calendar provider. Configure Microsoft Exchange Online to synchronize reservations with your calendar provider using personal authentication mode.

## About this task

The Workplace Calendar Synchronization application uses the calendar provider as the primary source, confirming that events are updated and confirmed for room bookings through the Workplace Reservation Management portal.

## Before you begin

Confirm the following:

-   As a personal authentication mode user, you must have a valid mailbox in the Microsoft Exchange Online. The user is identified by the email address. The same email address must be specified in the delegated user email address where it’s necessary.

Confirm that the application scope is set to **Workplace Calendar Synchronization**.

**Note:** For calendars to synchronize successfully, you must have an email address that matches that of the provider.

Role required: sn\_wsd\_rsvsync.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Calendar Synchronization** &gt; **Configuration** &gt; **Calendar Providers**.

2.  Select **New**.

3.  On the Provider form, fill in the fields.

    For a description of the field values, see [Provider form](../reference/wsd-calendar-provider-form-fields.md).

    **Note:** The **Strict mode** field is deprecated and you must set the Exchange Online Sync Integration Mode property to Strict, Personal, or Normal mode. Additionally, the strict mode email has been updated to Delegated user email.

4.  Select **Submit**.


## What to do next

To access resource calendars and generate a subscription ID, you must add a Reservable Sync Configuration. For more information, see [Add multiple Reservable Sync Configurations](add-reservable-sync-config.md).

Execute an instance scan to check the synchronization configuration. For more information, see [Run Instance scan to check Microsoft Exchange Online synchronization configuration](run-instance-scan-on-your-workplace-cal-sync-configs.md).

**Parent Topic:**[Create a personal authentication mode connection with Microsoft Exchange Online](../concept/personal-auth-mode-connection-with-msex.md)

**Related topics**  


[Configure Microsoft Azure](configure-azure-personal-auth-mode.md)

[Configure resource rooms in Microsoft Exchange Online](configure-resource-rooms-in-msex.md)

[Set up personal authentication mode OAuth connectivity with Microsoft Exchange Online](setup-personal-auth-mode-oauth-connectivity-with-msex.md)

[Configure a personal authentication mode Connection and Credential alias for Microsoft Exchange Online](configure-personal-auth-mode-connection-and-credential-alias.md)

[Configure your own connection and credential alias for personal authentication mode](configure-your-own-connection-and-credential-alias-for-personal-auth.md)

