---
title: Enabling Agent Client Collector data collection
description: You can perform actions which enhance data collection from the hosts on which Agent Client Collector is running.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/data-collection-enabling.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enabling Agent Client Collector data collection

You can perform actions which enhance data collection from the hosts on which Agent Client Collector is running.

-   **[Create a call API to send an osquery request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-api-send-os-query-reqs.md)**  
Create a background script to send an `osquery` request. The `osquery` request enables data collection from your host's operating system.
-   **[View host data collection for an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/collect-agent-host-data.md)**  
Run data collection on an agent's host to discover the components that are running on the host.
-   **[Generate an Agent Client Collector allow list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-generate-allow-list.md)**  
Specify the checks to be included in the list of checks that are enabled to run on the agent.
-   **[Run host data collection for an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/collect-host-data-agent.md)**  
Collect data on the host being monitored by an agent. Manually collecting host data ensures that the host's files are up to date.
-   **[Run host data collection on demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-run-discovery.md)**  
You can perform host data collection on demand, if you need to perform data collection before the job is scheduled to run.
-   **[Pause Agent Client Collector data collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-enable-silent-mode.md)**  
If CPU consumption on your server is getting too high, you can manually turn off the Agent Client Collector data collection to pause all checks performed by the agent, except for the agent's keep alive messages.
-   **[Clear Agent Client Collector plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/agent-plugins-remove.md)**  
Clear the plugin and configuration file cache folder and control plugin downloads. Clearing the cache folder removes unwanted plugins that have synced to the agent.

**Parent Topic:**[Deploying Agent Client Collector on both servers and endpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/acc-shared-deployment.md)

