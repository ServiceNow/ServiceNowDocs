---
title: Application patterns for the Agent Client Collector
description: Application patterns gather details on the applications that run on the Agent Client Collector \(ACC\) host. Application patterns are supported only for servers, and are triggered after the Agent Client Collector host Discovery is complete.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [ACC Discovery, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Application patterns for the Agent Client Collector

Application patterns gather details on the applications that run on the Agent Client Collector \(ACC\) host. Application patterns are supported only for servers, and are triggered after the Agent Client Collector host Discovery is complete.

## Prerequisites for using application patterns

To enable application patterns on the Agent Client Collector, install the following:

-   Agent Client Collector Framework
-   Agent Client Collector for Visibility - Content
-   Discovery

Set the **sn\_agent.appl\_classification\_behavior** property to **full**, and restart any MID Servers connected to the agent.

When working in a Windows environment, ensure that you're working with Powershell 3.0 or higher.

Role required \(on the host device\):

-   In a Linux or macOS environment: ServiceNow user with sudoers; nopasswd enabled with regular Discovery commands.
-   In a Windows environment: Local System user, SYSTEM, or a local user account where the local user account uses one of the following:
    -   Logon as a service
    -   Backup \(SeBackupPrivilege\)
    -   Debug Programs privileges

## Viewing supported application patterns

To view the list of patterns supported for Agent Client Collector, navigate to **All** &gt; **Pattern Designer** &gt; **Supported Patterns for ACC**. Application patterns are the only pattern types supported for use with Agent Client Collector.

## Viewing Application Patterns executed on Agent Client Collector

You can view the application patterns that were executed on a given agent.

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.
2.  Select an agent.
3.  Select **View** &gt; **Discovery** from the context menu \(hamburger\).
4.  Open the agent.
5.  Select the **Application Pattern logs** tab on the bottom of the page.

    The list of patterns executed on the agent appears. Executed patterns are indicated with the value **true** in the Executed On Agent column.


## Unsupported application pattern operations

Application patterns aren't supported in the following pattern operations:

-   WMI method invocation
-   Change/unchange user
-   All custom operations
-   SNMP query
-   Put file

## Agent Client Collector pattern execution properties

Configure the following properties \(**All** &gt; **System Properties** &gt; **All Properties**\) to maximize the use of application patterns with Agent Client Collector:

<table id="table_qls_jcw_11c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_agent.appl\_classification\_behavior

</td><td>

Set value to **full** to enable working with applications patterns and to access pattern commands in the allow-list.Default: simple

**Note:** To enable application pattern execution with the allow-list, use the allow-list template for application patterns. For details, see the [Pattern execution on ACC: Sample Allowlist for Pattern Content](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585764) article in the Now Support Knowledge Base.

</td></tr></tbody>
</table><table id="table_fsp_ctl_g1c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

mid.discovery.agent.command.mid.timeout

</td><td>

The maximum duration, in seconds, that the MID Server waits for a response from the agent before timing out. Default: 60 seconds

</td></tr><tr><td>

mid.discovery.agent.command.timeout

</td><td>

The maximum amount of time, in seconds, that the command is given to execute on the agent host.Default: 60 seconds

</td></tr></tbody>
</table>## Using pattern designer debugging in ACC mode

You can debug application patterns that are configured in ACC mode.

1.  Set the **sn\_agent.appl\_classification\_behavior** property to **full**.
2.  In the Pattern Designer, enable the debug option and select **Use ACC connection** in the Debug identification section.

The pattern log indicates whether the pattern was successfully executed on the agent.

You can also receive pattern details in the following logs:

-   MID Server logs: Set **mid.log.level** to DEBUG for the mid agent log to display details on the pattern step, ACC check, and the pattern response.
-   ACC logs: Search for the string **PatternOnTheFlyCheck** for details on pattern checks.

## Oracle Global License Advisory Services \(GLAS\) data collection

Oracle Java process discovery works either with patterns \(when using either a MID Server or Agent Client Collector\), or with file-based discovery \(using Agent Client Collector with file-based discovery\). If both the pattern and file-based discovery run the same Java installation, the pattern-collected data takes precedence.

When performing Discovery with Agent Client Collector, ensure that you have the following settings:

-   All users must have the Oracle GLAS store app, starting with version 1.8.4.
-   Agent Client Collector users:

    -   Must have the Agent Client Collector Framework store plugin.
    -   Can have the Agent Client Collector for Visibility - Content store plugin, for extra data.
    For information about privileged user access, see [KB1705845](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705845).

    **Note:** Oracle Java discovery with ACC is applicable in all server environments. However, currently, it's partially supported for different Desktop environments. For a Windows Desktop update set, see the KB article [KB1705845](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705845).


For information on java installation Discovery using Agent Client Collector for Visibility - Content, see [Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery](../task/acc-file-based-discovery.md).

For information on the collected data, see [Data collected during Agent Client Collector for Visibility - Content file-based Discovery](../reference/data-collected-file-based-discovery.md).

Application patterns support Oracle GLAS data collection in a Linux environment. For details on using patterns, see [Oracle Global License Advisory Services \(GLAS\) data collection using patterns](../../service-mapping/reference/oracle-glas-discovery.md).

Although Oracle GLAS supports Put file operations, the related files are deployed using Agent Client Collector plugins instead of SSH or WMI.

-   **[Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery](../task/acc-file-based-discovery.md)**  
Discovering java installation data using Agent Client Collector for Visibility - Content file-based discovery enables you to discover file information in your system.

**Parent Topic:**[Agent Client Collector Discovery](acc-discovery.md)

**Related topics**  


[Discovery patterns used by ITOM Visibility](../../service-mapping/concept/c_MappingPatternsCustomization.md)

