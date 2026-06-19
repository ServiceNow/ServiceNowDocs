---
title: Processor API components
description: Processors have access to dedicated API classes, objects, and methods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/r\_ProcessorAPIComponents.html
release: australia
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Processor API components

Processors have access to dedicated API classes, objects, and methods.

|Class, object, or method|Description|
|------------------------|-----------|
|`g_response`|An object of type HttpServletResponse. See [GlideServletResponse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideServletResponseScopedAPI.md).|
|`setContentType(‘text/html;charset=UTF-8’)`|A [GlideServletResponse](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideServletResponseScopedAPI.md) method to set the content type of the response being sent to the client.|
|`g_request`|An object of type HttpServletRequest. See [HttpServletRequest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideServletRequestScopedAPI.md).|
|`getParameter()`|A glide method to get the value of a URL parameter.|
|`canRead()`|A GlideRecord method to determine if the user can read data from a table. See [GlideRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideRecordScopedAPI.md).|
|`g_processor`|A simplified servlet for processors. See [GlideScriptedProcessor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideScriptedProcessorScopedAPI.md).|
|`writeOutput()`|A [GlideScriptedProcessor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/server-api-reference/c_GlideScriptedProcessorScopedAPI.md) method to display information on the client.|
|`g_target`|An object containing the target table name of a processor URL. For example, a processor containing the URI `incident.do` applies to the Incident table.|

**Parent Topic:**[Processors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_Processors.md)

