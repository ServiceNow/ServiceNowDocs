---
title: Event handler in the enhanced Case view component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the enhanced Case view component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on third-party webpage.

|Event handler|Description|Payload|
|-------------|-----------|-------|
|**SN\_EMBEDX\_CASE\_VIEW\#COMPONENT\_READY**|This event is dispatched when a component is ready and usable.|None|
|**SN\_EMBEDX\_CASE\_VIEW\#COMPONENT\_ERROR**|This event is dispatched when a property validation or internal error occurs.|`errorMessage, errorType`|
|**SN\_EMBEDX\_CASE\_VIEW\#CASE\_COMMENT\_ADDED**|This event is dispatched when a comment is added in the activity stream.|None|
|**SN\_EMBEDX\_CASE\_VIEW\#RELATED\_RECORD\_SELECTED**|This event is dispatched when a record of related list is selected.|`table, record_sys_id, reference_table, reference_record_sys_id`|
|Additional events|
|**SN\_EMBEDX\_CASE\_VIEW\#ACTIVITY\_SELECTED**|This event is dispatched when an activity is selected.|`playbookContextId, stageContextId, activityContextId`|
|**SN\_EMBEDX\_CASE\_VIEW\#STAGE\_SELECTED**|This event is dispatched when a stage is selected.|`playbookContextId, stageContextId`|
|**SN\_EMBEDX\_CASE\_VIEW\#FILTER\_OPTION\_SELECTED**|This event is dispatched when a filter option is selected.|`playbookContextId, item`|
|**SN\_EMBEDX\_CASE\_VIEW\#ACTIVITY\_STATE\_CHANGED**|This event is dispatched when the activity's state changes.|`playbookContextId, stageContextId, activityContextId`|
|**SN\_EMBEDX\_CASE\_VIEW\#OPEN\_RECORD**|This event is dispatched when an open record event is fired.|`table, sys_id, params, query`|
|**SN\_EMBEDX\_CASE\_VIEW\#PLAYBOOK\_EXPANDED**|This event is dispatched when the playbook chevron is expanded.|`playbookContextId, updatedExpandState`|
|**SN\_EMBEDX\_CASE\_VIEW\#UPDATE\_SELECTION**|This event is dispatched when an activity is completed.|`selectedPlaybook, selectedStage, selectedActivity`|
|**SN\_EMBEDX\_CASE\_VIEW\#OPEN\_LIST**|This event is dispatched when an open list event is fired.|`table, listTitle, query, disableInlineEditing, listView`|
|**SN\_EMBEDX\_CASE\_VIEW\#USER\_INTERACTION**|This event is dispatched when the user interacts with any element on playbook.|`playbookContextId, parentTable, parentRecord, stageName, stageTitle, stageState, activityTitle, activityContextId, associatedRecord, associatedTable`|
|**SN\_EMBEDX\_CASE\_VIEW\#FILTER\_SELECTED**|This event is dispatched when a filter is selected.|`playbookContextId, value`|

