---
title: Sample code for the Case list component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case list component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Case list component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_CASE_LIST#RECORD_SELECTED' : (e) => { 

// This event is dispatched when a record is selected. 

var {table, record_sys_id} = e.detail.payload; 

// the logic to construct the URL for the Case View component. Add your portal URL here. 

const caseViewURL = '/caseview?emb_table='+table+'&emb_recordid='+record_sys_id; 

// Redirect to the Case view component page 

open(caseViewURL,'_self'); 

}, 

'SN_EMBEDX_CASE_LIST#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'SN_EMBEDX_CASE_LIST#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

} 
```

**Related topics**  


[Configure the Case list component instance](../task/configure-case-list-component-on-instance.md)

[Embed the Case list component instance on the third-party website](../task/embed-case-list-component-on-third-party-website.md)

[Component properties for the Case list](component-properties-for-the-case-list.md)

[Event handler in the Case list component](we-case-list-event-handlers.md)

