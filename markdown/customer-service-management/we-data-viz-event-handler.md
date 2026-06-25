---
title: Event handler in the Data visualization component
description: A component triggers an event when a certain condition is met or on user interaction. The event can be used to execute an action through a code on a third-party webpage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/we-data-viz-event-handler.html
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


[Configure the Data visualization component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/config-data-viz-comp.md)

[Embed the Data visualization component instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-data-viz-comp.md)

[Component properties for the Data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/we-data-viz-comp-prop.md)

[Sample code for the Data visualization component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/we-data-viz-sample-code.md)

