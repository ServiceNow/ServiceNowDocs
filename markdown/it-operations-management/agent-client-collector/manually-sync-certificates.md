---
title: Manually refresh Agent Client Collector certificates
description: Refresh Agent Client Collector self-signed certificates manually to validate Agent Client Collector plugins, instead of waiting for the scheduled synchronization. For example, you can use this feature when the agent can't validate a plugin and you don't want to wait for the scheduled synchronization.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC certificates, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Manually refresh Agent Client Collector certificates

Refresh Agent Client Collector self-signed certificates manually to validate Agent Client Collector plugins, instead of waiting for the scheduled synchronization. For example, you can use this feature when the agent can't validate a plugin and you don't want to wait for the scheduled synchronization.

## Before you begin

-   Ensure that the self-signed certificate is placed in a `.zip` file on the MID Server in the following location: `agent\static\cert`
-   Ensure that the certificate authority is part of a truststore, as the certificate chain validates before the customer plugin signature.
-   Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

2.  Select a MID Server.

3.  In the Related Links section, select **Trigger ACC certificate sync**.

4.  Restart the MID Server.


## Result

When an agent fails to perform a certificate check, the agent synchronizes certificates available on the MID Server by pulling self-signed certificates from the install server. Certificates are downloaded by the Agent Client Collector if the agent does not validate its plugins.

**Parent Topic:**[Agent Client Collector certificates](../concept/acc-certificates.md)

