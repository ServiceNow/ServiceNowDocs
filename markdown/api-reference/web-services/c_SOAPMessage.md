---
title: SOAP message
description: Information needed to send SOAP requests is stored in SOAP message records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_SOAPMessage.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# SOAP message

Information needed to send SOAP requests is stored in SOAP message records.

Each record specifies an endpoint for the request, the required format of the request as a web services description language \(WSDL\) file, authentication information, and a list of functions that can run against the endpoint.

-   **[Create a SOAP message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/t_CreateASOAPMessage.md)**  
Create a SOAP message to define the remote endpoint, WSDL, and authentication settings.
-   **[SOAP message functions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_SOAPMessageFunctions.md)**  
After you create a SOAP message record, you can click **Generate sample SOAP messages** to populate the SOAP Message Functions related list.
-   **[Variable substitution in outbound SOAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_VariableSubstitutionSOAP.md)**  
To use variable substitution, use the format `${<variable_name>}` instead of defining a specific value.
-   **[Test the SOAP message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_TestTheSOAPMessage.md)**  
Test a SOAP message to validate the configuration before using the message in an integration.
-   **[Send a SOAP message through a MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_SendSOAPMsgMIDServer.md)**  
When creating SOAP message functions, you can configure the function to be sent through a MID Server.
-   **[Create a SOAP message from a WSDL that references an external XSD file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/create-soap-msg-external-xsd.md)**  
Create a SOAP message from a WSDL and external XSD file.

**Parent Topic:**[Outbound SOAP web service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_OutboundSOAPWebService.md)

