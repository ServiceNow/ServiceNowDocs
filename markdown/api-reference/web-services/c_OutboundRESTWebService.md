---
title: Outbound REST web service
description: ServiceNow outbound REST functionality allows you to retrieve, create, update, or delete data on a web services server that supports the REST architecture.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Outbound, Web services, API implementation, API implementation and reference]
---

# Outbound REST web service

ServiceNow outbound REST functionality allows you to retrieve, create, update, or delete data on a web services server that supports the REST architecture.

A REST message can be sent by a REST workflow activity or by using the RESTMessageV2 script API. You can run REST messages from a MID Server which allows the message to communicate with REST providers on an internal network.

ServiceNow REST functionality is flexible enough to accommodate many web service APIs. Be sure you are familiar with your web service and the parameters it accepts before attempting to define a REST message in ServiceNow.

-   **[REST message elements](../reference/r_RESTMessageElements.md)**  
An outbound REST message is composed of several elements, such as the endpoint and HTTP methods.
-   **[Create a REST message](../task/t_ConfiguringARESTMessage.md)**  
Send requests to a REST web service endpoint by creating a REST message record.
-   **[Outbound REST authentication](c_OutboundRESTAuth.md)**  
Outbound REST messages support multiple types of authentication.
-   **[Variable substitution in outbound REST messages](c_VariableSubstitutionREST.md)**  
You can use variables when creating outbound REST messages and assign values to those variables when performing a request.
-   **[Scripting outbound REST](c_ScriptingOutboundREST.md)**  
You can send outbound REST requests from any place in the ServiceNow AI Platform where scripting is allowed.

**Parent Topic:**[Outbound web services](../../outbound-web-services/concept/outbound-web-services.md)

