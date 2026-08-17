---
title: Components installed with Store Plans - Fulfilment in Portal
description: Certain roles, plugin dependencies, and fields must be considered when fulfilling Store Cases and Store Tasks from the Retail Portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/rahi-retail-components-fulfilment-in-portal.html
release: australia
topic_type: reference
last_updated: "2026-07-14"
reading_time_minutes: 3
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Store Plans - Fulfilment in Portal

Certain roles, plugin dependencies, and fields must be considered when fulfilling Store Cases and Store Tasks from the Retail Portal.

## Plugins used by Fulfilment in Portal

Fulfilment in Portal introduces no new plugin. It extends the existing Retail In-store Operations plugin so that Store Cases and Store Tasks generated from store plans can also be viewed and fulfilled from the Retail Portal, in addition to Retail Mobile and Workspace. The embedded questionnaire reuses the existing Smart Assessment components; see [Components installed with Smart Assessments for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-smart-assessments.md).

<table id="table_plugins-fulfilment-in-portal"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail In-store Operations

 \[com.sn\_rtl\_in\_store\_ops\]

</td><td>

Reused plugin. Enables the portal record pages, the Tasks tab on a Store Case, and the Questionnaires tab on a Store Task. Portal fulfilment supports the Australia platform version and above; it is not available on Zurich or earlier.

</td><td>

-   com.sn\_retail\_core
-   


</td></tr></tbody>
</table>## Roles used by Fulfilment in Portal

<table id="table_roles-fulfilment-in-portal"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_rtl\_instore\_ops.associate

</td><td>

On the portal, views all Store Cases and Store Tasks for their store. Can comment, upload attachments, and reassign a case or task via Edit. Can close a case or task only if assigned to it. Can fill in and submit a questionnaire only if assigned to the linked task.

</td><td>

-   sn\_retail.associate\_fulfiller
-   wm\_location\_agent
-   questionnaire\_user

</td></tr><tr><td>

sn\_rtl\_instore\_ops.manager

</td><td>

All associate capabilities, plus: can close a case or task on behalf of the assigned associate, can close a case with open tasks \(warning, not blocked\), and can reopen a closed case.

</td><td>

-   sn\_rtl\_instore\_ops.associate
-   sn\_retail.manager\_fulfiller
-   wm\_location\_assignment\_manager

</td></tr></tbody>
</table>## Store Case fields on the portal

|Field|Editable on portal|Example|
|-----|------------------|-------|
|Short description|Read-only|Daily Store Opening - HQ Oversight|
|Case number|Read-only|RIS0001037|
|Status|Read-only \(badge\)|Open|
|Description|Read-only|Plan-authored. Collapsed by default on the standard header.|
|Assigned to|Editable via Edit modal|Store Manager or Associate|
|Priority|Read-only|3 - Moderate|
|Due date|Read-only|2026-08-02 00:00:00|
|Parent|Read-only, plain text \(not hyperlinked\)|RHC00163|
|Supporting retail org|Read-only|Solana San Diego|
|Requesting retail org|Read-only|Solana California|

## Store Task fields on the portal

|Field|Editable on portal|Example|
|-----|------------------|-------|
|Short description|Read-only|Complete daily store opening questionnaire|
|Task number|Read-only|SOTASK001|
|Status|Read-only \(badge\)|Open|
|Description|Read-only|Collapsed by default on the standard header.|
|Assigned to|Editable via Edit modal; stays editable after questionnaire completion, until the task closes|Store Associate|
|Assignment group|Editable via Edit modal only; stays editable until the task closes|Store Associates Group|
|Priority|Read-only|Set by plan author|
|Due date|Read-only|Set by plan author|
|Parent case|Read-only, plain text \(not hyperlinked\)|RIS0001037|
|Supporting retail org|Read-only|Solana San Diego|
|Requesting retail org|Read-only|Solana California|

**Parent Topic:**[Components installed with plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-installed-with-plugins.md)

**Related topics**  


[Fulfill In-store operations cases and tasks on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-fulfill-in-store-ops-portal.md)

[Work on a Store Case on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-work-in-store-operations-case-portal.md)

[Work on a Store Task on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-in-store-task-portal.md)

[Complete a questionnaire for a Store Task on the Retail Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-complete-questionnaire-portal.md)

[Components installed with Retail In-store Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/retail-industry/rahi-retail-components-in-store-operations.md)

