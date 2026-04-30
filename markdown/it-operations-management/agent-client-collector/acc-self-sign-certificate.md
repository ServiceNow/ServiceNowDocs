---
title: Secure a custom plugin with a certificate
description: When you customize or create an Agent Client Collector plugin, you can secure the plugin with either a third-party certificate or an internal secure certificate in the plugin's script. Official plugins are signed by an external certificate authority.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create and edit Agent Client Collector plugins, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Secure a custom plugin with a certificate

When you customize or create an Agent Client Collector plugin, you can secure the plugin with either a third-party certificate or an internal secure certificate in the plugin's script. Official plugins are signed by an external certificate authority.

Using a self-signed certificate is enabled by default. To disable this feature, set the **verify-plugin-signature** property to **False**. When you disable a self-signed certificate, your configured plugins use no certificate.

For details on how to configure a self-signed certificate by using OpenSSL, see [Enable OpenSSL secure signing for plugins](../task/acc-signing-mechanism.md). For details on how to configure a third-party certificate, consult the third-party vendor's documentation.

When the agent's current certificates can't validate a plugin, Agent Client Collector requests the updated certificates from its synchronized MID Server. You can manually refresh the agent to receive these certificates before the scheduled synchronization. For details, see [Manually refresh Agent Client Collector certificates](../task/manually-sync-certificates.md).

You can manually save the certificates in a directory on the MID Server that is connected to the installed agents. Any agent that's installed in your environment can then access the certificates from that MID Server.

For details on how to configure the certificate synchronization properties, see [Synchronization properties for validating Agent Client Collector plugins](../reference/plugin-validation-reference.md).

