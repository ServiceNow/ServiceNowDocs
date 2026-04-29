---
title: Agent Client Collector Monitoring
description: Agent Client Collector Monitoring enables you to monitor your service availability, examine the health and performance of your environment, and ensure that your infrastructure and its applications are running properly.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Monitoring

Agent Client Collector Monitoring enables you to monitor your service availability, examine the health and performance of your environment, and ensure that your infrastructure and its applications are running properly.

## Get started

**Note:**

If checks are not running on the agent's devices, your agent may be in CPU protection mode. CPU protection mode is activated automatically when a device's CPU consumption is too high for one of two reasons: either the user is running too many checks, or the machine is under-resourced. When it happens, the agent's Data Collection status turns to Off. ACC-F generates an event and records it in a log. To manually resume data collection by the ACC agent, see [Pause Agent Client Collector data collection](../task/acc-enable-silent-mode.md).

The user needs to monitor the activity of the ACC to resolve the issue through manual intervention and then re-enable ACC collection. To setup the ACC monitoring, see [Enable Agent Client Collector monitoring on the MID Server](../task/acc-monitoring-setup.md).

<table id="table_vfd_41y_51c" class="nav-card"><tbody><tr><td>

[Explore ![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn the key features and business value that the Agent Client Collector Monitoring application offers.](exploring-agent-client-collector-monitoring.md)

</td><td>

[Configure ![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Configure the features and components to enable Agent Client Collector Monitoring.](configuring-agent-client-collector-monitoring.md)

</td><td>

[Metric Intelligence ![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)Use Metric Intelligence to explore metric data and identify anomalies.](operational-metrics.md)

</td></tr><tr><td>

[Work with the Monitoring Technology Dashboard![](../../../reuse/icons/brand-icons/bus-management-console.svg)Monitor server resources by platform.](monitor-tech-dashboard-concept.md)

</td><td>

[Use proxy agents ![](../../../reuse/icons/brand-icons/bus-proxy.svg)Monitor the health and performance of your Configuration Items \(CIs\) when the agent is deployed outside of your host server.](proxy-agent.md)

</td><td>

[Reference ![](../../../reuse/icons/brand-icons/bus-learn.svg)Get additional details about checks and policies, and metric collection.](../reference/acc-monitoring-reference.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Ask or answer questions in the Agent Client Collector community forum.](https://www.servicenow.com/community/itom-articles/itom-agent-client-collector-acc-knowledge-amp-troubleshooting/ta-p/2529658)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

