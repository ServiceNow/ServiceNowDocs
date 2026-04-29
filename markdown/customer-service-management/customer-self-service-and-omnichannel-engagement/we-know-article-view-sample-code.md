---
title: Sample code for the Knowledge article view component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge article view component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code for the Knowledge article view component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#LINK_CLICKED' : (e) => { 

// This event is dispatched when a record link has been clicked inside article body 

var {table, sys_id} = e.detail.payload; 

console.log(table, sys_id); 

}, 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#LANGUAGE_DROPDOWN_CLICKED' : (e) => { 

// This event is dispatched when language dropdown selection is clicked 

var {articleID} = e.detail.payload; 

 

// Set properties for the knowledge article view 

setProperties(snEmbedxKbArticleView, {recordId: articleID}); 

}, 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#NOTIFICATION_LINK_CLICKED' : (e) => { 

// This event is dispatched when link present on notification has been clicked 

var {table, sys_id} = e.detail.payload; 

 

if(table == 'kb_knowledge') { 

// Set properties for the knowledge article view 

setProperties(snEmbedxKbArticleView, {recordId: sys_id}); 

} 

}, 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#RATING_CLICKED' : (e) => { 

// This event is dispatched when rating is provided for the article 

var {rating} = e.detail.payload; 

console.log(rating); 

}, 

'SN_EMBEDX_KNOWLEDGE_ARTICLE_VIEW#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

}
```

**Related topics**  


[Configure the Knowledge article view component instance](../task/config-know-article-view-comp.md)

[Embed the Knowledge article view component instance on the third-party website](../task/embed-know-article-view-comp.md)

[Component properties for the Knowledge article view](we-know-article-view-comp-prop.md)

[Event handler in the Knowledge article view component](we-know-article-view-event-handler.md)

