---
title: Agent Client Collector deployment - servers
description: When deploying the Agent Client Collector, perform deployment and management tasks on your environment's servers.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-12-25"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector deployment - servers

When deploying the Agent Client Collector, perform deployment and management tasks on your environment's servers.

Server deployment uses MID Servers to connect your agents to a ServiceNow instance. Agents deployed on data center servers open WebSocket connections to your MID Servers, which relay data to your instance. You manage the sizing, certificates, and load balancing of the MID Server.

Use server deployment when your agents are in controlled environments such as data centers, where you are already running MID Servers and want to keep traffic on your network. Agent Client Collector Monitoring \(ACC-M\) and Agent Client Collector Log Analytics \(ACC-L\) require server deployment, and you can deploy Agent Client Collector for Visibility - Content \(ACC-VC\) with servers as well.

