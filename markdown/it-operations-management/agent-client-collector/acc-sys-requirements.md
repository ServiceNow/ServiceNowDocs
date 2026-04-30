---
title: Agent Client Collector system requirements
description: System requirements are the fundamental specifications and configuration needed to install and run Agent Client Collector \(ACC\) effectively.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [ACC installation, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector system requirements

System requirements are the fundamental specifications and configuration needed to install and run Agent Client Collector \(ACC\) effectively.

Before installing the Agent Client Collector, you must do the following:

-   When working with a MID Server:
    -   Ensure that one or more MID Servers are properly registered and validated with your instance, to be available for an agent connection request. For details, see [Configuring MID Servers](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US). In a staging environment, you need only one MID Server. However, in a production environment, configure at least two MID Servers to support zero-touch configuration and ensure that a MID Server is always available if one fails.
    -   Ensure that there's a validated connection from the designated server where you're installing the agent to the MID Server.
    -   Ensure that the MID Server port on which the Agent Client Collector listener runs is accessible.
-   When working with MID-less deployment, follow the instructions described in [Configuring MID-less Agent Client Collector](acc-configuring-without-mid.md).
-   Ensure that the following plugins are installed on your instance:

<table id="table_fq2_nnv_hfc"><thead><tr><th>

Application

</th><th>

Plugin

</th></tr></thead><tbody><tr><td>

ACC-F

</td><td>

-   MID Server
-   CMDB for scoped applications
-   Agent Client Collector global utilities
-   MID Web Server
-   Service Error Management


</td></tr><tr><td>

ACC-VC

</td><td>

-   Agent Client Collector for Visibility - Content
-   Agent Client Collector Framework
-   Discovery \[com.snc.discovery\] plugin


</td></tr><tr><td>

ACC-M

</td><td>

-   Agent Client Collector Framework
-   Agent Client Collector Monitoring
-   Event Management and Service Mapping Core
-   Metric Intelligence - \[com.snc.sa.metric\] plugin


</td></tr><tr><td>

ACC-L

</td><td>

-   Agent Client Collector Framework
-   Agent Client Collector Log Analytics
-   Health Log Analytics


</td></tr><tr><td>

DEX

</td><td>

-   Agent Client Collector Framework
-   ITOM Cloud Services Core \[sn\_itom\_cloud\_svc\]


</td></tr></tbody>
</table>    You can verify that these plugins are installed on the **System Definitions** &gt; **Plugins** page.

    All plugins that come with the base system are signed with the ServiceNow certificate. Optionally, you can use custom plugins and sign them using your own certificate, as described in [Enable OpenSSL secure signing for plugins](../task/acc-signing-mechanism.md).

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

Agent Client Collector for Visibility - Content

</td><td>

-   1 GB RAM
-   1 GB free disk space
-   1 CPU core


</td></tr></tbody>
</table>-   Ensure that you’re installing Agent Client Collector on one of the supported operating system distributions. For details on the supported operating systems, see [Agent Client Collector Framework](https://store.servicenow.com/store/app/bc09636e1be06a50a85b16db234bcbd1) in the ServiceNow® Store.

**Important:** All supported operating systems work only with the x86-64 CPU architecture type. ACC-F v3.1.1 also adds native support for ARM64 on Apple Silicon architectures. For the latest information, see the [Agent Client Collection on non- x86-64 computers and embedded boards \[KB1172387\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1172387) article in the Now Support Knowledge Base.

When using ACC-L: The Agent Client Collector comes with the default **servicenow** user. Ensure that this user has read access to enable Agent Client Collector to view all the configured log paths. For example, the Agent Client Collector **servicenow** user that comes installed with the base system does not have permissions to view the paths to `/var/log/` in Linux and `C:\Windows\System32` in Windows. For information about configuring permissions for the **servicenow** user, see the [ACC-L Permission Denied issues \[KB1117271\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1117271) article in the Now Support Knowledge Base.

When determining the number of machines and servers needed to support your agents \(such as the number of machines requiring proxy agents\), consider the agents' performance KPIs. For details on agent performance KPIs, see [Agent Client Collector performance and footprint for URL monitoring](../reference/acc-footprint-url-monitoring.md).

