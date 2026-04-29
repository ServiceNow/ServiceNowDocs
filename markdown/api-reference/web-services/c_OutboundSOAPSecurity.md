---
title: Outbound SOAP security
description: You can authenticate outbound SOAP messages using several different security protocols.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Outbound SOAP security

You can authenticate outbound SOAP messages using several different security protocols.

The security protocol you should use depends on the requirements of the web service provider. Mutual authentication is supported for outbound web services.

-   **[Enable basic authentication for outbound SOAP](../task/t_BasicAuthentication.md)**  
If the endpoint requires a user name and password, you can provide credentials using basic authentication.
-   **[Enable WS-Security for outbound SOAP](../task/t_WebServiceSecurity.md)**  
You can sign outbound SOAP messages using username and password or a key store and trusted server certificate saved on the instance.

**Parent Topic:**[Outbound SOAP web service](c_OutboundSOAPWebService.md)

