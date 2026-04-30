---
title: Synchronize team calendar with Microsoft Outlook
description: Managers and agents can synchronize their calendars and events with Microsoft Outlook.
locale: en-US
release: xanadu
product: Workforce Optimization for Customer Service
classification: workforce-optimization-for-customer-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Workforce Optimization for Customer Service, Workforce Optimization for Customer Service, Customer Service Management]
---

# Synchronize team calendar with Microsoft Outlook

Managers and agents can synchronize their calendars and events with Microsoft Outlook.

As a user with admin role, you can enable this feature by installing Microsoft Exchange Online Spoke. See [Set up](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

**Note:** Ensure that you grant the following Graph API permissions to synchronize Microsoft Outlook with team calendar.

|Permission|Type|
|----------|----|
|Calendars.ReadWrite|Delegated|
|Calendars.ReadWrite.Shared|Delegated|
|Calendars.ReadWrite|Application|

After installing Microsoft Exchange Online Spoke, set the **sn\_wfo\_outlook.enable\_outlook\_sync** system property to `true` in the System Properties \[sys\_properties\] table. Add the email IDs that you want to synchronize in the User \[sys\_user\] table.

**Parent Topic:**[Configuring Workforce Optimization for Customer Service](setup-configurable-wfo-cs.md)

