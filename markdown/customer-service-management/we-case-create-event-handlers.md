---
title: Event handlers in the Case create component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handlers in the Case create component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

|Event handler|Description|Payload|
|-------------|-----------|-------|
|**SN\_EMBEDX\_CASE\_FORM\#COMPONENT\_READY**|This event is dispatched when a component is ready and usable.|None|
|**SN\_EMBEDX\_CASE\_FORM\#COMPONENT\_ERROR**|This event is dispatched when a property validation or internal error occurs.|`errorMessage, errorType`|
|**SN\_EMBEDX\_CASE\_FORM\#BUTTON\_CLICKED**|This event is dispatched if any button is selected the confirmation message.|`table, record_sys_id, button_variant`|
|**SN\_EMBEDX\_CASE\_FORM\#RECORD\_CREATION\_SUCCEEDED**|This event is dispatched if the record was successfully created.|`table, record_sys_id`|
|**SN\_EMBEDX\_CASE\_FORM\#RECORD\_CREATION\_FAILED**|This event is dispatched if the record creation has failed.|None|
|**SN\_EMBEDX\_CASE\_FORM\#COMPONENT\_NOTIFICATION\_SENT**|This event is dispatched when the component provides a notification for the end user.|`item`|

**Related topics**  


[Configure the Case create component instance](../task/config-case-create-component-on-instance.md)

[Embed the Case create component instance on the third-party website](../task/embed-case-create-component-on-third-party-website.md)

[Component properties for the Case create](comp-properties-case-create.md)

[Sample code for the Case create component](we-case-create-sample-code.md)

