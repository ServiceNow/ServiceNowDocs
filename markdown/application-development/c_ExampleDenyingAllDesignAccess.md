---
title: Example denying all design access to a table
description: You can prevent other application scopes from creating configuration records on application data tables.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
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

![Limiting design-time access to this application scope only](../image/DenyingAllRuntimeAccess.png "Limiting design-time access to this application scope only")

The following diagram illustrates the effect of denying other application scopes the ability to create configuration records.

![Limiting design access to this application scope only](../image/EffectsOfDenyAllDesignTimeAccess.png "Limiting design access to this application scope only")

**Parent Topic:**[Design-time access to application tables](c_DesignTimeAccessToAppTables.md)

