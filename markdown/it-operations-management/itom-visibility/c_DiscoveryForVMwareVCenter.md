---
title: Discovery for VMware vCenter
description: Discovery can explore the VMware vCenter process running on a Windows or Linux host. IPv6 is supported for disocvery in VMware vCenter.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [VMware vCenter, Discovery VMware vCenter]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Discovery for VMware vCenter

Discovery can explore the VMware vCenter process running on a Windows or Linux host. IPv6 is supported for disocvery in VMware vCenter.

**Note:**

If a Windows or Linux server is running vCenter application, after creating the vCenter CI, a "Runs on" relationship to the Windows or Linux server host is created.

When a vCenter application is running on a dedicated vCenter appliance, a "Runs on" relationship to the vCenter CI isn’t created.

## Tested vCenter versions

The ServiceNow® platform supports vCenter API versions 4.0 and higher. The following versions were tested with the Australia release:

-   vCenter versions 8.0 and earlier
-   vCenter appliance version 6.7 and earlier

For installations based on the vCenter appliance, a server CI is created for the vCenter appliance and the following fields are populated:

-   NameIP
-   AddressMAC
-   AddressDiscovery
-   Source

**Note:** If you're discovering SUSE Linux hosts for vCenter appliances, version 6.0 and earlier, observe these [SSH restrictions](https://kb.vmware.com/s/article/2100508).

See [Data collected for VMware Cloud Discovery](../reference/data-collected-vmware-cloud-disco.md) for a description of the VMware architecture and component relationships.

## vCenter discovery process

After classifying vCenter, Discovery launches the VMware - vCenter Datacenters probe, which in turn launches specific probes that return information about ESX machines, virtual machines, and other vCenter objects. The vmapp port probe is also configured to launch the VMware - vCenter Datacenters probe.

**Note:** For accurate relationship mapping between server CIs and vCenter resources \(such as ESX hosts and datastores\), you should initiate discovery of the vCenter environment before discovering Server CIs. This approach helps Discovery associate servers with their corresponding vCenter-managed infrastructure more effectively.

## VMWare credentials

To access vCenter with a domain account, specify the domain with the user name in the credential record using a supported format, such as **Domain\\UserName**. The VMware credentials must have a read-only role in vCenter. For Software Asset Management \(SAM\) tracking, the credentials also require the "Assign license" privilege in vCenter, also known as the License Admin privilege.

**Important:** Windows credentials aren't necessary for vCenter Discovery when valid [VMware credentials](https://www.servicenow.com/docs/access?context=r_VMwareCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US) are used.

## Updating the CMDB with vCenter event collector

In addition to finding vCenter data through the standard discovery process, Discovery can also update the CMDB by detecting vCenter events through a MID Server extension called the [vCenter event collector](https://www.servicenow.com/docs/access?context=c_VCenterEventProcessorExtension&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

The event collector allows the CMDB to be updated with changes to virtual machines \(VMs\), in addition to the updates detected by Discovery. A change to a VM is sent as an event from the vCenter server to the vCenter event collector. When an event is received, the CMDB is updated accordingly. Full vCenter Discovery does not need to rerun. For some events, such as powered on and powered off events, Discovery does not need to run again at all. For most events, Discovery runs only on the necessary vCenter resource.

For instructions on configuring vCenter events, see [Configure and run the vCenter event collector extension](https://www.servicenow.com/docs/access?context=c_VCenterEventProcessorExtension&version=australia&pubname=australia-servicenow-platform&section=t_ConfigVCenEvntProcExt&ft:locale=en-US).

## VM deleted from vCenter

If the VM is deleted from vCenter, the cmdb\_ci\_vm\_instance state changes to terminated and the Status field changes to retired.

## CIs removed from vCenter

When a vCenter CI, such as a virtual machine, is removed, the ServiceNow instance marks it as "stale" in the CMDB, using either of these procedures:

-   When Discovery runs, it creates an audit record in the [Components installed with CMDB Health](https://www.servicenow.com/docs/access?context=r_TablesInstalledCMDBHealth&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) table for the missing CI and marks the CI "stale".
-   If the instance is configured to collect vCenter events, the system can also create a "stale" audit record for the CI in the CMDB Health Result \[cmdb\_health\_result\] table from the VmRemovedEvent event, without having to run Discovery.

**Note:** When the **Staleness** setting is configured, the dependency view \(BSM map\) grays out stale CIs in its relationship diagram to indicate that they were removed from vCenter.

To avoid stale CI health indicators from being generated during VMware discovery, set the system property **glide.cmdb.health.src.cmdb\_health\_audit\_only** to **true**. This disables stale CI reporting from the VMware discovery source, enabling you to manage the CI life cycle through other means. For more information, see [CMDB Health system properties](https://www.servicenow.com/docs/access?context=r_CMDBHealthProperties&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

You have the option of creating a [CMDB remediation rule](https://www.servicenow.com/docs/access?context=t_CreateCMDBRemediationRule&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) to automatically execute a remediation workflow that can, for example, delete stale CIs. For more information on stale CIs, see [CMDB Health Metrics](https://www.servicenow.com/docs/access?context=r_CMDBHealthMetrics&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## vCenter Discovery on Windows host

Windows credentials aren't necessary for vCenter Discovery, when valid VMware credentials are used.

**Parent Topic:**[Operating systems discovery](c_Computers.md)

