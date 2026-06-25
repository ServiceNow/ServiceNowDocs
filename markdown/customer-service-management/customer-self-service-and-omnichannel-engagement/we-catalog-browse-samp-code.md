---
title: Sample code for the Catalog browse component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/we-catalog-browse-samp-code.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Catalog browse component, Configure web components, Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Catalog browse component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'CATALOG_BROWSE#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'CATALOG_BROWSE#CATALOG_ITEM_SELECTED' : (e) => { 

// This event is dispatched when a catalog item is selected. 

var {catalog_item_details} = e.detail.payload; 

// Logic to construct the URL based on the catalog item details 

let redirectURL; 

const type = catalog_item_details.type; 

 

if (type === 'catalog_item' || type === 'record_producer') { 

redirectURL = '/catalog_form?emb_recordid=' + catalog_item_details.sys_id; 

} else if (type === 'content_item') { 

const content_type = catalog_item_details.content_type; 

if (content_type === 'kb') { 

redirectURL = '/article_view?emb_recordid=' + catalog_item_details.kb_article; 

} else if (content_type === 'external') { 

redirectURL = catalog_item_details.url; 

} else if (content_type === 'dynamic') { 

const dynamicContentItemDetails = catalog_item_details.dynamicContentItemDetails; 

// Check for 'Playbook' dynamic content type 

if(dynamicContentItemDetails.dynamicContentType === 'c0e6a71443923110f6669c7385b8f20a') 

redirectURL = '/playbook_intake?emb_playbook_title=' + dynamicContentItemDetails.content.title + '&emb_table=' + dynamicContentItemDetails.content.table + '&emb_record_generator=' + dynamicContentItemDetails.content.query + '&emb_playbook_experience=' + dynamicContentItemDetails.content.playbook_experience; 

} 

} 

// Redirect to the respective component page 

open(redirectURL, '_self'); 

}, 

'CATALOG_BROWSE#COMPONENT_EMPTY' : (e) => { 

// This event is dispatched when a component has nothing to display. 

}, 

'CATALOG_BROWSE#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a component encounters an error. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

} 

 
```

**Related topics**  


[Configure the Catalog browse component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/we-config-catalog-browse-comp.md)

[Embed the Catalog browse component on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/we-embed-catalog-browse-on-third-party-web.md)

[Component properties for the Catalog browse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/we-catalog-browse-comp-prop.md)

[Event handlers in the Catalog browse component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/we-event-handlers-catalog-browse.md)

