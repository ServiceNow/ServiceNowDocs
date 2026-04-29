---
title: Event handler in the Knowledge article view component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the Knowledge article view component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

|Event handler|Description|Payload|
|-------------|-----------|-------|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#LANGUAGE\_DROPDOWN\_CLICKED**|This event is dispatched when the user selects a language or version from the drop-down to open another article.|`articleID`|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#RATING\_CLICKED**|This event is dispatched when the user provides a star rating for the article.|`rating`|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#LINK\_CLICKED**|This event is dispatched when a link within the article body is selected.|`table, sys_id`|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#COMPONENT\_ERROR**|This event is dispatched when an error occurs while loading the article content.|`errorMessage, errorType`|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#COMPONENT\_READY**|This event is dispatched when the component is ready and usable.|None|
|**SN\_EMBEDX\_KNOWLEDGE\_ARTICLE\_VIEW** **\#NOTIFICATION\_LINK\_CLICKED**|This event is dispatched when link present on notification has been selected.|`table, sys_id`|

**Related topics**  


[Configure the Knowledge article view component instance](../task/config-know-article-view-comp.md)

[Embed the Knowledge article view component instance on the third-party website](../task/embed-know-article-view-comp.md)

[Component properties for the Knowledge article view](we-know-article-view-comp-prop.md)

[Sample code for the Knowledge article view component](we-know-article-view-sample-code.md)

