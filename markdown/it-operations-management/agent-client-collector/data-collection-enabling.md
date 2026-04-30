---
title: Enabling Agent Client Collector data collection
description: You can perform actions which enhance data collection from the hosts on which Agent Client Collector is running.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Enabling Agent Client Collector data collection

You can perform actions which enhance data collection from the hosts on which Agent Client Collector is running.

-   **[Create a call API to send an osquery request](../task/acc-api-send-os-query-reqs.md)**  
Create a background script to send an `osquery` request. The `osquery` request enables data collection from your host's operating system.
-   **[View host data collection for an agent](../task/collect-agent-host-data.md)**  
Run data collection on an agent's host to discover the components that are running on the host.
-   **[Generate an Agent Client Collector allow list](../task/acc-generate-allow-list.md)**  
Specify the checks to be included in the list of checks that are enabled to run on the agent.
-   **[Run host data collection on demand](../task/acc-run-discovery.md)**  
You can perform host data collection on demand, if you need to perform data collection before the job is scheduled to run.
-   **[Pause Agent Client Collector data collection](../task/acc-enable-silent-mode.md)**  
If CPU consumption on your server is getting too high, you can manually turn off the Agent Client Collector data collection to pause all checks performed by the agent, except for the agent's keep alive messages.
-   **[Validate assets on the MID Server](../task/validate-assets-mid-server.md)**  
Validate assets on your MID Server to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your MID Server assets.
-   **[Validate assets on agents](../task/validate-assets-agents.md)**  
Validate assets on your agents to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your agents' assets.

**Parent Topic:**[Agent Client Collector Framework](acc-framework-landing-page.md)

