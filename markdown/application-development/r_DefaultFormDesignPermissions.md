---
title: Default form design permissions
description: By default, new application data tables have the following form design permissions.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Form design visual indicators, Lists and forms in scoped applications, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Default form design permissions

By default, new application data tables have the following form design permissions.

|Form design action|Permission setting|
|------------------|------------------|
|Create new sections in tables belonging to another application scope|Allowed|
|Create new fields in sections belonging to the same application scope|By default, denied. Requires application designer to set **Allow configuration** for application table.|
|Add or remove fields from sections belonging to the same application scope|Allowed|
|Change the order of fields in sections belonging to the same application scope|Allowed|
|Change the order of sections belonging to the same application scope|Allowed|
|Add or remove fields from sections belonging to another application scope|Denied|
|Change the order of fields in sections belonging to another application scope|Denied|
|Change the order of sections belonging to another application scope|Denied|
|Create new fields in sections belonging to another application scope|Denied|

