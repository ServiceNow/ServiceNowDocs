---
title: Scripting outbound SOAP
description: You can send outbound SOAP requests from any place in the ServiceNow AI Platform where scripting is allowed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/r\_ScriptingOutboundSOAP.html
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Scripting outbound SOAP

You can send outbound SOAP requests from any place in the ServiceNow AI Platform where scripting is allowed.

For detailed API information about the server-side SOAPMessageV2 and SOAPResponseV2 APIs, see the API documentation on [developer.servicenow.com](https://developer.servicenow.com/app.do#!/home). For additional tips and best practices, see the [Outbound REST Web Services RESTMessageV2 and SOAPMessageV2 execute\(\) vs executeAsync\(\) Best Practices \[KB0694711\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0694711) article in the Now Support Knowledge Base.

-   **[Preview a SOAP message script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_UseASOAPMessageInAScript.md)**  
Generate a sample script to send the SOAP message.
-   **[Direct SOAPMessageV2 example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/r_DirectSOAPMessageV2Example.md)**  
You can send an outbound SOAP message directly to the endpoint.
-   **[Asynchronous SOAPMessageV2 example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/r_AsyncronousSOAPMessageV2Example.md)**  
You can send an outbound SOAP message asynchronously.
-   **[SOAPMessageV2 MID server example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/r_SOAPMessageV2MIDServerExample.md)**  
You can send an outbound SOAP message through a MID Server.
-   **[Recordless SOAPMessageV2 example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/r_RecordlessSOAPMessageV2Example.md)**  
You can use the SOAPMessageV2\(\) constructor with no parameters to define a SOAP message entirely in the script.

**Parent Topic:**[Outbound SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_OutboundSOAPWebService.md)

