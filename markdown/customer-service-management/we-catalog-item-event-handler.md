---
title: Event handler in the Catalog item component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the Catalog item component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

|Event handler|Description|Payload|
|-------------|-----------|-------|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#COMPONENT\_READY**|This event is dispatched when a component is ready and usable.|N/A|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#COMPONENT\_ERROR**|This event is dispatched when a property validation or internal error occurs.|`errorMessage, errorType`|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#BUTTON\_CLICKED**|This event is dispatched if any button is selected the confirmation message.|`table, record_sys_id, button_variant`|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#RECORD\_CREATION\_SUCCEEDED**|This event is dispatched if the record was successfully created.|`table, record_sys_id`|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#RECORD\_CREATION\_FAILED**|This event is dispatched if the record creation has failed.|N/A|
|**SN\_EMBEDX\_CATALOG\_ITEM\_FORM** **\#COMPONENT\_NOTIFICATION\_SENT**|This event is dispatched when the component provides a notification for the end user.|`items`|

**Related topics**  


[Configure the Catalog item component instance](../task/configure-catalog-item-component-on-instance.md)

[Embed the Catalog item component instance on the third-party website](../task/embed-catalog-item-component-on-third-party-website.md)

[Component properties for the Catalog item](component-properties-for-catalog-item.md)

[Sample code for the Catalog item component](we-catalog-item-sample-code.md)

