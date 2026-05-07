---
title: Sample code for the Playbook intake component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbook intake component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Playbook intake component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_PLAYBOOK_INTAKE#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'SN_EMBEDX_PLAYBOOK_INTAKE#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorType, errorMessage} = e.detail.payload; 

console.log(errorType, errorMessage); 

}, 

'SN_EMBEDX_PLAYBOOK_INTAKE#RECORD_CREATION_SUCCEEDED' : (e) => { 

// Dispatched when a record is created by a Record Generator Playbook. 

var {table, sysId, number, playbook_experience_id, hide_record_creation} = e.detail.payload; 

if(hide_record_creation){ 

var primaryURL = '/caseview'; // Replace with the URL of the case view page 

 

// Construct the URL for the Case View component with URL parameters 

const caseViewURL = primaryURL + '?emb_table=' + table + '&emb_recordid=' + sysId + (playbook_experience_id === '98e09a560f2200102920c912d4767e1a' ? '' : '&emb_playbook_experience=' + playbook_experience_id); 

open(caseViewURL,'_self'); // Open case record when record created confirmation is hidden 

} 

}, 

'SN_EMBEDX_PLAYBOOK_INTAKE#PRIMARY_BUTTON_CLICKED' : (e) => { 

// This event is dispatched when primary button is clicked on the record created confirmation page. 

var {table, record_sys_id, playbook_experience_id} = e.detail.payload; 

var primaryURL = '/caseview'; // Replace with the URL of the case view page 

 

// Construct the URL for the Case View component with URL parameters 

const caseViewURL = primaryURL + '?emb_table=' + table + '&emb_recordid=' + record_sys_id + (playbook_experience_id === '98e09a560f2200102920c912d4767e1a' ? '' : '&emb_playbook_experience=' + playbook_experience_id); 

open(caseViewURL,'_self'); // Open case record when primary button is clicked 

}, 

'SN_EMBEDX_PLAYBOOK_INTAKE#SECONDARY_BUTTON_CLICKED' : (e) => { 

// This event is dispatched when secondary button is clicked on the record created confirmation page. 

var {table, record_sys_id} = e.detail.payload; 

var secondaryURL = '/browse'; // Replace with the URL of the secondary page 

 

// Open the Case View component in the same tab 

open(secondaryURL,'_self'); 

}
```

**Related topics**  


[Configure the Playbook intake component instance](../task/config-playbook-intake-comp.md)

[Embed the Playbook intake component instance on the third-party website](../task/embed-playbook-intake-comp.md)

[Component properties for the Playbook intake](we-playbook-intake-comp-prop.md)

[Event handler in the Playbook intake component](we-playbook-intake-event-handler.md)

