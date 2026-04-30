---
title: Example granting all runtime access to a table
description: You can permit some or all runtime script API and web service calls from other application scopes.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Runtime access to applications tables, Table design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Example granting all runtime access to a table

You can permit some or all runtime script API and web service calls from other application scopes.

Granting access requires setting the following values in the table record.

|Field|Value|
|-----|-----|
|**Accessible from**|All application scopes|
|**Can read**|Enabled|
|**Can create**|Enabled|
|**Can update**|Enabled|
|**Can delete**|Enabled|
|**Allow access to this table via web services**|Enabled|

![Granting other application scopes all runtime access permissions](../image/GrantingAllRuntimeAccess.png "Granting other application scopes all runtime access permissions")

The following diagram illustrates the effect of granting access to application tables from API calls and web services in other application scopes.

![Granted access to application tables](../image/EffectsOfGrantAllRuntimeAccess.png "Granted access to application tables")

**Parent Topic:**[Runtime access to applications tables](c_RuntimeAccessToAppTables.md)

