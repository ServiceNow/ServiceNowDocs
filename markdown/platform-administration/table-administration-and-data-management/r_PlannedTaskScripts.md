---
title: Planned task scripts
description: Several business rules and one script include determines the dynamic calculation of crucial Planned Task fields.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Planned tasks, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Planned task scripts

Several business rules and one script include determines the dynamic calculation of crucial Planned Task fields.

|Business Rule|Description|
|-------------|-----------|
|Set actual work start value|Sets the Actual Start Date of the planned task when State is set to the default work state.|
|Set close data on inactive|Sets the close data of the planned task when task becomes inactive.|
|Recalculate|Recalculates the planned task schedule fields when one of the schedule fields changes.|
|Planned task global events|Raises global event for every insert or update of planned task record. For more information, see [Global events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/system-events/r_GlobalEvents.md).|
|Update parent actual effort|Rolls up actual effort from child task to parent task.|
|Update parent effort|Rolls up planned effort from child task to parent task.|
|Update parent percent complete|Rolls up percent complete from child task to parent task.|
|Validate duration|Validates the value in the planned duration field is not 0 or negative.|
|Validate percent complete|Validates the value in the percent complete field is between 0 and 100.|
|Validate work end before work start|Validates that the actual end date is not earlier than the actual start date.|
|Set top task|Sets top tasks to maintain hierarchy of tasks.|
|Set top task on children|Sets top tasks on child tasks to maintain hierarchy of tasks.|

**Parent Topic:**[Extending the Task table with Planned tasks](../concept/c_PlannedTask.md)

