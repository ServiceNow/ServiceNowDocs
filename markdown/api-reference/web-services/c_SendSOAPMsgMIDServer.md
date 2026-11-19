---
title: Send a SOAP message through a MID server
description: When creating SOAP message functions, you can configure the function to be sent through a MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_SendSOAPMsgMIDServer.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Messages, SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Send a SOAP message through a MID server

When creating SOAP message functions, you can configure the function to be sent through a MID Server.

There must be a running MID Server associated with your instance to use this functionality. All SOAP messages sent through a MID Server are performed asynchronously.

\[Omitted image "SoapMessageMid.png"\] Alt text:

By specifying a MID Server, all SOAP requests that use this SOAP message are sent through that MID Server. You can override the selected MID Server by using the setMIDServer\(mid server\) API call in a script.

**Parent Topic:**[SOAP message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_SOAPMessage.md)

