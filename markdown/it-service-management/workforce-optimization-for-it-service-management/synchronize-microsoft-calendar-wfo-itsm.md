---
title: Set up the Workforce Optimization for ITSM agent calendar integration with their Microsoft Outlook calendar
description: Display the schedules, shifts, and events from the agent's calendar also in their Microsoft Outlook calendar when you synchronize both the calendars.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Synchronize agent calendar in Workforce Optimization for ITSM with the Microsoft Outlook calendar, Setting up Scheduling in Workforce Optimization for ITSM, Scheduling in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Set up the Workforce Optimization for ITSM agent calendar integration with their Microsoft Outlook calendar

Display the schedules, shifts, and events from the agent's calendar also in their Microsoft Outlook calendar when you synchronize both the calendars.

## Before you begin

Role required: admin

## Procedure

1.  Set up the [Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

    **Note:** Verify that the following Microsoft Graph permissions are set correctly in the Microsoft Azure portal:

    |Permission|Type|Description|
    |----------|----|-----------|
    |Calendars.ReadWrite|Delegated|Full access to user calendars|
    |Calendars.ReadWrite.Shared|Delegated|Read and write access to user and shared calendars|
    |Calendars.ReadWrite|Application|Read and write access to calendars in all mailboxes|

2.  Set the **sn\_wfo\_outlook.enable\_outlook\_sync** system property to **true**.

    For more information, see [Scheduling components in Workforce Optimization for ITSM](../reference/configurable-wfo-itsm-scheduling-reference.md).

3.  Add the email IDs of the users that you want to synchronize to the User \[sys\_user\] table.

    Your agents' Workforce Optimization for ITSM calendar is now synchronized with their Microsoft Outlook calendar.

    **Important:** If the swapped shifts don't appear in the Microsoft Outlook calendar, verify that you've followed all steps in this procedure to make sure that the schedule for the shifts have been synchronized with Microsoft Outlook.


**Parent Topic:**[Synchronize agent calendar in Workforce Optimization for ITSM with the Microsoft Outlook calendar](../concept/synchronize-microsoft-outlook-wfo-itsm.md)

