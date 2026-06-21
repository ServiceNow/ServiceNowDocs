---
title: Configuring Agent Client Collector Framework
description: Plan and configure your Agent Client Collector Framework implementation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/agent-client-collector/configuring-agent-client-collector-framework.html
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-08-15"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configuring Agent Client Collector Framework

Plan and configure your Agent Client Collector Framework implementation.

Agent Client Collector Framework configuration typically follows these steps:

1.  [Configure an agent registration key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/agent-registration-key-configuration.md).
2.  [Configure the websocket server on the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-configure-web-server.md).
3.  [Configure a websocket endpoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-configure-websocket-endpoint.md).
4.  [Configure the frequency of updating the agent MID Server list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-update-mid-server-list.md).
5.  [Create and edit Agent Client Collector plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/create-edit-assets.md).
6.  [Incorporating the Agent Client Collector into a custom base image for mass deployment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-virtual-deployment.md).
7.  [Install the Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-installation.md).

    The installation procedure to follow depends on the OS you are performing installation on \(Linux, Windows, or macOS\).

    **Note:** Agent Client Collector does not support multiple Agents installed on a single host device. Each host should have only one ACC Agent configured to communicate with a single ServiceNow. instance.

8.  [Enable Agent Client Collector monitoring on the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-monitoring-setup.md).
9.  [Optimize distribution of agents to MID Servers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-redistribute-agents-mid.md).
10. [View the Agent Client Collector configuration file for an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-yml-view.md).
11. [Create an Agent Client Collector configuration data file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/create-acc-config-data-file.md).
12. [Manually refresh Agent Client Collector certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/manually-sync-certificates.md).
13. [Enable OpenSSL secure signing for plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/acc-signing-mechanism.md).
14. [Perform Zscaler remediation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/agent-client-collector/zscaler-remediation-concept.md).

