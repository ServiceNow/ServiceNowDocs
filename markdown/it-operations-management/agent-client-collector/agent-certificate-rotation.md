---
title: Agent certificate rotation
description: The Agent Client Collector certificate is valid for two years and must be rotated before it expires to avoid issues with agent connectivity. When expiration is approaching, the agent initiates a certificate rotation request.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-06-22"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent certificate rotation

The Agent Client Collector certificate is valid for two years and must be rotated before it expires to avoid issues with agent connectivity. When expiration is approaching, the agent initiates a certificate rotation request.

When an Agent Client Collector's certificate expiration is approaching, system properties verify that a valid certificate is in place when the existing certificate expires.

-   **certificate-rotation-days-out**: Indicates the number of days before certificate expiration that an agent attempts to rotate its certificate. Configured in the `acc.yml` configuration file. Default = 28.
-   **sn\_agent.certificate\_rotation\_days\_out**: Indicates the number of days before certificate expiration that the system accepts a certificate rotation request for a specific agent. Configured on the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\). Default = 28.

**Related topics**  


[View the Agent Client Collector configuration file for an agent](../task/acc-yml-view.md)

[Configuration file options](../reference/acc-yml-options.md)

