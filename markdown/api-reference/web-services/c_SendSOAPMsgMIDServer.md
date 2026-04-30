---
title: Send a SOAP message through a MID server
description: When creating SOAP message functions, you can configure the function to be sent through a MID Server.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP message, Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Send a SOAP message through a MID server

When creating SOAP message functions, you can configure the function to be sent through a MID Server.

There must be a running MID Server associated with your instance to use this functionality. All SOAP messages sent through a MID Server are performed asynchronously.

![](../image/SoapMessageMid.png "Soap message mid")

By specifying a MID Server, all SOAP requests that use this SOAP message are sent through that MID Server. You can override the selected MID Server by using the setMIDServer\(mid server\) API call in a script.

**Parent Topic:**[SOAP message](c_SOAPMessage.md)

