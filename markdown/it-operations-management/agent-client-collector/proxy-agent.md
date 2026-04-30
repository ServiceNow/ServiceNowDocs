---
title: Using proxy agents in Agent Client Collector
description: You can use a proxy agent to monitor the health and performance of your configuration items \(CIs\) even if the agent is in the cloud or any place that is external to your host server.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector Monitoring, Agent Client Collector, IT Operations Management]
---

# Using proxy agents in Agent Client Collector

You can use a proxy agent to monitor the health and performance of your configuration items \(CIs\) even if the agent is in the cloud or any place that is external to your host server.

Proxy agents are used to monitor:

-   URLs \(to ensure that the URLs are available and accessible\)
-   Services that don't have a host server
-   Closed services on which you can’t configure an agent
-   External databases in the cloud

One agent can monitor multiple entities and their CIs.

The following diagram shows the connection between a ServiceNow instance, the MID Server, and Agent Client Collector agents, as well as proxy agents that monitor CIs that are external to the agent.

![Proxy agent configuration diagram](../image/acc-proxy-agent.png "Proxy agent configuration")

You can configure the proxy agent to do a custom check when it is monitoring external entities. To learn how to create custom checks, see [Create and edit checks](../task/view-checks.md).

You can create a cluster of proxy agents on multiple proxy servers to monitor the services that are external to the host server. To learn how to create a proxy agent cluster, see [Create a proxy agent cluster](../task/configure-agent-proxy-cluster.md).

Use a Proxy Auto-Configuration \(PAC\) file to dynamically determine the appropriate proxy server to use. PAC files provide flexible and automated proxy configuration, enabling the agent to use different proxies for different destinations, connect directly to internal resources, implement complex proxy routing logic, and to automatically handle proxy failover. For details on the parameters used for PAC file configuration, see [Configuration file options](../reference/acc-yml-options.md).

Following is a sample PAC file:

```
function FindProxyForURL (url, host) {

   // Connect directly to internal hosts
   if (isPlainHostName(host) ||
      shExpMatch(host, "*.internal.company.com")) {
      return "DIRECT";
   }

   // use proxy for all other hosts
   return "PROXY proxy.company.com:8080:
}

```

**Related topics**  


[Checks and policies](checks-policies.md)

[Agent Client Collector Monitoring default checks and policies](../reference/agent-policies-checks.md)

