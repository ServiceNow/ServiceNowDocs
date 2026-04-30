---
title: MID Web Server and agent mTLS Authentication
description: Mutual authentication using the Transport Layer Security protocol \(mTLS\) is a secure, certificate-based authentication scheme. With mTLS, the server \(the MID Web Server extension\) and the client \(the agent\) authenticate each other.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# MID Web Server and agent mTLS Authentication

Mutual authentication using the Transport Layer Security protocol \(mTLS\) is a secure, certificate-based authentication scheme. With mTLS, the server \(the MID Web Server extension\) and the client \(the agent\) authenticate each other.

TLS authentication occurs when a client \(such as a web browser\) authenticates the server it’s accessing by validating the certificate presented by the server. The client verifies that the certificate \(or certificate chain\) is signed by a trusted certificate authority \(CA\). The client must have access to a bundle of CA certificates, which it uses to validate the server certificate.

When mTLS is configured, the client presents a certificate or certificate chain to the server, and the server authenticates the client in the same way that the client authenticates the server \(mutual authentication\).

In addition to verifying the certificate signature, some TLS implementations also check the revocation status of the certificate. In these cases, the Online Certificate Status Protocol \(OCSP\) is used. In this protocol, the verifying party sends a request to the OCSP responder set up by the CA that issued the presented certificate. \(The responder's address is typically embedded in the CA-issued certificates\). The response indicates whether the presented certificate is revoked.

Before enabling mTLS, you must first create keys and certificates, install the .pem file on your MID Server, and connect the agent to your MID Server.

-   **[Create keys and certificates](../../agent-client-collector/task/create-keys-and-certificates.md)**  
Create keys and certificates in your root directory to enable Transport Layer Security \(TLS\) setup. TLS setup is necessary before you can configure mTLS on the MID Web Server and agent.
-   **[Install the .pem file in the MID unified keystore and set up the MID Web Server](../../agent-client-collector/task/set-mid-web-server.md)**  
Install the .pem file into the MID unified keystore and set up the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
-   **[Connect the agent to the MID Web Server using TLS](../../agent-client-collector/task/agent-mid-connect.md)**  
Connect the agent to the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
-   **[Configure mTLS authentication for a MID Web Server](../task/configure-mid-web-server-extension-mTLS.md)**  
Enhance security in your MID Web Server extension by enabling mTLS authentication.
-   **[Connect the agent to the MID Server using mTLS](../../agent-client-collector/task/enable-tls-agent.md)**  
Before configuring mTLS authentication on the agent, you must run a series of commands that enable configuring Transport Layer Security \(TLS\) authentication.

**Parent Topic:**[Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md)

**Related topics**  


[Configure the MID Web Server extension](../task/configure-mid-web-server-extension.md)

[Configure mTLS authentication for a MID Web Server](../task/configure-mid-web-server-extension-mTLS.md)

