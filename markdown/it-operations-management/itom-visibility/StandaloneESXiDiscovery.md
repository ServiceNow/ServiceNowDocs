---
title: Standalone ESXi discovery
description: Standalone ESXi discovery supports discovery of individual ESXi servers that host virtual machines \(VMs\) and related components without a vCenter. Various CIs and relationships are discovered as part of a discovery schedule.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-12-02"
reading_time_minutes: 7
keywords: [ESXi server, standalone ESXi, ESXi server discovery]
breadcrumb: [Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Standalone ESXi discovery

Standalone ESXi discovery supports discovery of individual ESXi servers that host virtual machines \(VMs\) and related components without a vCenter. Various CIs and relationships are discovered as part of a discovery schedule.

## Required roles

Users with the **itil** and **asset** roles can access ESXi configuration item \(CI\) records. To run a standalone ESXi discovery, users must have the **discovery\_admin** role.

## VMware credentials

To run a standalone ESXi discovery, you need VMware credentials. Create the credentials by navigating to **Discovery** &gt; **Credentials** &gt; **VMware Credentials.**

If you use a domain account to access the ESXi host, specify the domain with the user name in the credential record in one of the supported formats, such as **Domain\\UserName**.

**Note:** The VMware credentials must have read-only role in the ESXi host.

## Requirements

-   Make sure the Discovery \(com.snc.discovery\) plugin is installed and activated and that you have upgraded to Yokohama or later.
-   Activate the ESXi trigger probe. Navigate to the Trigger Probe \[trigger\_probe\_m2m\] table. The esxi record is inactive by default. Mark Active as true to enable Standalone ESXi discovery.
-   Create a new Discovery schedule for the host with the appropriate IP address of the ESXi host.

**Note:** If both SSH and ESXi are triggered, SSH is launched first and may cause Discovery to complete with the message "ESX Discovery is only supported through the vCenter." In this case, open the Unix - Classify probe and set ESX - OS inactive.

## ESXi server Discovery components

Discovery identifies ESXi servers based on the correlation ID \(BIOS UUID\), when the hardware manufacturer is on a certified inclusion list. If the manufacturer is on the list, the correlation ID must be unique. If the manufacturer is not on the certified inclusion list, the Managed Object Reference ID \(MORID\) and Serial Number are checked as well.

After Shazzam runs, it checks for the port probe esxi. Discovery then launches the VMWare - Standalone ESXi Server probe, which then launches the probes that explore the ESXi server. Other existing Discovery probes are also launched. For the complete list of probes, see [List of Discovery probes](r_ListOfDiscoveryProbes.md).

<table id="table_jmv_4df_4nb"><thead><tr><th>

Component

</th><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Service

</td><td>

ESXi

</td><td>

IP Service ESXi - VMWare VM console is defined for the Port 902.

</td></tr><tr><td>

Port Probe

</td><td>

esxi

</td><td>

ESXi Server Appliance web user interface. It is triggered by the IP Service ESXi and it triggers the probe VMWare - Standalone ESXi Server.

</td></tr><tr><td>

Probe

</td><td>

VMWare - Standalone ESXi Server

</td><td>

Probe to get information about an ESXi server.

</td></tr><tr><td>

Probe

</td><td>

VMWare - vCenter ESX Hosts

</td><td>

Creates records for ESXi servers and host mounts. Triggers other probes.-   VMware - vCenter ESX Hosts Storage
-   VMware - vCenter Datastores
-   VMware - vCenter Networks
-   VMware -vCenter VMs

</td></tr><tr><td>

Probe

</td><td>

VMWare - vCenter ESX Hosts Storage

</td><td>

Creates records for ESXi host hardware: network adapters, disks, HBAs, FC ports, iSCSI and FC disks. Creates relationships between DAS/iSCSI/FC disks and datastore disks.

</td></tr></tbody>
</table>Basic server data from ESXi hosts is collected by the VMware - vCenter ESX Hosts probe.

## ESXi Standalone server data

Discovery uses multiple existing probes to collect this data from ESXi. The data is saved in various tables. Some of the CIs which have the "server" field have a reference to ESXi Host \(for example, cmdb\_ci\_esx\_server\).

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Memory \(MB\)|memory|
|CPUs|cpus|
|Disks|disks|
|Network adapters|nics|
|Object ID|object\_id|
|Server|server|
|State|state|
|Correlation ID|correlation\_id|
|VM Instance UUID|vm\_instance\_uuid|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Capacity \(GB\)|capacity|
|Free space \(GB\)|freespace|
|Accessible|accessible|
|Type|type|
|Object ID|object\_id|
|Server|server|
|URL|url|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Object ID|object\_id|
|Server|server|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|MAC Address|mac\_address|
|IP Address|ip\_address|
|Netmask|netmask|
|Configuration Item|cmdb\_ci|
|Object ID|object\_id|
|Mac manufacturer|mac\_manufacturer|
|DHCP Enabled|dhcp\_enabled|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|VMware vCenter Datastore|datastore|
|ESX Server|esx\_server|
|Accessible|accessible|
|Access Mode|access\_mode|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Manufacturer|manufacturer|
|Location|location|
|Description|short\_description|
|Class|sys\_class\_name|
|Updated|sys\_updated\_on|
|Maintenance schedule|maintenance\_schedule|
|Correlation ID|correlation\_id|
|Datastore|datastore|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|CPU reserved \(MHz\)|cpu\_reserved\_mhz|
|CPU limit \(MHz\)|cpu\_limit\_mhz|
|CPU shares|cpu\_shares|
|Memory reserved \(MB\)|mem\_reserved\_mb|
|Memory limit \(MB\)|mem\_limit\_mb|
|Memory shares|mem\_shares|
|Object ID|object\_id|
|Server|server|
|Managed object reference ID|morid|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Operating System|os|
|OS Version|os\_version|
|Description|short\_description|
|Class|sys\_class\_name|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Mac Address|mac\_address|
|Netmask|netmask|
|Configuration Item|cmdb\_ci|
|Mac manufacturer|mac\_manufacturer|
|DHCP Enabled|dhcp\_enabled|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Computer|computer|
|Size|size|
|Manufacturer|manufacturer|
|Model ID|model\_id|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Model ID|model\_id|
|Computer|computer|
|WWNN|wwnn|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|WWNN|wwnn|
|WWPN|wwpn|
|Speed|speed|
|Controller|controller|
|Computer|computer|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Computer|computer|
|Size|size|
|Provided by|provided\_by|
|IQN|iqn|
|Device LUN|device\_lun|
|Storage type|storage\_type|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|Name|name|
|Computer|computer|
|Size|size|
|Provided by|provided\_by|
|Device LUN|device\_lun|
|WWN|wwn|
|Status|install\_status|

|Field label|Column name|
|-----------|-----------|
|IP Address|ip\_address|
|IP version|ip\_version|
|Netmask|netmask|
|Nic|nic|
|Status|install\_status|

## Relationships

![Flowchart of standalone ESXi discovery relationships](../image/standalone_ESXi_relationships_.png "Standalone ESXi discovery relationships")

## Resource pools

Standalone ESXi discovery also fetches the resource pools on the host including the root resource pool. This root resource pool is always hidden for every ESXi host. The root resource pool may not be visible in the VSphere web client for the ESXi host, but you can view it using the mob browser.

Navigate to this URL: **&lt;domain name/or ip\_address&gt;/mob/?moid=ha-root-pool**

The root resource pool groups the resources of that host. Other child resource pools can also be created from the root resource pool. The root is identified in the ESXi host with the Managed Object ID: ha-root-pool.

## Forward migration

If you were using standalone ESXi discovery and now the same ESXi is part of vCenter, you can use vCenter discovery instead. Create a vCenter discovery schedule and trigger it. Triggering a vCenter discovery creates duplicate CIs in the following tables as the identifiers for the CIs are different when ESXi is standalone or part of vCenter:

-   VMware VCenter Network \[cmdb\_ci\_vcenter\_network\]
-   ESX Resource Pool \[cmdb\_ci\_esx\_resource\_pool\]
-   VMware VCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]
-   Datastore Disk \[cmdb\_ci\_vcenter\_datastore\_disk\]

To avoid duplicates, you must mark the CIs created by standalone ESXi discovery in the above four tables as retired. When vCenter discovery is triggered, the vCenterESXHostsSensor script include checks for all the ESXi servers whether they were previously discovered as standalone ESXi server. If yes, it automatically triggers the ESXMigrationUtil script to mark all the previously discovered duplicate CIs as retired.

**Note:** If you want to trigger migration manually, you can do so by executing the following script from the background script: // @params esx\_sys\_ids – array of sys ids of all the ESXi servers which need to be migrated.

```
ESXMigrationUtil. retireCIsForESXForwardMigration(esx_sys_ids)
```

Once an ESXi server is migrated to vCenter, triggering a standalone ESXi discovery schedule on the same ESXi host will result in an error. Discovery will be aborted with an error message that “This ESXi is part of vCenter &lt;IP\_address of Vcenter&gt; discovery schedule. Aborting discovery”.

**Parent Topic:**[Discovery for VMware virtualization](../concept/c_DiscoverVMwareInfrastructure.md)

**Related topics**  


[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

[ESXi server discovery](r_DiscoverESXServers.md)

[Discovery for VMware virtual machines](../concept/c_VMwareVirtualMachines.md)

[VM instance state and status fields](vm-instance-state-and-status-fields.md)

[Datastore Discovery](../concept/c_DatastoreDiscovery.md)

