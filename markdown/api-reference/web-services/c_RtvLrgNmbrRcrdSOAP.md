---
title: Retrieve a large number of records using SOAP
description: By default, a single SOAP request can retrieve a maximum of 250 records.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Retrieve a large number of records using SOAP

By default, a single SOAP request can retrieve a maximum of 250 records.

SOAP relies on Extensible Markup Language \(XML\) as its message format, and usually relies on other Application Layer protocols \(most notably Remote Procedure Call \(RPC\) and HTTP\) for message negotiation and transmission. SOAP can form the foundation layer of a web services protocol stack, providing a basic messaging framework upon which web services can be built.

Because of the verbose XML format, SOAP can be considerably slower than other transport methods. Therefore, sending a large amount of data via SOAP is inefficient and is discouraged. Because of this, ServiceNow has imposed a hard-limit of 250 records that can be retrieved at any time in a single query. You may find that this limit poses some technological challenges for your integration design.

-   **[SOAP strategies](c_SOAPStrategies.md)**  
Retrieve the information that you need and make your integration more efficient.

**Parent Topic:**[SOAP web service](../../inbound-soap/concept/c_SOAPWebService.md)

