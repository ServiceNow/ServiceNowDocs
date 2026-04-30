---
title: Cross-scope privilege record
description: Runtime access tracking uses cross-scope privilege records to determine which script operations and targets the system allows to run.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application design and runtime settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Cross-scope privilege record

Runtime access tracking uses cross-scope privilege records to determine which script operations and targets the system allows to run.

The system creates cross-scope privilege records when:

-   Runtime access tracking is set to **Tracking** or **Enforcing**.
-   A script attempts to access another application.

Each cross-scope privilege record in the Cross scope privileges \[sys\_scope\_privilege\] table contains the following information.

|Field|Description|
|-----|-----------|
|Source Scope|The application requesting runtime access to another application's resources.|
|Target Scope|The application whose resources are being requested.|
|Target Name|The name of the table, script include, or script object being requested.|
|Target Type|The type of request: table, script include, or script object.|
|Operation|The operation the script performs on the target. The target type determines the available operations. Tables support the read, write, create, and delete operations. Script includes and script objects only support the execute API operation.|
|Status|The authorization for this record: requested, allowed, or denied|

Administrators can manually create cross-scope privilege records for application developers in advance to communicate which cross-scope resources they expect developers to access. For example, administrators could create these cross-scope privilege records to permit application developers access to resources from Incident Management.

|Source Scope|Target Scope|Target Name|Operation|Status|
|------------|------------|-----------|---------|------|
|My App|Global|incident|Read|Allowed|
|My App|Global|incident|Write|Allowed|
|My App|Global|ScopedGlideRecord|Execute API|Allowed|

During testing, application developers should run all of their application scripting logic to ensure the system creates any necessary cross-scope privilege records. After application publication, the system only allows runtime requests to run that have a valid cross-scope privilege record.

**Note:** Table privilege granting is limited to, at most, the permissions set on the table object \(sys\_db\_object\) record. For example, granting a scope privilege to delete for table incident would not be allowed if the table object for incident did not allow Can delete scopes.

**Parent Topic:**[Application design and runtime settings](r_ApplicationDesignAndRuntimeSettings.md)

