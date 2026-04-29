---
title: Sample code to handle the Case view component
description: Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Case view component, Configure web components, Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Sample code to handle the Case view component

Sample code is provided to define an action when an event is triggered. Update the sample code for your use case before embedding the component on your webpage.

## Sample code

```
{ 

'SN_EMBEDX_CASE_VIEW#COMPONENT_READY' : (e) => { 

// This event is dispatched when a component is ready and usable. 

}, 

'SN_EMBEDX_CASE_VIEW#COMPONENT_ERROR' : (e) => { 

// This event is dispatched when a property validation or internal error occurs. 

var {errorMessage, errorType} = e.detail.payload; 

console.log(errorMessage, errorType); 

}, 

'SN_EMBEDX_CASE_VIEW#CASE_COMMENT_ADDED' : (e) => { 

// This event is dispatched when a comment is added in the activity stream. }
	};

	setEvents(snEmbedxCaseView, eventHandlers);
</script>
```

**Related topics**  


[Configure the Case view component instance](../task/configure-case-view-component-on-instance.md)

[Embed the Case view component instance on the third-party website](../task/embed-case-view-comp-on-third-party-website.md)

[Component properties for the Case view](component-properties-for-case-view-comp.md)

[Event handler in the enhanced Case view component](we-case-view-event-handler.md)

