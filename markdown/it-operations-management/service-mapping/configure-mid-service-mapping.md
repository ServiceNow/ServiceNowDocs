---
title: MID Server configuration for Service Mapping
description: Configure Service Mapping and MID Servers to work together.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# MID Server configuration for Service Mapping

Configure Service Mapping and MID Servers to work together.

## What is the MID Server

The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server. MID Servers, which are located in the enterprise private network, facilitate communication between servers on the network and some ServiceNow applications, such as Service Mapping, and Discovery.

**Note:** If the Service Mapping \(com.sn\_itom\_pattern\) plugin is activated on the instance and a language plugin \(for example, Spanish\) is also activated, make sure that the MID Server language is also set to English/None on the user record.

## MID Server selection criteria

Most environments require multiple MID Servers, with Service Mapping using the relevant MID Server for discovery. MID Servers have the following selection criteria that Service Mapping can use to choose the relevant MID Server:

-   Application — defines what application a MID Server works with. Set it to Service Mapping to reserve this MID Server exclusively to Service Mapping discovery requests. Alternatively, set it to ALL to allow any ServiceNow application to use this MID Server.
-   Capability — defines the network capability. For Service Mapping, set this parameter to ALL or any combination of SSH, WMI, SNMP, and Cloud Provisioning and Governance . See Configure MID Server capabilities.

-   IP range — limits operation of this MID Server to this IP range. Service Mapping does not choose this MID Server for a discovery request whose endpoint is outside this IP range. See Configure an IP address range for the MID Server.

    **Note:** For information on how to bypass MID Server configuration based on IP range, see [Fine-tune Service Mapping with MID affinity and IP reuse](network-location-mid-affinity-td-discovery.md).


Service Mapping selects a MID Server using the following algorithm:

-   Service Mapping chooses the MID Server whose selection criteria best match the parameters of the discovery request.
-   If there are no MID Servers with matching selection criteria, Service Mapping chooses the default MID Server.
-   If there are no MID Servers with matching selection criteria or default MID Server, Service Mapping cannot start the discovery process.

While by default Service Mapping uses this algorithm in all deployments upgraded from Istanbul or Jakarta, it can support both new and legacy algorithms for selecting a MID Server. For more information, see [Choose MID Server selection algorithm](../task/choose-mid-selection-algorithm.md).

## Default MID Servers for Service Mapping

In addition to selection criteria, you can configure one of the MID Servers as the default server that Service Mapping uses. If there are no MID Servers with matching application, capability, or IP range, Service Mapping uses the default MID Server. See Configure a default MID Server for each application.

## Using PowerShell for discovery

MID Servers can use PowerShell to directly communicate with Windows servers using both WMI and WinRM protocols. For Windows services using the WinRM protocol, the PowerShell process establishes a secure PSSession \(PowerShell Remoting session\) that stays open until the MID Server finishes querying a Windows server. For Windows servers using the WMI protocol, the PowerShell process sends every PowerShell command with credentials.

If you do not configure MID Servers to use PowerShell and PowerShell Remoting, MID Servers use WMI.

ServiceNow now supports PowerShell 3.0 up to 5.1.

## MID Server credential-less discovery with Nmap

If the MID Server does not have sufficient credentials to access a device or application, it can run Network Mapper \(Nmap\) commands to collect basic information without using credentials. Credential-less discovery with Nmap requires additional configuration as described in Install and uninstall Nmap on a MID Server.

ServiceNow applications refer to devices and applications that comprise a service instance as configuration items \(CIs\).

## Placing MID Servers

The number of MID Servers that you require and where you place them depends on your organization needs. If you want to map devices and applications inside your private network, place the MID Servers inside the private network. If you want to map devices and applications located in the DMZ, place the MID Servers both in the DMZ and inside the private network.

![Placing MID Servers inside private network](../image/SNcomponentsSMtopology.png "Placing MID Servers inside private network")

In deployments where domain separation is enabled and domains are configured to form a hierarchy, MID Servers must be placed in the lowest domain level, a "leaf domain".

![Placing MID Servers to support domain separation](../image/MIDServerDeplDomainSep.png "Placement of MID Servers in domain-seprated environments")

Once MID Servers MID Servers are installed, configure them to work with Service Mapping for the best discovery results.

-   **[Choose MID Server selection algorithm](../task/choose-mid-selection-algorithm.md)**  
Service Mapping supports the new and the legacy algorithms for selecting a MID Server for a discovery request. Depending on your organization needs, you can choose which algorithm to enable.
-   **[MID Server configuration for Service Mapping in upgraded deployments](MID-selection-criteria-upgrade.md)**  
For ServiceNow deployments upgraded from earlier versions to Istanbul, Service Mapping uses the legacy algorithm to choose a MID Server for a discovery request.
-   **[Configure a default MID Server for Service Mapping for upgraded deployments](../task/config-default-mid-for-sm.md)**  
In deployments upgraded to Istanbul or earlier, Service Mapping uses the default MID Server when it cannot find a MID Server with the matching IP range. Configuring a default MID Server improves the discovery process.

**Parent Topic:**[Configuring Service Mapping](service-mapping-setup.md)

**Related topics**  


[PowerShell for Discovery and Service Mapping](../../discovery/reference/r_PowerShellForDiscovery.md)

[Pattern-based discovery in Service Mapping](pattern-based-discovery.md)

[bundle-platcap.c_MIDServerConnectionPrerequisites]

[Credential-less Discovery with Nmap](../../discovery/concept/nmap-credential-less-discovery.md)

[Credential-less Application Discovery](../../discovery/reference/credential-less-app-discovery.md)

[bundle-platcap.c_DeployMultipleMIDServers]

[bundle-platcap.mid-server-installation]

[MID Server properties used by Service Mapping](../reference/mid-server-properties-service-mapping.md)

