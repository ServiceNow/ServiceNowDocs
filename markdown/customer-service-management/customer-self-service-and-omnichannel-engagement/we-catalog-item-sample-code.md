---
title: Sample code for the Catalog item component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Catalog item component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Catalog item component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_CATALOG_ITEM_FORM#COMPONENT_NOTIFICATION_SENT' : (e) => { 

// This event is dispatched when the component provides a notification for the end user. 

var {items} = e.detail.payload; 

console.log(items); 

}, 

'SN_EMBEDX_CATALOG_ITEM_FORM#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

}, 

'SN_EMBEDX_CATALOG_ITEM_FORM#RECORD_CREATION_SUCCEEDED' : (e) => { 

// This event is dispatched if the record was successfully created. 

var {table, record_sys_id} = e.detail.payload; 

console.log(table, record_sys_id); 

}, 

'SN_EMBEDX_CATALOG_ITEM_FORM#BUTTON_CLICKED' : (e) => { 

// This event is dispatched if any button is clicked on the confirmation message. 

var {table, record_sys_id, button_variant} = e.detail.payload; 

var primaryURL = '/caseview'; // Replace with the URL of the case view page 

var secondaryURL = '/browse'; // Replace with the URL of the secondary page 

 

if(button_variant == 'primary') { 

// Construct the URL for the Case View component with URL parameters 

const caseViewURL = primaryURL+'?emb_table='+table+'&emb_recordid='+record_sys_id; 

open(caseViewURL,'_self'); // Open case record when primary button is clicked 

} 

else { 

// Open the Case View component in the same tab 

open(secondaryURL,'_self'); 

} 

}, 

'SN_EMBEDX_CATALOG_ITEM_FORM#RECORD_CREATION_FAILED' : (e) => { 

// This event is dispatched if the record creation has failed. 

}, 

'SN_EMBEDX_CATALOG_ITEM_FORM#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}
```

**Related topics**  


[Configure the Catalog item component instance](../task/configure-catalog-item-component-on-instance.md)

[Embed the Catalog item component instance on the third-party website](../task/embed-catalog-item-component-on-third-party-website.md)

[Component properties for the Catalog item](component-properties-for-catalog-item.md)

[Event handler in the Catalog item component](we-catalog-item-event-handler.md)

