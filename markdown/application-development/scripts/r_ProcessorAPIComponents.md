---
title: Processor API components
description: Processors have access to dedicated API classes, objects, and methods.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Processors, Server-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# Processor API components

Processors have access to dedicated API classes, objects, and methods.

|Class, object, or method|Description|
|------------------------|-----------|
|`g_response`|An object of type HttpServletResponse. See [GlideServletResponse](https://www.servicenow.com/docs/access?context=c_GlideServletResponseScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|`setContentType(‘text/html;charset=UTF-8’)`|A [GlideServletResponse](https://www.servicenow.com/docs/access?context=c_GlideServletResponseScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) method to set the content type of the response being sent to the client.|
|`g_request`|An object of type HttpServletRequest. See [HttpServletRequest](https://www.servicenow.com/docs/access?context=c_GlideServletRequestScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|`getParameter()`|A glide method to get the value of a URL parameter.|
|`canRead()`|A GlideRecord method to determine if the user can read data from a table. See [GlideRecord](https://www.servicenow.com/docs/access?context=c_GlideRecordScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|`g_processor`|A simplified servlet for processors. See [GlideScriptedProcessor](https://www.servicenow.com/docs/access?context=c_GlideScriptedProcessorScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).|
|`writeOutput()`|A [GlideScriptedProcessor](https://www.servicenow.com/docs/access?context=c_GlideScriptedProcessorScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US) method to display information on the client.|
|`g_target`|An object containing the target table name of a processor URL. For example, a processor containing the URI `incident.do` applies to the Incident table.|

**Parent Topic:**[Processors](../concept/c_Processors.md)

