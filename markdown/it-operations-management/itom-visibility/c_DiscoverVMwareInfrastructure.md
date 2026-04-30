---
title: Discovery for VMware virtualization
description: A Discovery schedule for VMware virtualization can discover vCenter and ESX hosts as well as individual ESXi hosts that manage VMs and related components without a vCenter.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-12-02"
reading_time_minutes: 1
keywords: [VMware virtualization, VMware infrastructure, VMware Discovery]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Discovery for VMware virtualization

A Discovery schedule for VMware virtualization can discover vCenter and ESX hosts as well as individual ESXi hosts that manage VMs and related components without a vCenter.

These options are available for getting VMware vCenter data:

-   Discovery runs the [VMware - vCenter Datacenters](../reference/r_ListOfDiscoveryProbes.md) probe when it identifies a VMware vCenter process running on a Windows machine or detects activity with the vmapp port probe.
-   [Classic Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) can run any of the vCenter probes from a workflow

To discover VMware data without a vCenter, use standalone ESXi discovery.

**Note:** See the knowledge article [KB0687582](https://support.servicenow.com/kb_view.do?sysparm_article=KB0687582) for information on model\_id and manufacturer.

-   **[Discovery for VMware vCenter](c_DiscoveryForVMwareVCenter.md)**  
Discovery can explore the VMware vCenter process running on a Windows or Linux host. IPv6 is supported for disocvery in VMware vCenter.
-   **[ESXi server discovery](../reference/r_DiscoverESXServers.md)**  
Discovery identifies and classifies information about ESXi servers and ESXi resource pools through the discovery of vCenter and not from the direct discovery of any ESXi servers.
-   **[Standalone ESXi discovery](../reference/StandaloneESXiDiscovery.md)**  
Standalone ESXi discovery supports discovery of individual ESXi servers that host virtual machines \(VMs\) and related components without a vCenter. Various CIs and relationships are discovered as part of a discovery schedule.
-   **[Discovery for VMware virtual machines](c_VMwareVirtualMachines.md)**  
Discovery gathers information about virtual machines managed by VMware vCenter.
-   **[VM instance state and status fields](../reference/vm-instance-state-and-status-fields.md)**  
These tables represent the state and status of the cmdb\_ci\_vm\_instance in various flows such as vCenter Discovery and vCenter Events and the Business Rules which are triggered.
-   **[Datastore Discovery](c_DatastoreDiscovery.md)**  
A datastore is a storage object for virtual machines that are hosted on an ESXi server.

**Parent Topic:**[Operating systems discovery](c_Computers.md)

