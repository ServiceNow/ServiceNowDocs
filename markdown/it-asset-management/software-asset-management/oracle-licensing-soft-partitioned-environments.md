---
title: Oracle Database and WebLogic Server licensing in soft-partitioned environments
description: The Software Asset Management application supports Oracle Database and WebLogic Server licensing rules in soft-partitioned environments, such as VMware virtualization technology.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Oracle Database and WebLogic Server licensing in partitioned environments, Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Database and WebLogic Server licensing in soft-partitioned environments

The Software Asset Management application supports Oracle Database and WebLogic Server licensing rules in soft-partitioned environments, such as VMware virtualization technology.

Soft partitioning enables you to segment the operating system \(OS\) of the environment into different OS types and OS versions by using OS resource managers. OS resource managers limit the number of processors that each Oracle database or WebLogic server can run on by creating segments in which CPU resources are allocated to applications within the same OS. For more information about Oracle licensing and soft partitioning, refer to the [Oracle Help Center](https://docs.oracle.com/en/).

## VMware vSphere

VMware vSphere is a virtualization platform through which you can install and run Oracle databases or WebLogic servers on virtual machines \(VMs\). To run an Oracle database or WebLogic server on a VM, you must license all processors on the underlying physical ESXi host that is running your VM. If your physical ESXi host is running multiple VMs simultaneously, you must still license all processors on the host regardless of how many VMs are running the database or WebLogic server.

Oracle licensing on VMware vSphere is based on the VMware vMotion capability that is associated with each vSphere version. VMware vMotion is the VMware vSphere technology that enables VMs to migrate from one physical ESXi host to another without service interruptions.

The Oracle publisher pack supports the following Oracle licensing models on VMware vSphere:

|VMware vSphere version|VMware vMotion capability|Licensing model|
|----------------------|-------------------------|---------------|
|VMware vSphere ESXi 5.0 and earlier|VMs can migrate to any physical ESXi host within the same shared storage under the same datacenter.|You must license the processors on all physical ESXi hosts within the same shared storage under the same datacenter.|
|VMware vSphere ESXi 5.1-5.5|VMs can migrate to any physical ESXi host within the same VMware vCenter Server instance.|You must license the processors on all physical ESXi hosts within the same VMware vCenter Server instance.|
|VMware vCenter Server 6.0 and later|VMs can migrate to physical ESXi hosts within any VMware vCenter Server instance across your network. Migration is supported only on physical hosts that run VMware vSphere ESXi 5.1 or later on VMware vCenter Server 6.0 and later instances.|You must license the processors on all physical hosts that run VMware vSphere ESXi 5.1 or later within all VMware vCenter Server 6.0 and later instances across your network.|

**Important:** If you enable the **Use host affinity for reconciling licenses for Oracle databases and WebLogic servers on VMware at the vCenter\(s\) aggregation level** option in your [Software Asset Management properties](../reference/sam-properties.md), the Software Asset Management application honors all VM-Host affinity rules when reconciling Oracle licenses within your VMware vCenter Server instances. In this scenario, licensing is based on the sum of all physical ESXi hosts that the VMs can reside on, as specified in your VM-Host affinity rules.

![Oracle database licensing on VMware vSphere.](../image/oracle-vmware-licensing.png)

For more information about Oracle licensing on VMware, see [Understanding Oracle Certification, Support and Licensing for VMware Environments](https://www.vmware.com/content/dam/digitalmarketing/vmware/en/pdf/whitepaper/solutions/oracle/understanding_oracle_certification_support_licensing_vmware_environments-white-paper.pdf).

**Parent Topic:**[Oracle Database and WebLogic Server licensing in partitioned environments](oracle-licensing-partitioned-environments.md)

