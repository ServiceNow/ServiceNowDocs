---
title: Configuring Agent Client Collector with a MID Server
description: Configure the Agent Client Collector with a MID Server to enable communication between network servers and the ServiceNow instance.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configuring Agent Client Collector with a MID Server

Configure the Agent Client Collector with a MID Server to enable communication between network servers and the ServiceNow instance.

-   **[Configure an Agent Client Collector with a MID Server using a single-line command](../task/configure-acc-with-mid.md)**  
Use a single-line command to set up an Agent Client Collector with a MID Server. You can also use the single-line command to migrate agents with MID-less configuration to be used with a MID Server.
-   **[Configure the websocket server on the MID Server](../task/acc-configure-web-server.md)**  
Configure the websocket server on MID Servers to enable connections from agents to the MID Server. You can configure only one websocket server per MID Server.
-   **[Configure a websocket endpoint](../task/acc-configure-websocket-endpoint.md)**  
Configure a websocket to enable the endpoint to provide web access from the MID Server to the Agent Client Collector \(ACC\).
-   **[Configure the frequency of updating the agent MID Server list](../task/acc-update-mid-server-list.md)**  
By default, the list of MID servers connected to agents is updated once daily. If you have a dynamic environment that adds MID servers frequently, you may want to schedule updates more often, or execute the job on demand.
-   **[Enable Agent Client Collector monitoring on the MID Server](../task/acc-monitoring-setup.md)**  
Enable Agent Client Collector monitoring on the MID Server by configuring the Agent Client Collector framework \(ACC-F\) and Metric Intelligence extensions in a single action. Enabling Agent Client Collector monitoring also enables monitoring on agents connected to the MID Server.
-   **[Automatic MID Server selection](acc-auto-mid-selection.md)**  
Automatic selection of MID Servers ensures that each agent uses the most efficient available MID Server.

**Parent Topic:**[Deploying Agent Client Collector on servers](acc-server-deployment.md)

