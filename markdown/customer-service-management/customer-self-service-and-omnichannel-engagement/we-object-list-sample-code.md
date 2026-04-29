---
title: Sample code for the Object list component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Object list component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Object list component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_OBJECT_LIST#FOOTER_LINK_SELECTED' : (e) => { 

// This event is dispatched when footer link is selected 

var {table, view, edit_query, nest_by} = e.detail.payload; 

const objectListURL = '/objectlist?emb_table=' + table + '&emb_query=' + edit_query + '&emb_view=' + view + '&emb_nestby=' + nest_by; 

// Open the Record List component in the same tab 

open(objectListURL, '_self'); 

}, 

'SN_EMBEDX_OBJECT_LIST#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

}, 

'SN_EMBEDX_OBJECT_LIST#RECORD_SELECTED' : (e) => { 

// This event is dispatched when a record is selected. 

var {table, record_sys_id} = e.detail.payload; 

 

var RecordViewURL; 

if(table == 'sn_customerservice_case'){ 

RecordViewURL = '/caseview?emb_table=' + table + '&emb_recordid=' + record_sys_id; 

} else { 

RecordViewURL = '/recordview?emb_table=' + table + '&emb_recordid=' + record_sys_id; 

} 

open(RecordViewURL, '_self'); 

}, 

'SN_EMBEDX_OBJECT_LIST#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

} 
```

