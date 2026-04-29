---
title: Agent Client Collector certificates
description: Agent Client Collector certificates verify the authenticity of your agents, servers, and users. Using Agent Client Collector certificates ensures the safety of your environment.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector certificates

Agent Client Collector certificates verify the authenticity of your agents, servers, and users. Using Agent Client Collector certificates ensures the safety of your environment.

## Discovering certificates

To discover certificates on all of your host's applications with open ports, navigate to **All** &gt; **System Properties** &gt; **All Properties** and set the **sn\_acc\_vis\_content.tls\_ssl\_scan\_all\_open\_ports** property to **true**.

If you want to maintain certificates only for applications running on specific ports, set this property to **false**. The property's default value is **true**.

-   **[Manually refresh Agent Client Collector certificates](../task/manually-sync-certificates.md)**  
Refresh Agent Client Collector self-signed certificates manually to validate Agent Client Collector plugins, instead of waiting for the scheduled synchronization. For example, you can use this feature when the agent can't validate a plugin and you don't want to wait for the scheduled synchronization.
-   **[Enable OpenSSL secure signing for plugins](../task/acc-signing-mechanism.md)**  
Create a self-signed certificate for an Agent Client Collector plugin. The following procedure gives an example of how to create an x509 certificate using OpenSSL. For other certificate types, consult OpenSSL documentation.
-   **[Add a self-signed certificate to your operating system's truststore](../task/add-certificate-trust-store.md)**  
Add a self-signed certificate to the truststore of your operating system \(OS\). By adding a certificate to the truststore, you can verify that the certificate is authentic and that your connections are secure.
-   **[Import a self-signed certificate](../task/import-self-signed-certificate.md)**  
Import a self-signed certificate in a Windows system by using the Certificate Import Wizard. The Certificate Import Wizard is required to complete the self-signed certificate import process on a Windows Operating System \(OS\).
-   **[Revoke Agent Client Collector certificates](../task/revoke-agent-certificate.md)**  
Stop communication between the agent and ITOM cloud services by removing an Agent Client Collector certificate. For example, there might be a security breach due to which you want to stop communication by revoking the agent's certificate.
-   **[Agent certificate rotation](agent-certificate-rotation.md)**  
The Agent Client Collector certificate is valid for two years and must be rotated before it expires to avoid issues with agent connectivity. When expiration is approaching, the agent initiates a certificate rotation request.
-   **[Run Certificate Discovery via Agent Client Collector for Visibility - Content](../task/run-cert-discovery-accvc.md)**  
Discover TLS/SSL certificates used by ports running on the agent's server. The Certificate Inventory and Management application uses this information to manage TLS/SSL certificates.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](acc-shared-deployment.md)

