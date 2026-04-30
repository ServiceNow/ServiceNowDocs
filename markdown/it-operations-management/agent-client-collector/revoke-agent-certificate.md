---
title: Revoke Agent Client Collector certificates
description: Stop communication between the agent and ITOM cloud services by removing an Agent Client Collector certificate. For example, there might be a security breach due to which you want to stop communication by revoking the agent's certificate.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-06-16"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Revoke Agent Client Collector certificates

Stop communication between the agent and ITOM cloud services by removing an Agent Client Collector certificate. For example, there might be a security breach due to which you want to stop communication by revoking the agent's certificate.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select the agent for which you want to revoke the certificate.

3.  Select the **Revoke Agent Certificate** button.

4.  Select the reason for certificate revocation.

    For a list and explanation of the available revocation reasons, see [Agent Client Collector certificate revocation reasons](../reference/certificate-revocation-reasons.md).

5.  Select **OK**.

    The agent's certificate is revoked and the ITOM cloud services layer has its certificate revocation list \(CRL\) updated.


## Result

Communication between the agent and ITOM cloud services is stopped.

**Related topics**  


[Add a self-signed certificate to your operating system's truststore](add-certificate-trust-store.md)

