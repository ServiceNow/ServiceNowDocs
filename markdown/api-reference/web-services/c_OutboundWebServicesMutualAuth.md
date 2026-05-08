---
title: Outbound web service mutual authentication
description: Mutual authentication establishes trust by exchanging Secure Sockets Layer \(SSL\) certificates.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound, Web services, API implementation, API implementation and reference]
---

# Outbound web service mutual authentication

Mutual authentication establishes trust by exchanging Secure Sockets Layer \(SSL\) certificates.

Before connecting to a server, the client requests an SSL certificate. The server responds by requesting that the client send its own certificate. Both respond by validating the certificates of the other and sending acknowledgments before initiating an HTTPS connection.

As an administrator, you can enable mutual authentication by defining a protocol profile for connections that require mutual authentication. Protocol profiles allow you to associate a specific certificate record with a protocol, such as HTTPS.

For example, you can create a protocol profile called `mauth` with a certificate for mutual authentication. You can then make an HTTPS web service request by calling `mauth://<external-endpoint.com>` when the end point requires mutual authentication.

**Note:** This feature enables mutual authentication only on outbound HTTPS connections, such as SOAP, REST, or direct HTTPS calls. ServiceNow does not support mutual authentication for outbound requests sent through a MID Server. For information about mutual authentication for inbound web services, see Certificate-based authentication.

-   **[Create a protocol profile](../task/t_CreateAProtocolProfile.md)**  
You can create a custom HTTPS protocol profile to specify the credentials and certificates used for outbound web services. For example, you can create a custom HTTPS protocol profile to enable mutual authentication.
-   **[Enable mutual authentication](../task/t_EnableMutualAuth.md)**  
You can configure a SOAP or REST message for mutual authentication using a protocol profile.

**Parent Topic:**[Outbound web services](outbound-web-services.md)

