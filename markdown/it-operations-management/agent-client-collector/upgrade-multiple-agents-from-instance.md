---
title: Upgrade multiple agents in an instance
description: When performing selective upgrade of an agent in an instance, you can select multiple instances to upgrade at once.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC installation, ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Upgrade multiple agents in an instance

When performing selective upgrade of an agent in an instance, you can select multiple instances to upgrade at once.

## Before you begin

Supported Operating Systems: Windows and Linux.

Agent Client Collector installs need to access this URL: `https://install.service-now.com/`. MID connected agents can download the installer from the MID Server \(`https://<MID-WEBSERVER-URI:PORT>/static/acc_installers/agent-client-collector`\).

Select the version to which you want to upgrade your agent.

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
2.  Select **New**.
3.  Assign the following values:
    -   Name = **sn\_agent.agent\_upgrade\_version**
    -   Type = **string**
    -   Value = The version number to be upgraded to, in the format &lt;major\_version.minor\_version.patch\_version&gt;. For example: **4.3.2**
4.  Select **Submit**.

If you do not select a version, the agent automatically upgrades to the current Agent Client Collector Framework scoped app version.

When working with MID-less agents, ensure that the agents are connected to a Content Delivery Network \(CDN\). For details, see [Configure proxies when performing MID-less upgrade using a Content Delivery Network \(CDN\)](cdn-upgrade-proxies.md).

Role required: agent\_client\_collector\_admin

## About this task

You can select up to 20 agents at a time for upgrade. To upgrade large numbers of agents, incorporate the Agent Client Collector into your software deployment tools.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select the check box next to the agents that you want to upgrade.

    You can select up to 20 agents.

3.  In the **Actions on selected rows...** box, select **Upgrade agent**.

4.  In the confirmation dialog box, select **Upgrade**.


**Related topics**  


[Upgrade an agent in an instance](upgrade-agent-from-instance.md)

[Perform high-volume Agent Client Collector upgrade](acc-high-volume-upgrade.md)

