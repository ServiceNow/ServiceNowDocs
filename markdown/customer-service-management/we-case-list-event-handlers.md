---
title: Event handler in the Case list component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the Case list component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

<table id="table_csm_base_entities"><thead><tr><th>

Event handler

</th><th>

Description

</th><th>

Payload

</th></tr></thead><tbody><tr><td>

**SN\_EMBEDX\_CASE\_LIST\#RECORD\_SELECTED**

</td><td>

This event is dispatched when a record is selected.**Note:** If the first column is the reference column, selecting the case record shows the error in the Case view component.

</td><td>

`table, record_sys_id`

</td></tr><tr><td>

**SN\_EMBEDX\_CASE\_LIST\#COMPONENT\_READY**

</td><td>

This event is dispatched when a component is ready and usable.

</td><td>

None

</td></tr><tr><td>

**SN\_EMBEDX\_CASE\_LIST\#COMPONENT\_ERROR**

</td><td>

This event is dispatched when a property validation or internal error occurs.

</td><td>

`errorMessage, errorType`

</td></tr></tbody>
</table>**Related topics**  


[Configure the Case list component instance](../task/configure-case-list-component-on-instance.md)

[Embed the Case list component instance on the third-party website](../task/embed-case-list-component-on-third-party-website.md)

[Component properties for the Case list](component-properties-for-the-case-list.md)

[Sample code for the Case list component](we-case-list-sample-code.md)

