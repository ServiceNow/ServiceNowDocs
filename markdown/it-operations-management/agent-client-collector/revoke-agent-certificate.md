---
title: Revoke Agent Client Collector certificates
description: Stop communication between the agent and ITOM cloud services by removing an Agent Client Collector certificate. For example, there might be a security breach due to which you want to stop communication by revoking the agent's certificate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/revoke-agent-certificate.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC certificates, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
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

    For a list and explanation of the available revocation reasons, see [Agent Client Collector certificate revocation reasons](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/certificate-revocation-reasons.md).

5.  Select **OK**.

    The agent's certificate is revoked and the ITOM cloud services layer has its certificate revocation list \(CRL\) updated.


## Result

Communication between the agent and ITOM cloud services is stopped.

**Parent Topic:**[Agent Client Collector certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-certificates.md)

**Related topics**  


[Add a self-signed certificate to your operating system's truststore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/add-certificate-trust-store.md)

