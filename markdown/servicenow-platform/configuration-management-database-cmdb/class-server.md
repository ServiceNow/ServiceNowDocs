---
title: Server \[cmdb\_ci\_server\] class
description: Attributes, identification rule, and other important schema structures for the CMDB Server \[cmdb\_ci\_server\] class.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Server \[cmdb\_ci\_server\] class

Attributes, identification rule, and other important schema structures for the CMDB Server \[cmdb\_ci\_server\] class.

For descriptions of common CMDB tables in a base system, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

![Relationships and references between the Hardware, Computer, and Server classes.](../image/schema-hw-computer-server.png "Hardware, Computer, Server Schema")

**Note:** cmdb\_sw\_instance noted in the diagram, is a reference to the cmdb\_software\_instance class, and Supported\_Group is a reference to Support\_Group.

## Attributes

The Server class adds the following unique attributes:

|Attribute|Description|
|---------|-----------|
|Classification​|Type of server, such as production, development, disaster recovery, or user acceptance testing \(UAT\).|
|Firewall status|Internet or intranet facing server.|
|Host name|Use the Name attribute to store the host name of the server instead of the Host name attribute.|
|Used for|Business service supported by the server, such as production, staging, or quality assurance \(QA\). This attribute uses the **Used for** choice list field from the Service \[cmdb\_ci\_service\] table.|

|Reference attribute|Reference to|
|-------------------|------------|
|Disaster backup|Server \[cmdb\_ci\_server\] table. Reference to another server that is the backup server for this server.|

## Reference classes

The following reference classes extend the Server class. They do not add any new attributes.

|Reference class​|Name​|Description​|
|----------------|-----|------------|
|cmdb\_ci\_solaris\_server​|Solaris Server​|Server running Oracle Solaris operating system​.|
|cmdb\_ci\_lb\_cisco\_csm​|Cisco CSM​|Cisco Security Manager \(CSM\) load balancer​.|
|cmdb\_ci\_win\_server​|Windows Server​|Server running Microsoft Windows Server operating system​.|
|cmdb\_ci\_lb\_ace​|ACE​|Cisco Application Control Engine load balancer.​|
|cmdb\_ci\_lb\_netsclaer​|Citrix Netscaler​|Citrix Netscaler​ load balancer.|
|cmdb\_ci\_lb\_alteon​|Alteon​|Alteon load balancer.​|
|cmdb\_ci\_lb​|Load Balancer​|Generic load balancer​.|
|cmdb\_ci\_lb\_a10​|A10 Load Balancer​|A10 load balancer.​|
|cmdb\_ci\_lb\_cisco\_css​|Cisco CSS​|Cisco Content Services Switch \(CSS\) load balancer.​|
|cmdb\_ci\_lb\_cisco\_gss​|Cisco GSS​|Cisco Global Site Selector \(GSS\) load balancer.​|
|cmdb\_ci\_osx\_Server​|OS/X Server​|Server running OS/X operating system​.|
|cmdb\_ci\_HPUX\_Server​|HPUX Server​|Server running HP-UX operating system​.|
|cmdb\_ci\_tape\_server​|Server Tape Unit​|Server using a tape drive​.|
|cmdb\_ci\_Server\_Hardware​|Server Hardware​|Server hardware.​|
|cmdb\_ci\_datapower\_server|Data Power Hosting Server​|IBM DataPower hosting server​.|
|cmdb\_ci\_net\_app\_server​|Network Appliance Hardware​|NetApp hardware​.|
|cmdb\_ci\_netware\_server​|Netware Server​|Server running NetWare operating system​.|
|cmdb\_ci\_ibm\_zos\_server​|IBM zOS Server​|Server running IBM z/OS operating system​.|
|cmdb\_ci\_storage\_node\_element​|Storage Node Element​|Storage node.​|
|cmdb\_ci\_chassis\_server​|Server Chassis​|Server chassis​.|
|cmdb\_ci\_lb\_network​|Network Load Balancer​|Network load balancer hardware​.|
|cmdb\_ci\_Unix\_Server​|Unix Server​|Server running Unix operating system.​|
|cmdb\_ci\_linux\_server|Linux Server|Server running Linux operating system.​|
|cmdb\_ci\_virtualization\_server​|Virtualization Server​|Abstract base table used by Hyper-V Server \[cmdb\_ci\_hyper\_v\_server\] and ESX Server \[cmdb\_ci\_esx\_server\].|
|cmdb\_ci\_mainframe​|IBM Mainframe​|Large-scale computer system with high-end capabilities.​|

## Schema description

The CMDB schema model does not separate between servers and computers that are physical and servers and computer that are virtual. Instead, ​the Computer and the Server classes have a field named **IsVirtual**. If a computer or server is a virtual instance, set this **IsVirtual** attribute to **true**.

As described in the Virtual Machine schema section, to fully model a virtual machine, set the **IsVirtual** attribute in the Computer or Server CI to **true**. Create a Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] record using the **BIOS UUID** attribute as the key identifier. Then create a Hosted\_On relationship between the Virtual Machine Instance record and the Computer or Server instance and set **IsVirtual** to **true**.

## Key relationship structures

Use the following key relationships as important guidelines when creating Hardware, Computer, or Server CIs:

-   Serial number: During CI identification, Identification and Reconciliation Engine \(IRE\) processes search for a serial number in two locations. One is the CI serial number attribute, and the second one is the Serial Number \[cmdb\_serial\_number\] table, with reference back to the Hardware \[cmdb\_ci\_hardware\] table.

    -   Store any serial number of any type other than System, only in the Serial Number table \(and not in the server CI attribute\).​
    -   If the system serial number is available, store it in both the **Serial Number** attribute of the CI and in the Serial Number table.
    The Serial Number table is a many to one relationship linking back to the server CI. This table has a type field for specifying the type of the serial number \(system, uuid, chassis, bios, or baseboard\) and storing the actual value itself. Use the following Windows standards for serial number types in the Serial Number \[cmdb\_serial\_number\] table:

    -   **system**: Product identification such as a serial number for software, a die number on a hardware chip, or a project number \(for noncommercial products\).
    -   **uuid**: Universally unique identifier \(UUID\) for the product. A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.
    -   **chassis**: Manufacturer-allocated number that is used to identify a physical element. Value is the Serial Number member of the System Enclosure or Chassis structure in the SMBIOS information. This type represents the properties associated with a physical system enclosure.
    -   **bios**: The assigned serial number of the BIOS. This type represents the attributes of the computer system basic input/output services \(BIOS\) that are installed on the computer.
    -   **baseboard**: Manufacturer-allocated number that is used to identify the physical element. This property is inherited from CIM\_PhysicalElement, and is sometimes referred to as the 'Motherboard Serial Number'.
-   Network adapter:

    -   Use the Network Adapter \[cmdb\_ci\_network\_adapter\] class to store network adapters.
    -   Set the **Name** attribute in the Network Adapter class to be the name of the Network Adapter device \(such as eth0, eth1\).
    -   Set the **MAC Address** attribute to be the MAC address value. Format the string with colon separators between octets and lower case hexadecimal characters with padded zeros.

        For example: 'f8:f2:1e:00:d4:66'.

    -   In the CI Relationship \[cmdb\_rel\_ci\] table, create an **Owned By::Owns** relationship to the associated Hardware CI. Specify a reference from the Network Adapter \[cmdb\_ci\_network\_adapter\] table using the CI with a reference to the associated Hardware CI.
-   IP address:

    -   Use the IP Address \[cmdb\_ci\_ip\_address\] class to store IP addresses.
    -   Store an IP address value in the **IP Address** attribute, and in the **Name** attribute \(to avoid empty **Name** attributes\).
    -   Store an IPv4 IP address value using the format 'NNN.NNN.NNN.NNN', with decimal-based octets and period separators. Non-conforming values should be considered invalid and cleansed to null values.
    -   Store an IPv6 IP address value using lower case hexadecimal with colon separators. Non-confirming values should be considered invalid and cleansed to null values.
    -   Set the **Netmask** attribute to the IP address.
    -   In the CI Relationship \[cmdb\_rel\_ci\] table, create an **Owned By::Owns** relationship to the associated Hardware CI.
    -   Specify for the IP address a reference to the Network Adapter \[cmdb\_ci\_network\_adapter\] table using the Configuration Item with a reference to the associated Hardware CI.
    -   To ensure that base system identification rules work properly, also store the IP address in the associated Network Adapter class.
-   Network adapter and IP address:

    -   Store the MAC address of the network adapter installed on a server, in the Network Adapter \[cmdb\_ci\_network\_adapter\] class.
    -   Store the IP address in the IP Address \[cmdb\_ci\_ip\_address\] class.
    -   Do not store the MAC address or the IP address in the Server \[cmdb\_ci\_server\] class.​

## Key reference structures

Use the following key references as important guidelines when creating Hardware, Computer, or Server CIs:

-   Software and processes running on a server: The Software \[cmdb\_ci\_spkg\] class contains the generic software package that is related to the server CI. The cmdb\_software\_instance table instantiates each instance of the software package with:

    -   One to one reference back to the Server \[cmdb\_ci\_server\] class
    -   Many to one reference back to the Software class
    These references are stored in the **Installed on** and the **Product Name** reference attributes respectively.

    If either the Software Asset Management Foundation \[com.snc.sams\] or the Software Asset Management \[com.snc.software\_asset\_management\] plugin is installed, then store software details in the Software Installation \[cmdb\_sam\_sw\_install\] table instead of the cmdb\_software\_instance table.

-   The **Manufacturer** and **Model ID** are reference attributes to the Company \[core\_company\] and Product Model \[cmdb\_model\] tables respectively.
-   The **Owned By**, **Assigned To**, **Managed By**, and **Supported By** are reference attributes to the User \[sys\_user\] table. The **Change Group** and **Support Group** are reference attributes to the Group \[sys\_user\_group\] table.

## Identification rule

The base system contains pre-defined identification rules for the Hardware, Computer, and Server classes, which are identical. That identification rule has the following key identifier entries, listed in priority order:

1.  Identifier entry which uses lookup-based identification specified with Serial Number \[cmdb\_serial\_number\] as the lookup table. The Serial Number table is a many to one reference from Serial Number back to the server CI​.
2.  Identifier entry specified with the **Serial Number** attribute in the CI.
3.  Identifier entry for the **Name** attribute. If **Serial Number** is not available, then the **Name** \(which is the hostname\) attribute is used. If both the **Serial Number** and the **Name** attributes are provided, then Identification and Reconciliation Engine \(IRE\) looks first for the Serial Number. Then, if a Serial Number is not found, IRE falls back to using Name.
4.  Identifier entry specified for the **MAC Address**/**IP Address** attributes in the Network Adapter table. However, do not rely only on the **MAC Address**/**IP Address**.

    If both **Serial Number** and **Name** are not available, and only **MAC Address**/**IP Address** are available, use **MAC Address** as the name of the CI. Using the **MAC Address** as the name of the CI ensures that you don't create an empty CI.


For more information, see [CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md).

