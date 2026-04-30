---
title: Manually refresh Agent Client Collector certificates
description: Pull self-signed certificates from the ServiceNow install server, instead of waiting for the scheduled MID Server synchronization.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Manually refresh Agent Client Collector certificates

Pull self-signed certificates from the ServiceNow install server, instead of waiting for the scheduled MID Server synchronization.

## Before you begin

-   Ensure that the self-signed certificate is placed in a `.zip` file on the MID Server in the following location: `agent\static\cert`
-   Ensure that the certificate authority is part of the agent host's truststore, as the certificate chain is validated before the customer plugin signature.
-   Role required: agent\_client\_collector\_admin

## About this task

The MID Server checks for updates once each day, or after being restarted.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **MID Servers**.

2.  Select a MID Server.

3.  In the Related Links section, select **Trigger ACC certificate sync**.

4.  Restart the MID Server.


## Result

When an agent fails to perform a certificate check, the agent synchronizes certificates available on the MID Server. Synchronization is carried out for certificates on the ServiceNow install server and the self-signed certificates placed in the `.zip` file on the MID Server's `agent\static\cert` folder. Certificates are downloaded by the Agent Client Collector if the agent fails to validate a check definition's associated plugin assets.

