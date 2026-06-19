---
title: Example denying all design access to a table
description: You can prevent other application scopes from creating configuration records on application data tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/building-applications/c\_ExampleDenyingAllDesignAccess.html
release: zurich
product: Building Applications
classification: building-applications
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Design-time access to application tables, Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Example denying all design access to a table

You can prevent other application scopes from creating configuration records on application data tables.

Typically, this is to prevent any other applications from changing the functionality of a table. Denying access requires setting the following value in the table record.

|Field|Value|
|-----|-----|
|**Accessible from**|This application scope only|
|**Can read**|Disabled|
|**Can create**|Disabled|
|**Can update**|Disabled|
|**Can delete**|Disabled|
|**Allow access to this table via web services**|Disabled|
|**Allow configuration**|Disabled|

\[Omitted image "DenyingAllRuntimeAccess.png"\] Alt text: Limiting design-time access to this application scope only

The following diagram illustrates the effect of denying other application scopes the ability to create configuration records.

\[Omitted image "EffectsOfDenyAllDesignTimeAccess.png"\] Alt text: Limiting design access to this application scope only

**Parent Topic:**[Design-time access to application tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/c_DesignTimeAccessToAppTables.md)

