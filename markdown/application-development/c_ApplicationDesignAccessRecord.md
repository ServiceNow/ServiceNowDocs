---
title: Application design access record
description: Administrators use application design access records to specify which other applications are available to developers during application creation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application design access record

Administrators use application design access records to specify which other applications are available to developers during application creation.

When administrators restrict an application's table choices, they can then create application design access records to grant developers access to the tables of selected applications.

Each application design access record contains the following information.

|Field|Description|
|-----|-----------|
|Source Scope|The application requesting design access to another application's tables.|
|Target Package|The application whose tables will be available for design time access.|
|Application|The application to which this record belongs.|

Application design access records allow administrators to have oversight of the resources available to application developers. When creating configuration records, application developers can only select tables from another application if there is an application design access record granting them access to the application. For example, administrators could create the following application design access records to grant developers access to tables from Incident Management and Problem Management.

|Source Scope|Target Package|
|------------|--------------|
|My App|Incident|
|My App|Problem Management|

After developers create configuration records to other applications, the system displays these applications as dependencies.

**Parent Topic:**[Application design and runtime settings](../reference/r_ApplicationDesignAndRuntimeSettings.md)

