---
title: Synchronize team calendar with Microsoft Outlook
description: Managers and agents can synchronize their calendars and events with Microsoft Outlook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/synch-cal-msoutlook-wfo-cs.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Optimize workforce operations, Extend capabilities, Configure, Customer Service Management]
---

# Synchronize team calendar with Microsoft Outlook

Managers and agents can synchronize their calendars and events with Microsoft Outlook.

As a user with admin role, you can enable this feature by installing Microsoft Exchange Online Spoke. See [Set up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integration-hub/setup-ms-exch-ol.md).

**Note:** Ensure that you grant the following Graph API permissions to synchronize Microsoft Outlook with team calendar.

|Permission|Type|
|----------|----|
|Calendars.ReadWrite|Delegated|
|Calendars.ReadWrite.Shared|Delegated|
|Calendars.ReadWrite|Application|

After installing Microsoft Exchange Online Spoke, set the **sn\_wfo\_outlook.enable\_outlook\_sync** system property to `true` in the System Properties \[sys\_properties\] table. Add the email IDs that you want to synchronize in the User \[sys\_user\] table.

**Parent Topic:**[Optimize workforce operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/setup-configurable-wfo-cs.md)

