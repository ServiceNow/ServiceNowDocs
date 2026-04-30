---
title: Scripting outbound REST
description: You can send outbound REST requests from any place in the ServiceNow AI Platform where scripting is allowed.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Scripting outbound REST

You can send outbound REST requests from any place in the ServiceNow AI Platform where scripting is allowed.

For example, you can return data from a REST endpoint using a business rule when an event is triggered. Create a script from scratch or let the REST message preview feature create the script based on content and parameters you provide in the method record.

For detailed API information about the server-side RESTMessageV2 and RESTResponseV2 APIs, see the API documentation on [developer.servicenow.com](https://developer.servicenow.com/app.do#!/home). For additional tips and best practices, see the [Outbound REST Web Services RESTMessageV2 and SOAPMessageV2 execute\(\) vs executeAsync\(\) Best Practices \[KB0694711\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0694711) article in the Now Support Knowledge Base.

-   **[Generate a REST message script preview](../task/t_ScriptingWithREST.md)**  
You can generate an example script to send a REST message based on content and parameters you provide in the method record.
-   **[Direct RESTMessageV2 example](../../../app-store/dev_portal/API_reference/RESTMessageV2/reference/r_DirectRESTMessageV2Example.md)**  
You can send an outbound REST message directly to the endpoint.
-   **[RESTMessageV2 MID server example](../../../app-store/dev_portal/API_reference/RESTMessageV2/reference/r_RESTMessageV2MIDServerExample.md)**  
You can send an outbound REST message through a MID Server.
-   **[Recordless RESTMessageV2 example](../../../app-store/dev_portal/API_reference/RESTMessageV2/reference/r_RecordlessRESTMessageV2Example.md)**  
You can use the RESTMessageV2\(\) constructor with no parameters to define a REST message entirely in the script.

**Parent Topic:**[Outbound REST web service](c_OutboundRESTWebService.md)

