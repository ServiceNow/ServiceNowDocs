---
title: MID Server selection
description: You can configure MID Server selection by application, IP address ranges, network capability, or behavior. Specific MID Servers can be assigned to particular tasks, or the MID Server can be selected automatically. MID Servers can use domain separation to limit the scope of discoveries and event management.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server selection

You can configure MID Server selection by application, IP address ranges, network capability, or behavior. Specific MID Servers can be assigned to particular tasks, or the MID Server can be selected automatically. MID Servers can use domain separation to limit the scope of discoveries and event management.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>The MID Selector used by most applications has three modes to select a MID Server:

-   **Auto-select MID Server**: Selects from MID Servers based on MID Server criteria, regardless of whether they are members of a cluster.
-   **Use specific MID Server**: Automatic reassignment to another MID Server is not supported.
-   **Use specific MID Server cluster**: Automatic reassignment to another MID Server only selects from members of the specified cluster.

For Agent Client Collector, refer to [Automatic MID Server selection](https://www.servicenow.com/docs/access?context=acc-auto-mid-selection&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

## MID Server criteria

MID Servers offer these types of criteria that help an application determine which MID Server to use:

-   **Application**: The application that you specify on the MID Server. You can designate these applications for a specific MID Server:

    -   Discovery
    -   Orchestration
    -   Service Mapping
    -   Event Management
    -   Operational Intelligence
    -   Cloud Management
    An **ALL** application option is also available. By default, this option includes all applications. You can [configure which applications](../task/t_SpecifyMIDServerApplications.md#) are included in the **ALL** designation.

-   **IP address or range**: The IP address or the IP ranges that the MID Server is allowed to work within. You can specify an IP address or IP range in the application, such as on a Discovery schedule or an Orchestration activity, and for the MID Server. If the IP configured in the application matches the IP address or falls within the allowable IP range configured on the MID Server, a match is possible, and that MID Server passes this criteria. To have the instance automatically assign IP ranges \(subnets\) to available MID Servers, see [Using MID Server IP range auto-assignment](mid-servers-auto-assignment.md#).
-   **Capabilities**: The [network capability](../reference/r_MIDServerCapabilities.md) an application needs to use, such as the [PowerShell Orchestration activity](../../orchestration/reference/mid-server-powershell-files.md) or the Workflow Studio [PowerShell step](https://www.servicenow.com/docs/access?context=powershell-step-action-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). Some applications, like Cloud Management, require a specific capability.

    **Note:** Discovery and Service Mapping can also use behaviors, which determine the type of port probes used during the port scan phase of Discovery. Both Discovery and Service Mapping use a behavior to discover [Create a discovery behavior for Unix-based load balancers](https://www.servicenow.com/docs/access?context=t_CreateDiscoBehavior4LB&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US). Other applications do not use behaviors. Behaviors are not used for auto-selection, default MID Servers, or specific MID Servers as described below. See [Discovery behaviors](https://www.servicenow.com/docs/access?context=c_DiscoveryBehaviors&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) for more information.


## How an application selects a MID Server

If you do not specify a specific MID Server for an application to use, the application tries to select one. Each application relies on different criteria to select an appropriate MID Server.

<table id="table_d1w_sbb_vw"><thead><tr><th>

Application

</th><th>

Supported Application on the MID Server

</th><th>

IP address range

</th><th>

Capability

</th></tr></thead><tbody><tr><td>

Discovery\(Select **Auto-Select MID Server** on the Discovery schedule\)

</td><td>

The **Discovery** or **ALL** application must be [specified on the MID Server](../task/t_SpecifyMIDServerApplications.md#).

</td><td>

Discovery uses IP ranges that you configure on the [Discovery Schedule form](https://www.servicenow.com/docs/access?context=t_CreateADiscoverySchedule&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) to see if they fall within the IP ranges that you configure on the MID Server, or the **ALL** IP ranges option must be selected on the MID Server.

</td><td>

N/A**Note:** Any configured behaviors are ignored.

</td></tr><tr><td>

Orchestration

</td><td>

The **Orchestration** or **ALL** application must be specified on the MID Server.

</td><td>

The target IP address that you configure in an Orchestration activity must fall within the IP ranges that you configure on the MID Server, or the **ALL** option must be selected on the MID Server.

</td><td>

The capability that is required for an Orchestration activity must match the [capabilities you configure on the MID Server](../task/t_ConfigureCapabilities.md#), or the MID Server capability must be set to **ALL**.

</td></tr><tr><td>

Service Mapping

</td><td>

The **Service Mapping** or **ALL** application must be specified on the MID Server.

</td><td>

The endpoint IP address must fall within the IP range that you configure on the MID Server, or the **ALL** option must be selected on the MID Server.

</td><td>

One of the supported Service Mapping capabilities \(for new installs\) must be configured on the MID Server, or the MID Server capability must be set to **ALL**.

</td></tr><tr><td>

Event Management

</td><td>

The **Event Management** or **ALL** application must be specified on the MID Server.

</td><td>

The IP configured in the event connector instances, such as [Configure event collection from HPOM](https://www.servicenow.com/docs/access?context=t_EMConfigureHPOMConnector&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), must fall within the IP range configured on the MID Server.

</td><td>

 

</td></tr><tr><td>

Cloud Management

</td><td>

N/A

</td><td>

N/A

</td><td>

The **Cloud Management** or **ALL** capability must be added.

</td></tr></tbody>
</table>## Mode: Auto-select MID Server

During initial work assignment to a MID Server, or when failing over existing work from a down MID Server to another MID Server, the MID selector picks a set of suitable MID from a given status level by traversing the steps below once. If at any step it finds at least one server, all remaining steps are skipped.

1.  Suitable MID Servers with status = Up.

2.  Default MID Server \(if it was defined\) with status = Up.

3.  Suitable MID Servers with status = Upgrading or Paused.

4.  Default MID Server \(if it was defined\) with status = Upgrading or Paused.

5.  Suitable MID Servers with status = Upgrade Failed, Draining, Drained, Drain Failed, or Down.

6.  Default Mid Server \(if was defined\).


All steps which are below an application's minimum status level are skipped. Many applications \(such as Discovery\) allow Up or Degraded MID Servers, other applications only allow Up MID Servers.

## Mode: Use specific MID Server cluster

During initial work assignment to a MID Server, or when failing over existing work from a down MID Server to another MID Server, the MID selector picks a set of suitable MID from a given status level by traversing the steps below once. If at any step it finds at least one server, all remaining steps are skipped.

1.  Suitable Mid Servers with status = Up.

2.  Suitable Mid Servers with status = Upgrading or Paused.

3.  Suitable Mid Servers with status = Upgrade Failed, Draining, Drained, Drain Failed, or Down.


All steps which are below an application's minimum status level are skipped. Many applications \(such as Discovery\) allow Up or Degraded MID Servers, other applications only allow Up MID Servers.

A MID server is picked from set of MID servers at the highest status level as follows depending on cluster type:

-   **Load Balance Cluster**: picks a MID Server within the status level randomly.

-   **Fail-over Cluster**: picks a MID Server with best cluster records' order number \(0 = best\).


## Mode: Use a specific MID Server

Discovery and Event Management can use a MID Server that you specifically call out.

**Note:** Selecting a specific MID Server is not the same as specifying the [default MID Server for an application](../task/t_SpecifyMIDServerApplications.md#). A specific MID Server is always used. If it is **Down** or not validated, the application does not execute commands against the MID Server. A default MID Server is fallback that is used when the auto-selection of MID Servers does not find any eligible MID Server.

<table id="table_nbd_23b_vw"><thead><tr><th>

Application

</th><th>

How you specify a specific MID Server

</th><th>

Criteria that the default MID Server must meet

</th></tr></thead><tbody><tr><td>

Discovery

</td><td>

Choose the MID Server on the Discovery schedule.**Note:** You can also specify [a cluster of MID Servers](../task/t_ConfigureAMIDServerCluster.md#).

</td><td>

If you select a MID Server without the **Discovery** or **ALL** application, it automatically adds the **Discovery** application.

</td></tr><tr><td>

Orchestration

</td><td>

N/A

</td><td>

N/A

</td></tr><tr><td>

Service Mapping

</td><td>

N/A

</td><td>

N/A

</td></tr><tr><td>

Event Management

</td><td>

Choose one or more MID Servers on the connector instance event collection, such as [Configure event collection from HPOM](https://www.servicenow.com/docs/access?context=t_EMConfigureHPOMConnector&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

</td><td>

N/A

</td></tr><tr><td>

Cloud Management

</td><td>

N/A

</td><td>

N/A

</td></tr></tbody>
</table>**Note:** If a MID Server manages resources within defined IP ranges for Orchestration, you must map the fully-qualified domain name \(FQDN\) of a server with its IP address to run certain activities, such as [Exchange activities](../../../administer/orchestration-activities/task/t_ConfigureMIDServerForExchange.md).

## Domain separation

If you are using domain separation, you can configure MID Servers to be in separate domains. The domain that the MID Server is in affects how the application selects the domain:

**Discovery and Service Mapping**: On the Discovery schedule, the MID Servers and clusters that available for selection are limited to the same domain of the user who is configuring the schedule. This also applies to the auto-selection option: only MID Servers in the same domain as the user can be automatically selected.

## MID Server selection test for Service Mapping

If Service Mapping is active, you can preview which MID Server that Service Mapping uses for a specific target device or computer. To do this, navigate to **Service Mapping** &gt; **MID Servers** and click **MID Selection Test**. Enter the IP address and an optional application and capability, and then click **OK**. The name of the MID Server that Service Mapping will use appears in the window.

## Related topics

-   **[Configure a default MID Server for each application](../task/t_SpecifyMIDServerApplications.md#)**  
You can configure a default MID Server that an application can use if all other possible MID Servers are unavailable. You can narrow down the list of applications that are included in the definition of ALL.
-   **[Configure an IP address range for the MID Server](../task/t_ConfigureMIDIPRange.md)**  
You can manually configure an IP address range for the MID Server to explore.
-   **[Override the MID Server selection filter](../task/override_mid_server_selector.md)**  
Use the override feature to write your own filter condition that overrides the normal MID Server selection criteria for an application. An override has precedence over the default filter and can be defined for a specific selection condition.

**Parent Topic:**[Configuring MID Servers](c_MIDServerConfiguration.md)

