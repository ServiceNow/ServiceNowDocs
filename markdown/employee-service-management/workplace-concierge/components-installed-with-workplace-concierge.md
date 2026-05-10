---
title: Components installed with Workplace Concierge
description: Several types of components are installed with activation of the Workplace Concierge application, including tables, user roles, and business rules.
locale: en-US
release: australia
product: Workplace Concierge
classification: workplace-concierge
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workplace Concierge - Components, Workplace Concierge, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Concierge

Several types of components are installed with activation of the Workplace Concierge application, including tables, user roles, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/find-components.md).

## Roles installed with Workplace Concierge

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_wsd\_concierge.admin|Has complete access to the application.|sn\_wsd\_core.profile\_writer|

## Tables installed with Workplace Concierge

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Employee Presence Routine\[sn\_wsd\_concierge\_employee\_presence\_routine\]

</td><td>

Stores information about all the Employee Presence routines created in the application.

</td></tr><tr><td>

Employee Presence Exceptions

</td><td>

If the presence status is changed from **In-office** to **Remote**, a record is created in the Employee Presence Exceptions table \(**All** &gt; **Workplace Concierge** &gt; **Employee Presence** &gt; **Exceptions**\). If the presence status is changed from "**In-office** or **Remote**" to "**Visit another office**," a record is created in the Employee Presence Exceptions table and Location column is updated with the building name for the **In-office** day. For more information, see [Manage workplace schedule and in-office presence using Workplace Service Delivery for Mobile](../../wsd-for-mobile/concept/workplace-preference-schedule.md).

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Concierge - Components](../concept/workplace-concierge-references.md)

**Related topics**  


[Properties installed with Workplace Concierge](properties-installed-with-workplace-concierge.md)

[Insights installed with Workplace Concierge](insights-installed-workplace-concierge.md)

