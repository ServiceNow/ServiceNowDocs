---
title: Sample code for the Case create component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case create component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Case create component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_CASE_FORM#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

}, 

'SN_EMBEDX_CASE_FORM#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'SN_EMBEDX_CASE_FORM#BUTTON_CLICKED' : (e) => { 

// This event is dispatched if any button is clicked on the confirmation message. 

var {table, record_sys_id, button_variant} = e.detail.payload; 

var primaryURL = '/caseview'; // Replace with the URL of the case view page 

var secondaryURL = '/browse'; // Replace with the URL of the secondary page 

 

if(button_variant == 'primary') { 

// Construct the URL for the Case view component with URL parameters 

const caseViewURL = primaryURL+'?emb_table='+table+'&emb_recordid='+record_sys_id; 

open(caseViewURL,'_self'); // Open case record when primary button is clicked 

} 

else { 

// Open the Case View component in the same tab 

open(secondaryURL,'_self'); 

} 

}, 

'SN_EMBEDX_CASE_FORM#RECORD_CREATION_SUCCEEDED' : (e) => { 

// This event is dispatched if the record was successfully created. 

var {table, record_sys_id} = e.detail.payload; 

console.log(table, record_sys_id); 

}, 

'SN_EMBEDX_CASE_FORM#RECORD_CREATION_FAILED' : (e) => { 

// This event is dispatched if the record creation has failed. 

}, 

'SN_EMBEDX_CASE_FORM#COMPONENT_NOTIFICATION_SENT' : (e) => { 

// This event is dispatched when the component provides a notification for the end user. 

var {items} = e.detail.payload; 

console.log(items); 

} 
```

**Related topics**  


[Configure the Case create component instance](../task/config-case-create-component-on-instance.md)

[Embed the Case create component instance on the third-party website](../task/embed-case-create-component-on-third-party-website.md)

[Event handlers in the Case create component](we-case-create-event-handlers.md)

[Component properties for the Case create](comp-properties-case-create.md)

