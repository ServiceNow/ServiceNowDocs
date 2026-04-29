---
title: Event handler in the Playbook intake component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the Playbook intake component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

|Event handler|Description|Payload|
|-------------|-----------|-------|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#COMPONENT\_READY**|This event is dispatched when a component is ready and usable.|None|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#COMPONENT\_ERROR**|This event is dispatched when a property validation or internal error occurs.|`errorType, errorMessage`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#RECORD\_CREATION\_SUCCEEDED**|This event is dispatched when a record is created by a Record Generator Playbook.|`table, sysId, number, playbook_experience_id, hide_record_creation`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#PRIMARY\_BUTTON\_CLICKED**|This event is dispatched when the primary button is selected the record created confirmation page.|`table, record_sys_id, playbook_experience_id`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#SECONDARY\_BUTTON\_CLICKED**|This event is dispatched when the secondary button is selected on the record created confirmation page.|`table, record_sys_id`|
|Additional event handlers|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#OPEN\_LIST**|This event is dispatched when an open list event is fired.|`table, listTitle, query, disableInlineEditing, listView`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#ACTIVITY\_SELECTED**|Select the provided playbook, stage, and activity by context ID.|`playbookContextId, stageContextId, activityContextId`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#ACTIVITY\_STATE\_CHANGED**|This event is dispatched by Playbook Custom Layout Controller when playbook activity state has changed to either Complete, Skipped, canceled, or Error.|`playbookContextId, stageContextId, activityContextId`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#STAGE\_SELECTED**|Select the provided playbook and stage by context ID.|`playbookContextId, stageContextId`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#UPDATE\_SELECTION**|This event is dispatched by the Playbook Custom Layout Controller when the selected state of a playbook, stage, or activity has changed.|`selectedPlaybook, selectedStage, selectedActivity`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#FILTER\_SELECTED**|This event is dispatched when playbook filter is opened or closed.|`playbookContextId, value`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#USER\_INTERACTION**|This event is dispatched on User interaction with a Playbook Activity.|`playbookContextId, parentTable, parentRecord, stageName, stageTitle, stageState, activityTitle, activityContextId, associatedTable, associatedRecord`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#OPEN\_RECORD**|This event is dispatched when an open record event is fired.|`table, sys_id, params, query`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#FILTER\_OPTION\_SELECTED**|This event is dispatched when an item is selected the playbook filter.|`playbookContextId, item`|
|**SN\_EMBEDX\_PLAYBOOK\_INTAKE** **\#PLAYBOOK\_EXPANDED**|This event is dispatched when the playbook stage list changes expanded state.|`playbookContextId, updatedExpandState`|

**Related topics**  


[Configure the Playbook intake component instance](../task/config-playbook-intake-comp.md)

[Embed the Playbook intake component instance on the third-party website](../task/embed-playbook-intake-comp.md)

[Component properties for the Playbook intake](we-playbook-intake-comp-prop.md)

[Sample code for the Playbook intake component](we-playbook-intake-sample-code.md)

