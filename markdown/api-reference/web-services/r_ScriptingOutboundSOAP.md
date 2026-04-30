---
title: Scripting outbound SOAP
description: You can send outbound SOAP requests from any place in the ServiceNow AI Platform where scripting is allowed.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Scripting outbound SOAP

You can send outbound SOAP requests from any place in the ServiceNow AI Platform where scripting is allowed.

For detailed API information about the server-side SOAPMessageV2 and SOAPResponseV2 APIs, see the API documentation on [developer.servicenow.com](https://developer.servicenow.com/app.do#!/home). For additional tips and best practices, see the [Outbound REST Web Services RESTMessageV2 and SOAPMessageV2 execute\(\) vs executeAsync\(\) Best Practices \[KB0694711\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0694711) article in the Now Support Knowledge Base.

-   **[Preview a SOAP message script](../concept/c_UseASOAPMessageInAScript.md)**  
Generate a sample script to send the SOAP message.
-   **[Direct SOAPMessageV2 example](../../../app-store/dev_portal/API_reference/SOAPMessageV2/reference/r_DirectSOAPMessageV2Example.md)**  
You can send an outbound SOAP message directly to the endpoint.
-   **[Asynchronous SOAPMessageV2 example](../../../app-store/dev_portal/API_reference/SOAPMessageV2/reference/r_AsyncronousSOAPMessageV2Example.md)**  
You can send an outbound SOAP message asynchronously.
-   **[SOAPMessageV2 MID server example](../../../app-store/dev_portal/API_reference/SOAPMessageV2/reference/r_SOAPMessageV2MIDServerExample.md)**  
You can send an outbound SOAP message through a MID Server.
-   **[Recordless SOAPMessageV2 example](../../../app-store/dev_portal/API_reference/SOAPMessageV2/reference/r_RecordlessSOAPMessageV2Example.md)**  
You can use the SOAPMessageV2\(\) constructor with no parameters to define a SOAP message entirely in the script.

**Parent Topic:**[Outbound SOAP web service](../concept/c_OutboundSOAPWebService.md)

