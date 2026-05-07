---
title: Sample code for the Data visualization component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data visualization component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Data visualization component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'NOW_VIS_WRAPPER#PROPERTY_OVERRIDE' : (e) => { 

// Dispatched when the visualization overrides its property. For example when the user selects a different group by from the alternative group by selection 

var {properties} = e.detail.payload; 

console.log(properties); 

}, 

'NOW_VIS_WRAPPER#SELECTED' : (e) => { 

// Dispatched when the user selects/de-selects element on data visualizations, typically to filter other content on the page 

var {title, type, isSelected, params, data} = e.detail.payload; 

console.log(title, type, isSelected, params, data); 

}, 

'NOW_VIS_WRAPPER#CLICKED' : (e) => { 

// Dispatched when the visualization is clicked 

var {title, type, params, data} = e.detail.payload; 

console.log(title, type, params, data); 

}
```

**Related topics**  


[Configure the Data visualization component instance](../task/config-data-viz-comp.md)

[Embed the Data visualization component instance on the third-party website](../task/embed-data-viz-comp.md)

[Component properties for the Data visualization](we-data-viz-comp-prop.md)

[Event handler in the Data visualization component](we-data-viz-event-handler.md)

