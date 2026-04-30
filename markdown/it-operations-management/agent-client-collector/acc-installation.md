---
title: Agent Client Collector installation
description: You can install the Agent Client Collector on any supported host machine. The Agent Client Collector connects to a MID Server using the HTTP/S protocol, and the connection remains active after being established. One MID Server may handle several agents simultaneously, while a single agent works with one MID Server at a time and switches to a different MID Server when necessary to provide failover protection.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector installation

You can install the Agent Client Collector on any supported host machine. The Agent Client Collector connects to a MID Server using the HTTP/S protocol, and the connection remains active after being established. One MID Server may handle several agents simultaneously, while a single agent works with one MID Server at a time and switches to a different MID Server when necessary to provide failover protection.

When an agent's IP address changes, it selects a MID Server to connect to based on the agent's MID Server list.

The maximum number of agents that can be connected to a single MID Server is configurable in the **sn\_agent.mid.max\_allowed\_agents** MID Server property. The default value is 4,000.

On Windows, run the agent service as gMSA, LocalService, or Local system accounts.

On Linux and macOS, run the agent as a system account.

For ACC-V, a default 1 GiB MID Server can support 700 agents concurrently. An 8 GiB configuration for MID Server can support 8,000 agents concurrently. You can also scale out. For example, 5 MID Servers with 8 GiB of heap size can handle up to 40k agents.

If you completely reinstall the agent on a single host server, a second agent record registers on the instance. Delete the original agent on the **Agent Client Collectors** page \(**All** &gt; **Agent Client Collector** &gt; **Agents**\).

Agents whose **Status = Down** or **Disconnected** which haven't been deleted are deleted automatically after 30 days. You can modify this setting on the Autoflush form page \(see [Autoflush form](https://www.servicenow.com/docs/access?context=atf-auto-flush&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)\).

Before installing the Agent Client Collector, you must do the following:

-   Ensure that one or more MID Servers are properly registered and validated with your instance, to be available for an agent connection request. For details, see [Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US). In a staging environment, you need only one MID Server. However, in a production environment, configure at least two MID Servers to support zero-touch configuration and ensure that a MID Server is always available if one fails.
-   Ensure that there's a validated connection from the designated server where you're installing the agent to the MID Server.
-   Ensure that the MID Server port on which the Agent Client Collector listener runs is accessible.
-   Ensure that the following plugins are installed on your instance.

    For ACC-V:

    -   Agent Client Collector for Visibility
    -   Agent Client Collector Framework
    -   Discovery \[com.snc.discovery\] plugin
    For ACC-M:

    -   Agent Client Collector Framework
    -   Agent Client Collector Monitoring
    -   Event Management and Service Mapping Core
    -   Metric Intelligence - com.snc.sa.metric plugin
    For ACC-L:

    -   Agent Client Collector Log Analytics
    -   Health Log Analytics
    For DEX: ITOM Cloud Services

    You can verify that these plugins are installed on the **System Definitions** &gt; **Plugins** page.

-   All plugins that come with the base system are signed with the ServiceNow certificate. Optionally, you can use custom plugins and sign them using your own certificate, as described in [Enable OpenSSL secure signing for plugins](../task/acc-signing-mechanism.md).

-   Ensure that your system has the minimum requirements for agent installation.

<table id="table_xfj_pz4_hbc"><thead><tr><th>

Agent Client Collector component

</th><th>

Requirements

</th></tr></thead><tbody><tr><td>

Agent Client Collector Framework

</td><td>

-   1 GB RAM
-   300 MB free disk space
-   1 CPU core


</td></tr><tr><td>

Agent Client Collector Monitoring

</td><td>

-   1 GB RAM
-   1 GB free disk space
-   1 CPU core


</td></tr><tr><td>

Agent Client Collector for Visibility

</td><td>

-   1 GB RAM
-   1 GB free disk space
-   1 CPU core


</td></tr></tbody>
</table>-   Ensure that you are installing Agent Client Collector on one of the supported operating system distributions:

<table id="table_ids_3rw_ywb"><thead><tr><th>

Operating System

</th><th>

Distribution

</th></tr></thead><tbody><tr><td>

Linux

</td><td>

-   Red Hat Enterprise Linux - RHEL and Oracle Linux - OL 7, 8, 9
-   CentOS 7, CentOS Stream 8 and 9
-   SLES 12, 15
-   Debian 9, 10, 11
-   Ubuntu 18.04, 20.04, 22.04, 24.04 LTS
-   Amazon Linux 2 AMIs
-   Amazon 2023


</td></tr><tr><td>

Windows \(ACC-M and ACC-L are supported only on servers, not endpoints\)

</td><td>

-   Windows Server 2012, 2012r2, 2016, 2019, 2022
-   Windows 10 Enterprise Edition
-   Windows 11 Professional and Enterprise
-   Windows 11 Surface on ARM64


</td></tr><tr><td>

macOS \(on both x86\_64 and arm64 \(Apple Silicon\) architectures. ACC-M and ACC-L are supported only on servers, not endpoints\)

</td><td>

-   Catalina
-   Big Sur
-   Monterey
-   Ventura


</td></tr></tbody>
</table>
**Important:** All supported operating systems only work with the x86-64 CPU architecture type. ACC-F v3.1.1 also adds native support for ARM64 on Apple Silicon architectures. For the latest information, see the [Agent Client Collection on non- x86-64 computers and embedded boards \[KB1172387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1172387) article in the Now Support Knowledge Base.

When using ACC-L: The Agent Client Collector comes with the default **servicenow** user. Ensure that this user has read access to enable Agent Client Collector to view all the configured log paths. For example, the Agent Client Collector **servicenow** user that comes installed with the base system does not have permissions to view the paths to `/var/log/` in Linux and `C:\Windows\System32` in Windows. For information about configuring permissions for the **servicenow** user, see the [ACC-L Permission Denied issues \[KB1117271\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117271) article in the Now Support Knowledge Base.

When determining the number of machines and servers needed to support your agents \(such as the number of machines requiring proxy agents\), you must consider the agents' performance KPIs. For details on agent performance KPIs, see [Agent Client Collector performance and footprint for URL monitoring](../reference/acc-footprint-url-monitoring.md).

For details on using Agent Client Collector in an air-gapped environment, see the [Agent Client Collector Framework Air Gapped Configuration Item Management Solution \[KB1585753\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585753) article in the Now Support Knowledge Base.

Agent Client Collector supports domain separation. The domain of the agent and the CIs it creates is determined by the domain of the MID Server that the agent is connected to. The user's domain must be the lowest domain level \(known as a leaf domain\) to enable creating a Websocket endpoint extension for the MID Server.

**Related topics**  


[Agent Client Collector installation on a Linux OS system](acc-install-linux-concept.md)

[Install the Agent Client Collector on a Windows machine manually](../task/acc-install-windows.md)

