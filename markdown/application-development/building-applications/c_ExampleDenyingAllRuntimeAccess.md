---
title: Example denying all runtime access to a table
description: You can prevent script API and web service calls from other application scopes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/c\_ExampleDenyingAllRuntimeAccess.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Runtime access to applications tables, Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Example denying all runtime access to a table

You can prevent script API and web service calls from other application scopes.

Typically, this is to prevent any other application from creating or modifying data in the table. Denying access requires setting the following value in the table record.

|Field|Value|
|-----|-----|
|**Accessible from**|This application scope only|
|**Can read**|Disabled|
|**Can create**|Disabled|
|**Can update**|Disabled|
|**Can delete**|Disabled|
|**Allow access to this table via web services**|Disabled|

\[Omitted image "DenyingAllRuntimeAccess.png"\] Alt text: Application access settings

The following diagram illustrates the effect of denying other application scopes access to application tables from script API and web service calls.

\[Omitted image "EffectsOfDenyAllRuntimeAccess.png"\] Alt text: Effects of denying all runtime access to application tables

**Parent Topic:**[Runtime access to applications tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_RuntimeAccessToAppTables.md)

