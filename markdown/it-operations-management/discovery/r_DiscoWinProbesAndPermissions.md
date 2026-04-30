---
title: Windows probes and permissions
description: Discovery accesses devices and software by executing commands as a specific user on Windows computers.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 14
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Discovery, ITOM Visibility, IT Operations Management]
---

# Windows probes and permissions

Discovery accesses devices and software by executing commands as a specific user on Windows computers.

Most probes require access to Windows classes, properties, and registry entries. Certain probes also require additional access to Windows directories and resources. Security policies vary by organization, so there’s no one specific role or right to grant. Verify that the Windows user has `local admin` permission for these Windows components.

## Administrative shares

Windows administrative shares are hidden server resources that Discovery uses to store temporarily the results of processes run by specific probes. The MID Server script file **LaunchProc.psm1** launches the process, writes its output to the administrative share on the machine, and then retrieves the results for the MID Server. Access to administrative shares is restricted to users with administrative rights to the target. For example: Users, local or on the domain, who belong to the local administrators group.

With the New York release, all Windows probes using the WMI protocol call the **LaunchProc.psm1** script file and write to the admin$ share folder as default. If another network share is mounted on each Windows target, the folder could be changed by updating the [MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) **mid.powershell.target\_base\_dir**.

## Windows Classes

Most Windows probes access Windows classes and properties contained in those classes. Some Windows classes don’t specify a file namespace path. If an explicit path isn’t specified, ServiceNow uses `root\cimv2\<Class>` by default.

**Note:** Discovery of Cluster VIP isn’t supported.

|Probe|Windows Class|Property|
|-----|-------------|--------|
|Hyper-V - Cluster|`root\MSCluster\MSCluster_ClusterToNode`|**Antecedent**|
|Hyper-V - Cluster|`root\MSCluster\MSCluster_ClusterToNode`|**Dependent**|
|Hyper-V - Cluster|`root\MSCluster\MSCluster_Resource`|**Type**|
|Hyper-V - Resource Pools|`root\virtualization\Msvm_ResourcePool`|**AllocationUnits**|
|Hyper-V - Resource Pools|`root\virtualization\Msvm_ResourcePool`|**Capacity**|
|Hyper-V - Resource Pools|`root\virtualization\Msvm_ResourcePool`|**InstanceID**|
|Hyper-V - Resource Pools|`root\virtualization\Msvm_ResourcePool`|**Name**|
|Hyper-V - Resource Pools|`root\virtualization\Msvm_ResourcePool`|**ResourceSubType**|
|Hyper-V - Resource Pools|`root\virtualization\v2\Msvm_ResourcePool`|**AllocationUnits**|
|Hyper-V - Resource Pools|`root\virtualization\v2\Msvm_ResourcePool`|**Capacity**|
|Hyper-V - Resource Pools|`root\virtualization\v2\Msvm_ResourcePool`|**InstanceID**|
|Hyper-V - Resource Pools|`root\virtualization\v2\Msvm_ResourcePool`|**Name**|
|Hyper-V - Resource Pools|`root\virtualization\v2\Msvm_ResourcePool`|**ResourceSubType**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ComputerSystem`|**Description**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ComputerSystem`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ComputerSystem`|**EnabledState**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ComputerSystem`|**Name**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ComputerSystem`|**TimeOfLastStateChange**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_LogicalDisk`|**BlockSize**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_LogicalDisk`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_LogicalDisk`|**NumberOfBlocks**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_LogicalDisk`|**SystemName**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_MemorySettingData`|**AllocationUnits**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_MemorySettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_MemorySettingData`|**VirtualQuantity**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ProcessorSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_ProcessorSettingData`|**VirtualQuantity**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_SyntheticEthernetPortSettingData`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_SyntheticEthernetPortSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**BaseBoardSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**BIOSGUID**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**BIOSSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**ChassisSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\Msvm_VirtualSystemSettingData`|**SystemName**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ComputerSystem`|**Description**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ComputerSystem`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ComputerSystem`|**EnabledState**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ComputerSystem`|**Name**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ComputerSystem`|**TimeOfLastStateChange**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_LogicalDisk`|**BlockSize**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_LogicalDisk`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_LogicalDisk`|**NumberOfBlocks**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_LogicalDisk`|**SystemName**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_MemorySettingData`|**AllocationUnits**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_MemorySettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_MemorySettingData`|**VirtualQuantity**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ProcessorSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_ProcessorSettingData`|**VirtualQuantity**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_SyntheticEthernetPortSettingData`|**ElementName**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_SyntheticEthernetPortSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**BaseBoardSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**BIOSGUID**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**BIOSSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**ChassisSerialNumber**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**InstanceID**|
|Hyper-V - Virtual Machines|`root\virtualization\v2\Msvm_VirtualSystemSettingData`|**SystemName**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_ActiveConnection`|**Antecedent**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_ActiveConnection`|**Dependent**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_VirtualEthernetSwitch`|**ElementName**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_VirtualEthernetSwitch`|**Name**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_VirtualSwitch`|**ElementName**|
|Hyper-V - Virtual Networks|`root\virtualization\Msvm_VirtualSwitch`|**Name**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_ActiveConnection`|**Antecedent**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_ActiveConnection`|**Dependent**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_VirtualEthernetSwitch`|**ElementName**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_VirtualEthernetSwitch`|**Name**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_VirtualSwitch`|**ElementName**|
|Hyper-V - Virtual Networks|`root\virtualization\v2\Msvm_VirtualSwitch`|**Name**|
|Windows - Active Connections Session|`Win32_OperatingSystem`|**Name**|
|Windows - Active Processes|`Win32_Process`|**Caption**|
|Windows - Active Processes|`Win32_Process`|**CommandLine**|
|Windows - Active Processes|`Win32_Process`|**CreationDate**|
|Windows - Active Processes|`Win32_Process`|**Description**|
|Windows - Active Processes|`Win32_Process`|**ExecutablePath**|
|Windows - Active Processes|`Win32_Process`|**Name**|
|Windows - Active Processes|`Win32_Process`|**ParentProcessId**|
|Windows - Active Processes|`Win32_Process`|**Priority**|
|Windows - Active Processes|`Win32_Process`|**ProcessId**|
|Windows - Amazon EC2|Win32\_ComputerSystemProduct|**UUID**|
|Windows - Azure Relationship|Win32\_ComputerSystemProduct|**UUID**|
|Windows - Classify|`root\MSCluster\MSCluster_Cluster`|**Name**|
|Windows - Classify|`root\MSCluster\MSCluster_ClusterToNode`|**Antecedent**|
|Windows - Classify|`root\MSCluster\MSCluster_ClusterToNode`|**Dependent**|
|Windows - Classify|`root\MSCluster\MSCluster_ClusterToResource`|**GroupComponent**|
|Windows - Classify|`root\MSCluster\MSCluster_ClusterToResource`|**PartComponent**|
|Windows - Classify|`root\MSCluster\MSCluster_Node`|**Name**|
|Windows - Classify|`root\MSCluster\MSCluster_Resource`|**Name**|
|Windows - Classify|`root\MSCluster\MSCluster_Resource`|**PrivateProperties**|
|Windows - Classify|`root\MSCluster\MSCluster_Resource`|**Type**|
|Windows - Classify|`root\virtualization\Msvm_ComputerSystem`|**Name**|
|Windows - Classify|`root\virtualization\v2\Msvm_ComputerSystem`|**Name**|
|Windows - Classify|`Win32_ComputerSystem`|**Domain**|
|Windows - Classify|`Win32_ComputerSystem`|**Name**|
|Windows - Classify|`Win32_OperatingSystem`|**Caption**|
|Windows - Classify|`Win32_OperatingSystem`|**Version**|
|Windows - Cluster|`root\MSCluster\MSCluster_Cluster`|**Caption**|
|Windows - Cluster|`root\MSCluster\MSCluster_Cluster`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_Cluster`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_Cluster`|**Status**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNetwork`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNetwork`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNetworkInterface`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNetworkInterface`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNode`|**Antecedent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToNode`|**Dependent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToQuorumResource`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToQuorumResource`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToResource`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToResource`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToResourceGroup`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ClusterToResourceGroup`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_Event`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_Event`|**Type**|
|Windows - Cluster|`root\MSCluster\MSCluster_Network`|**Address**|
|Windows - Cluster|`root\MSCluster\MSCluster_Network`|**AddressMask**|
|Windows - Cluster|`root\MSCluster\MSCluster_Network`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_Network`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_NetworkInterface`|**Address**|
|Windows - Cluster|`root\MSCluster\MSCluster_NetworkInterface`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_NetworkInterface`|**DeviceID**|
|Windows - Cluster|`root\MSCluster\MSCluster_NetworkInterface`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_NetworkInterface`|**Network**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Caption**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Characteristics**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Flags**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**NodeInstanceID**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**PrivateProperties**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**State**|
|Windows - Cluster|`root\MSCluster\MSCluster_Node`|**Status**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToActiveGroup`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToActiveGroup`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToActiveResource`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToActiveResource`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToNetworkInterface`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_NodeToNetworkInterface`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**Caption**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**PrivateProperties**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**Status**|
|Windows - Cluster|`root\MSCluster\MSCluster_Resource`|**Type**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroup`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroup`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroup`|**PrivateProperties**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroup`|**State**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroupToResource`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceGroupToResource`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceToDependentResource`|**Antecedent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceToDependentResource`|**Dependent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceToPossibleOwner`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceToPossibleOwner`|**PartComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceType`|**Description**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceType`|**DisplayName**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceType`|**Name**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceType`|**PrivateProperties**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceTypeToResource`|**GroupComponent**|
|Windows - Cluster|`root\MSCluster\MSCluster_ResourceTypeToResource`|**PartComponent**|
|Windows - Cluster|`Win32_NetworkAdapterConfiguration`|**IPAddress**|
|Windows - Cluster|`Win32_NetworkAdapterConfiguration`|**IPEnabled**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**BankLabel**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**Capacity**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**DataWidth**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**DeviceLocator**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**FormFactor**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**Manufacturer**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**MemoryType**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**PartNumber**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**SerialNumber**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**Speed**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**Status**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**Tag**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**TotalWidth**|
|Windows - CPU / Memory|`Win32_PhysicalMemory`|**TypeDetail**|
|Windows - CPU / Memory|Win32\_Processor|**Manufacturer**|
|Windows - CPU / Memory|Win32\_Processor|**MaxClockSpeed**|
|Windows - CPU / Memory|Win32\_Processor|**Name**|
|Windows - CPU / Memory|Win32\_Processor|**NumberOfCores**|
|Windows - CPU / Memory|Win32\_Processor|**NumberOfLogicalProcessors**|
|Windows - Get IIS Information|`root\MicrosoftIISv2\IIsWebServerSetting`|**LogFileDirectory**|
|Windows - Get IIS Information|`root\MicrosoftIISv2\IIsWebServerSetting`|**Name**|
|Windows - Get IIS Information|`root\MicrosoftIISv2\IIsWebServerSetting`|**SecureBindings**|
|Windows - Get IIS Information|`root\MicrosoftIISv2\IIsWebServerSetting`|**ServerBindings**|
|Windows - Get IIS Information|`root\MicrosoftIISv2\IIsWebServerSetting`|**ServerComment**|
|Windows - Get IIS Information|`root\WebAdministration\Site`|**Bindings**|
|Windows - Get IIS Information|`root\WebAdministration\Site`|**Id**|
|Windows - Get IIS Information|`root\WebAdministration\Site`|**LogFile**|
|Windows - Get IIS Information|`root\WebAdministration\Site`|**Name**|
|Windows - Get Physical Address for VIP|`root\MSCluster\MSCluster_NetworkInterface`|**Address**|
|Windows - Get Physical Address for VIP|`Win32_NetworkAdapterConfiguration`|**IPAddress**|
|Windows - Get Physical Address for VIP|`Win32_NetworkAdapterConfiguration`|**IPEnabled**|
|Windows - Hardware Information|`Win32_BaseBoard`|**SerialNumber**|
|Windows - Hardware Information|`Win32_BIOS`|**SerialNumber**|
|Windows - Hardware Information|`Win32_ComputerSystemProduct`|**IdentifyingNumber**|
|Windows - Hardware Information|`Win32_ComputerSystemProduct`|**UUID**|
|Windows - Hardware Information|`Win32_SystemEnclosure`|**ChassisTypes**|
|Windows - Hardware Information|`Win32_SystemEnclosure`|**SerialNumber**|
|Windows - Hardware &amp; Network Info|`Win32_BaseBoard`|**SerialNumber**|
|Windows - Hardware &amp; Network Info|`Win32_BIOS`|**SerialNumber**|
|Windows - Hardware &amp; Network Info|`Win32_ComputerSystemProduct`|**IdentifyingNumber**|
|Windows - Hardware &amp; Network Info|`Win32_ComputerSystemProduct`|**UUID**|
|Windows - Hardware &amp; Network Info|`Win32_IP4RouteTable`|**Destination**|
|Windows - Hardware &amp; Network Info|`Win32_IP4RouteTable`|**Mask**|
|Windows - Hardware &amp; Network Info|`Win32_IP4RouteTable`|**NextHop**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapter`|**Index**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapter`|**Manufacturer**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapter`|**NetConnectionID**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**Caption**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**DefaultIPGateway**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**DHCPEnabled**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**Index**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**IPAddress**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**IPEnabled**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**IPSubnet**|
|Windows - Hardware &amp; Network Info|`Win32_NetworkAdapterConfiguration`|**MACAddress**|
|Windows - Hardware &amp; Network Info|`Win32_SystemEnclosure`|**ChassisTypes**|
|Windows - Hardware &amp; Network Info|`Win32_SystemEnclosure`|**SerialNumber**|
|Windows - Network|`Win32_IP4RouteTable`|**Destination**|
|Windows - Network|`Win32_IP4RouteTable`|**Mask**|
|Windows - Network|`Win32_IP4RouteTable`|**NextHop**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**Caption**|
|Windows - Network|`Win32_NetworkAdapter`|**Index**|
|Windows - Network|`Win32_NetworkAdapter`|**Manufacturer**|
|Windows - Network|`Win32_NetworkAdapter`|**NetConnectionID**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**DefaultIPGateway**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**DHCPEnabled**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**Index**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**IPAddress**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**IPEnabled**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**IPSubnet**|
|Windows - Network|`Win32_NetworkAdapterConfiguration`|**MACAddress**|
|Windows - OS Information|`Win32_ComputerSystem`|**Manufacturer**|
|Windows - OS Information|`Win32_ComputerSystem`|**Model**|
|Windows - OS Information|`Win32_ComputerSystem`|**UserName**|
|Windows - OS Information|`Win32_OperatingSystem`|**CSDVersion**|
|Windows - OS Information|`Win32_OperatingSystem`|**Description**|
|Windows - OS Information|`Win32_OperatingSystem`|**Version**|
|Windows - OS Information|`Win32_Processor`|**AddressWidth**|
|Windows - Printers|`Win32_TCPIPPrinterPort`|**HostAddress**|
|Windows - Printers|`Win32_Printer`|**DeviceID**|
|Windows - Printers|`Win32_TCPIPPrinterPort`|**Name**|
|Windows - Printers|`Win32_Printer`|**Name**|
|Windows - Printers|`Win32_Printer`|**PortName**|
|Windows - Services|`Win32_Service`|**AcceptPause**|
|Windows - Services|`Win32_Service`|**AcceptStop**|
|Windows - Services|`Win32_Service`|**DesktopInteract**|
|Windows - Services|`Win32_Service`|**DisplayName**|
|Windows - Services|`Win32_Service`|**Name**|
|Windows - Services|`Win32_Service`|**PathName**|
|Windows - Services|`Win32_Service`|**ProcessId**|
|Windows - Services|`Win32_Service`|**ServiceType**|
|Windows - Services|`Win32_Service`|**StartMode**|
|Windows - Services|`Win32_Service`|**StartName**|
|Windows - Services|`Win32_Service`|**State**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Caption**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**DeviceID**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Index**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**InterfaceType**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Manufacturer**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Model**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**SCSIBus**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**SCSILogicalUnit**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**SCSIPort**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**SCSITargetId**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**SerialNumber**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Size**|
|Windows - Storage 2008 - WMI|`Win32_DiskDrive`|**Status**|
|Windows - Storage 2008 - WMI|`Win32_DiskPartition`|**DiskIndex**|
|Windows - Storage 2008 - WMI|`Win32_DiskPartition`|**Index**|
|Windows - Storage 2008 - WMI|`Win32_DiskPartition`|**Size**|
|Windows - Storage 2008 - WMI|`Win32_DiskPartition`|**StartingOffset**|
|Windows - Storage 2008 - WMI|`Win32_LogicalDisk`|**DeviceID**|
|Windows - Storage 2008 - WMI|`Win32_LogicalDisk`|**VolumeSerialNumber**|
|Windows - Storage 2008 - WMI|`Win32_LogicalDiskToPartition`|**Antecedent**|
|Windows - Storage 2008 - WMI|`Win32_LogicalDiskToPartition`|**Dependent**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**Description**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**DeviceID**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**DriveType**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**FileSystem**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**FreeSpace**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**ProviderName**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**Size**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**VolumeName**|
|Windows - Storage 2008 - WMI|`Win32_MappedLogicalDisk`|**VolumeSerialNumber**|
|Windows - Storage 2008 - WMI|`Win32_MountPoint`|**Directory**|
|Windows - Storage 2008 - WMI|`Win32_MountPoint`|**Volume**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**Capacity**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**DeviceID**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**DriveLetter**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**DriveType**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**FileSystem**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**FreeSpace**|
|Windows - Storage 2008 - WMI|`Win32_Volume`|**Label**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**AllocatedSize**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**BusType**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**FriendlyName**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**Manufacturer**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**Model**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**Number**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**ObjectId**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**OperationalStatus**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**SerialNumber**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Disk`|**Size**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_DiskToPartition`|**Disk**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_DiskToPartition`|**Partition**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_iSCSISession`|**InitiatorNodeAddress**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_iSCSISession`|**SessionIdentifier**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_iSCSISession`|**TargetNodeAddress**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_iSCSISessionToDisk`|**Disk**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_iSCSISessionToDisk`|**iSCSISession**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**AccessPaths**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**DiskId**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**ObjectId**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**Offset**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**OperationalStatus**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**PartitionNumber**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Partition`|**Size**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_PartitionToVolume`|**Partition**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_PartitionToVolume`|**Volume**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**DriveLetter**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**DriveType**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**FileSystem**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**FileSystemLabel**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**ObjectId**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**Size**|
|Windows - Storage 2012 - WMI|`root\microsoft\windows\storage\MSFT_Volume`|**SizeRemaining**|
|Windows - Storage 2012 - WMI|`Win32_DiskDrive`|**Name**|
|Windows - Storage 2012 - WMI|`Win32_DiskDrive`|**SCSIBus**|
|Windows - Storage 2012 - WMI|`Win32_DiskDrive`|**SCSILogicalUnit**|
|Windows - Storage 2012 - WMI|`Win32_DiskDrive`|**SCSIPort**|
|Windows - Storage 2012 - WMI|`Win32_DiskDrive`|**SCSITargetId**|
|Windows - Storage 2012 - WMI|`Win32_LogicalDisk`|**DeviceID**|
|Windows - Storage 2012 - WMI|`Win32_LogicalDisk`|**VolumeSerialNumber**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**Description**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**DeviceID**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**DriveType**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**FileSystem**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**FreeSpace**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**ProviderName**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**Size**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**VolumeName**|
|Windows - Storage 2012 - WMI|`Win32_MappedLogicalDisk`|**VolumeSerialNumber**|
|Windows - Storage 2012 - WMI|`Win32_MountPoint`|**Directory**|
|Windows - Storage 2012 - WMI|`Win32_MountPoint`|**Volume**|

## Windows Registry entries

Several Windows Registry entries are available for Discovery Windows probes.

**Note:** The Windows - Installed Software sensor appends a timestamp of 00:00:00 to the install\_date retrieved from the registry. The installation time of all Windows software is independent of the time zone and is set to midnight of the day it was installed. For example, an install date of **2.19.2017** in the Windows registry appears as **2.19.2017 00:00:00** in the CMDB.

|Probe|Windows Registry Entries|
|-----|------------------------|
|Windows - Active Connections Session|`HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/Tcpip/Parameters/Hostname`|
|Windows - Classify|`HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/Tcpip/Parameters/Hostname`|
|Windows - Classify|`HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Services/Tcpip/Parameters/Domain`|
|Windows - Get IIS Information|`HKEY_LOCAL_MACHINE/SOFTWARE/Microsoft/InetStp/MajorVersion`|
|Windows - Get IIS Information|`HKEY_LOCAL_MACHINE/SOFTWARE/Microsoft/InetStp/MinorVersion`|
|Windows - Find APD File Location|`HKEY_LOCAL_MACHINE/SOFTWARE/APD/APD/CONFIGPATH`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/InstallDate`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayVersion`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows NT/CurrentVersion/ProductId`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/ProductId`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/InstallDate`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/ParentDisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/DisplayVersion`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/UninstallString`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/Publisher`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Internet Explorer/Version`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/DisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/Publisher`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/ProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Office/*/Registration/*/ProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/ProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayVersion`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/DisplayVersion`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Office/*/Registration/*/DigitalProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/Publisher`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/DisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/UninstallString`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Office/*/Registration/*/DigitalProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Internet Explorer/Registration/ProductId`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/Publisher`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Internet Explorer/svcVersion`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Office/*/Registration/*/ProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/InstallDate`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/ParentDisplayName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/InstallDate`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows NT/CurrentVersion/DigitalProductID`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_*_KB*/InstallName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_*_KB*/InstallTimeHigh`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_*_KB*/InstallTimeLow`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_for_RollupFix*/InstallLocation`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_for_RollupFix*/InstallName`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_for_RollupFix*/InstallTimeHigh`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Component Based Servicing/Packages/Package_for_RollupFix*/InstallTimeLow`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Installer/UserData/*/Products/*/InstallProperties/InstallLocation`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Microsoft/Windows/CurrentVersion/Uninstall/*/InstallLocation`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/SOFTWARE/WOW6432Node/Microsoft/InetStp/SetupString`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/SOFTWARE/WOW6432Node/Microsoft/InetStp/VersionString`|
|Windows - Installed Software|`HKEY_LOCAL_MACHINE/Software/Wow6432Node/Microsoft/Windows/CurrentVersion/Uninstall/*/InstallLocation`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Adobe/Adobe Acrobat/DC/AVEntitlement/iEntitlementLevel`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayName`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Microsoft/Windows/CurrentVersion/Uninstall/*/DisplayVersion`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Microsoft/Windows/CurrentVersion/Uninstall/*/ParentDisplayName`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Microsoft/Windows/CurrentVersion/Uninstall/*/Publisher`|
|Windows - Installed Software|`HKEY_USERS/*/SOFTWARE/Microsoft/Windows/CurrentVersion/Uninstall/*/UninstallString`|

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

**Related topics**  


[Discovery commands for probes and patterns](../concept/discovery-command-probe-pattern.md)

