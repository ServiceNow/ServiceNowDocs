---
title: Configuring MID Servers
description: After installing and validating your MID Servers, ensure that they have access to sufficient system resources, probe the proper targets, and communicate with the instance as expected. Configure MID Server selection criteria, create clusters for failover protection, and set up MID Servers in different domains to protect data.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configuring MID Servers

After installing and validating your MID Servers, ensure that they have access to sufficient system resources, probe the proper targets, and communicate with the instance as expected. Configure MID Server selection criteria, create clusters for failover protection, and set up MID Servers in different domains to protect data.

<table id="table_qf5_z54_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>Some of these configuration procedures rely on data found in the MID Server [references home page](mid-server-reference-information.md). See that page for links to the parameters, properties, and privileged commands you need to fine tune the behavior of your MID Servers. You can apply controls to individual MID Servers or to all the MID Servers in your environment. Remember to restart the MID Server after any configuration change for those changes to take effect.

## MID Server selection

MID Servers are selected for use based on three criteria: applications, IP address or range, and capabilities. You can designate specific applications for a given MID Server, such as Discovery or Orchestration. You can specify an IP address or a range that a MID Server is allowed to work within. Some applications require specific capabilities, and so are restricted to MID Servers with those capabilities.

-   **[MID Server selection](c_MIDServerSelector.md)**

    Configure the way your instance selects a MID Server, either by application, IP address ranges, network capability, or behavior.

-   **[MID Server capabilities](../reference/r_MIDServerCapabilities.md)**

    Create capabilities that define the specific functions of a MID Server within an IP address range.

-   **[MID Server IP range auto-assignment](mid-servers-auto-assignment.md#)**

    Configure the system to automatically assign a qualified MID Server to a subnet by that subnet's IP address range.

-   **[Map an IP address to a DNS name](../task/t_MapIPAddressToDNSName.md)**

    Map host server DNS names to IP addresses if your MID Server manages resources within defined IP ranges.

-   **[Configure MID Server as WinRM trusted host](../task/enable-winRM-MID-servers.md)**

    Add servers, which are part of WinRM, as trusted hosts on all MID Servers that Discovery or Service Mapping use for discovery.

-   **[File permission enforcement for Windows MID Servers](mid-non-admin-permission.md)**

    To improve security, Windows MID Servers will enforce Windows file permission restrictions. This will prevent compromised accounts from accessing unauthorized files by restricting their permissions to the minimum necessary for their role.


## MID Server clusters

MID Server clusters are groups of MID Servers which provide support to each other in the forms of load balancing and fail-over protection. Work sent to a MID Server that is part of a cluster is automatically balanced between all the MID Servers in that cluster. MID Servers in a fail-over cluster each have a configured order that the platform uses to determine which MID Server to use next in case of failure.

-   **[Create a MID Server cluster](../task/t_ConfigureAMIDServerCluster.md#)**

    Create a MID Server cluster for load balancing and fail-over protection.

-   **[Set thread use](../task/t_SetMIDServerThreadUse.md)**

    Set the number of threads your MID Server uses for the desired MID Server speed, based on hardware capabilities and competing applications running on the host.


## Domain separation

Domain separation segregates MID Servers based on the records they can access. The credentials configured in a MID Server's config.xml file determine which records that MID Server can read, update, or create. You can specify MID Server policy records that only MID Servers from the same domain can use.

-   **[MID Server domain separation](c_MIDServerDomainSeparation.md#)**

    Set up your MID Servers in different domains to restrict the records and credentials that a MID Server can access.

-   **[Synchronize a JAR file to MID Servers](../task/t_SynchronizeAJARFiletoMIDServers.md)**

    Upload a JAR file to an instance and synchronize it to all MID Servers connected to that instance. Use JAR file synchronization to create policies that only a MID Server from the same domain can use.


## MID Servers used for credential-less Discovery

MID Servers that are used for [credential-less Discovery](https://www.servicenow.com/docs/access?context=nmap-credential-less-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) require special configuration to run Network Mapper \(Nmap\) commands on target computers.

[Install and uninstall Nmap on a MID Server](../task/install-nmap-on-mid-server.md#)

You must install Nmap on each MID Server running on a Windows host. When given the proper capability, those MID Servers can discover some basic information about CIs in your network if normal authentication fails.

## MID Server extensions

-   **[vCenter event collector](c_VCenterEventProcessorExtension.md#)**

    The vCenter event collector listens for vCenter-related events and updates the CMDB accordingly. The event collector allows the CMDB to be updated with changes to virtual machines \(VMs\), in addition to the updates detected by Discovery. A change to a VM is sent as an event from the vCenter server to the vCenter event collector. When an event is received, the CMDB is updated accordingly. Full vCenter Discovery does not need to rerun. For some events, such as powered on and powered off events, Discovery does not need to run again at all. For most events, Discovery runs only on the necessary vCenter resource.

-   **[SNMP trap collector extension](c_SNMPTrapCollectorExtension.md#)**

    The SNMP trap collector is a MID Server extension that listens for SNMP traps from the devices on your network. Upon receiving a trap, the MID Server sends the trap to the instance for further processing by Event Management. If Event Management is not active, traps are not processed and are discarded by the instance.


