---
title: Event handler in the Data visualization component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web Embeddables event handlers, Web Embeddables reference, Reference, Customer Service Management]
---

# Event handler in the Data visualization component

A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.

<table id="table_rvc_k3n_c2c"><thead><tr><th>

Event handler

</th><th>

Description

</th><th>

Payload

</th></tr></thead><tbody><tr><td>

**NOW\_VIS\_WRAPPER\#PROPERTY\_OVERRIDE**

</td><td>

This event is dispatched when the visualization overrides its property.For example, when the user selects a different group by from the alternative group by selection.

</td><td>

`properties`

</td></tr><tr><td>

**NOW\_VIS\_WRAPPER\#SELECTED**

</td><td>

This event is dispatched when the user selects order-selects element on data visualizations, typically to filter other content on the page.

</td><td>

`title, type, isSelected, params, data`

</td></tr><tr><td>

**NOW\_VIS\_WRAPPER\#CLICKED**

</td><td>

This event is dispatched when the visualization is selected.

</td><td>

`title, type, params, data`

</td></tr></tbody>
</table>**Related topics**  


[Configure the Data visualization component instance](../task/config-data-viz-comp.md)

[Embed the Data visualization component instance on the third-party website](../task/embed-data-viz-comp.md)

[Component properties for the Data visualization](we-data-viz-comp-prop.md)

[Sample code for the Data visualization component](we-data-viz-sample-code.md)

