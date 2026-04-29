---
title: SOAP message
description: Information needed to send SOAP requests is stored in SOAP message records.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# SOAP message

Information needed to send SOAP requests is stored in SOAP message records.

Each record specifies an endpoint for the request, the required format of the request as a web services description language \(WSDL\) file, authentication information, and a list of functions that can run against the endpoint.

-   **[Create a SOAP message](../task/t_CreateASOAPMessage.md)**  
Create a SOAP message to define the remote endpoint, WSDL, and authentication settings.
-   **[SOAP message functions](c_SOAPMessageFunctions.md)**  
After you create a SOAP message record, you can click **Generate sample SOAP messages** to populate the SOAP Message Functions related list.
-   **[Variable substitution in outbound SOAP](c_VariableSubstitutionSOAP.md)**  
To use variable substitution, use the format `${<variable_name>}` instead of defining a specific value.
-   **[Test the SOAP message](c_TestTheSOAPMessage.md)**  
Test a SOAP message to validate the configuration before using the message in an integration.
-   **[Send a SOAP message through a MID server](c_SendSOAPMsgMIDServer.md)**  
When creating SOAP message functions, you can configure the function to be sent through a MID Server.
-   **[Create a SOAP message from a WSDL that references an external XSD file](../task/create-soap-msg-external-xsd.md)**  
Create a SOAP message from a WSDL and external XSD file.

**Parent Topic:**[Outbound SOAP web service](c_OutboundSOAPWebService.md)

