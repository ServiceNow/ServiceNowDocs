---
title: Discovery for VMware vCenter
description: Discovery can explore the VMware vCenter process running on a Windows or Linux host. IPv6 is supported for discovery in VMware vCenter.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/c\_DiscoveryForVMwareVCenter.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 4
keywords: [VMware vCenter, Discovery VMware vCenter]
breadcrumb: [Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Discovery for VMware vCenter

Discovery can explore the VMware vCenter process running on a Windows or Linux host. IPv6 is supported for discovery in VMware vCenter.

**Note:**

If a Windows or Linux server is running vCenter application, after creating the vCenter CI, a "Runs on" relationship to the Windows or Linux server host is created.

When a vCenter application is running on a dedicated vCenter appliance, a "Runs on" relationship to the vCenter CI isn’t created.

## Tested vCenter versions

The ServiceNow® platform supports vCenter API versions 4.0 and higher. The following versions were tested with the Australia release:

-   vCenter versions 9.0 and earlier
-   vCenter appliance version 6.7 and earlier

For installations based on the vCenter appliance, a server CI is created for the vCenter appliance and the following fields are populated:

-   NameIP
-   AddressMAC
-   AddressDiscovery
-   Source

**Note:** If you're discovering SUSE Linux hosts for vCenter appliances, version 6.0 and earlier, observe these [SSH restrictions](https://kb.vmware.com/s/article/2100508).

See [Data collected for VMware Cloud Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/data-collected-vmware-cloud-disco.md) for a description of the VMware architecture and component relationships.

## vCenter discovery process

After classifying vCenter, Discovery launches the VMware - vCenter Datacenters probe, which in turn launches specific probes that return information about ESX machines, virtual machines, and other vCenter objects. The vmapp port probe is also configured to launch the VMware - vCenter Datacenters probe.

**Note:** For accurate relationship mapping between server CIs and vCenter resources \(such as ESX hosts and datastores\), you should initiate discovery of the vCenter environment before discovering Server CIs. This approach helps Discovery associate servers with their corresponding vCenter-managed infrastructure more effectively.

## VMWare credentials

To access vCenter with a domain account, specify the domain with the user name in the credential record using a supported format, such as **Domain\\UserName** or **username@domain**. The VMware credentials must have a read-only role in vCenter. For Software Asset Management \(SAM\) tracking, the credentials also require the "Assign license" privilege in vCenter, also known as the License Admin privilege.

**Important:** Windows credentials aren't necessary for vCenter Discovery when valid [VMware credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_VMwareCredentialsForm.md) are used.

## Updating the CMDB with vCenter event collector

In addition to finding vCenter data through the standard discovery process, Discovery can also update the CMDB by detecting vCenter events through a MID Server extension called the [vCenter event collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_VCenterEventProcessorExtension.md).

The event collector allows the CMDB to be updated with changes to virtual machines \(VMs\), in addition to the updates detected by Discovery. A change to a VM is sent as an event from the vCenter server to the vCenter event collector. When an event is received, the CMDB is updated accordingly. Full vCenter Discovery does not need to rerun. For some events, such as powered on and powered off events, Discovery does not need to run again at all. For most events, Discovery runs only on the necessary vCenter resource.

For instructions on configuring vCenter events, see [Configure and run the vCenter event collector extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_VCenterEventProcessorExtension.md).

## VMs deleted from vCenter

When a VM is deleted from vCenter, the ServiceNow instance updates the VM's record in the VM Instance \[cmdb\_ci\_vm\_instance\] table. The field changes depend on whether the update comes from Discovery or from the vCenter event collector:

-   vCenter Discovery sets **State** to Terminated, **Install Status** to Retired, and **Operational status** to Non-operational for every VM that's no longer in vCenter.
-   The vCenter event collector sets **State** to Terminated and **Install Status** to Retired when it receives a VmRemovedEvent event. It doesn't change **Operational status**. The event collector doesn't save these changes in the following cases:
    -   The VM is already marked stale in CMDB Health.
    -   The VM's **State** is already Terminated or is empty.

## CIs removed from vCenter

When a vCenter CI, such as a virtual machine, is removed, the ServiceNow instance marks it as "stale" in the CMDB, using either of these procedures:

-   When Discovery runs, it creates an audit record in the [Components installed with CMDB Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_TablesInstalledCMDBHealth.md) table for the missing CI and marks the CI "stale". It also updates the CI fields every time, as described in [VMs deleted from vCenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/c_DiscoveryForVMwareVCenter.md).
-   When the instance is configured to collect vCenter events, the system can also create a "stale" audit record for the CI in the CMDB Health Result \[cmdb\_health\_result\] table. This record is created from the VmRemovedEvent event, without having to run Discovery. The event collector handles these cases differently:
    -   The CI is already marked stale: The event collector skips the event. It doesn't create another stale record or update the CI fields.
    -   The VM's **State** is already Terminated or empty: The event collector creates the stale record but doesn't save the CI field changes.

**Note:** When the **Staleness** setting is configured, the dependency view \(BSM map\) grays out stale CIs in its relationship diagram to indicate that they were removed from vCenter.

To prevent stale CI records from being created during VMware discovery, set the system property **glide.cmdb.health.src.cmdb\_health\_audit\_only** to **true**. When this property is true, only CMDB Health audits create records in the CMDB Health Result \[cmdb\_health\_result\] table. Records from the Cloud Discovery source, which includes vCenter Discovery and the vCenter event collector, aren't created. Discovery and the event collector still update the CI fields, as described in [VMs deleted from vCenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/c_DiscoveryForVMwareVCenter.md). For more information, see [CMDB Health system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_CMDBHealthProperties.md).

You have the option of creating a [CMDB remediation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_CreateCMDBRemediationRule.md) to automatically execute a remediation workflow that can, for example, delete stale CIs. For more information on stale CIs, see [CMDB Health Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_CMDBHealthMetrics.md).

## vCenter Discovery on Windows host

Windows credentials aren't necessary for vCenter Discovery, when valid VMware credentials are used.

**Parent Topic:**[Operating systems discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/c_Computers.md)

