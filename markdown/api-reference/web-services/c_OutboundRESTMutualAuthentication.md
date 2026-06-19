---
title: Outbound REST mutual authentication
description: Mutual authentication causes the web service provider and consumer to authenticate with each other before communicating.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/c\_OutboundRESTMutualAuthentication.html
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound REST authentication, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Outbound REST mutual authentication

Mutual authentication causes the web service provider and consumer to authenticate with each other before communicating.

Mutual authentication verifies the identity of both the client and the server during an outbound REST connection.

When ServiceNow initiates an outbound REST request using mutual authentication, it presents a client certificate to the external server. The server validates the certificate and, if trusted, allows the connection to proceed. ServiceNow similarly validates the server certificate before completing the handshake.

Mutual authentication requires a client certificate and private key stored on the ServiceNow instance, and a server certificate issued by a trusted certificate authority \(CA\).

**Note:** For information about mutual authentication for inbound web services, see Certificate-based authentication.

For information about using a custom HTTPS protocol profile to enable mutual authentication, see [Create a protocol profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/t_CreateAProtocolProfile.md).

**Parent Topic:**[Outbound REST authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_OutboundRESTAuth.md)

