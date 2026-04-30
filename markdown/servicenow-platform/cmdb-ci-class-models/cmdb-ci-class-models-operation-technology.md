---
title: Operational Technology \(OT\) extension classes
description: The CMDB CI Class Models store app adds or updates classes for Operational Technology \(OT\).
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 22
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Operational Technology \(OT\) extension classes

The CMDB CI Class Models store app adds or updates classes for Operational Technology \(OT\).

The CMDB CI Class Models app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Operational Technology \(OT\) data model

The Operational Technology \(OT\) data model was created to enable management of “OT Device” data. Operational Technology that controls industrial equipment can be based on IT class hardware \(computers, servers, network gear, and so on\), or on specific hardware profiles not included in the ServiceNow IT class model \(PLCs, HMIs, Engineering Workstations, Historians, and so on\). Therefore, a single OT Device in the OT data model includes two primary components:

1.  A CI class record. This can be an IT or an OT class CI.
2.  An OT Device details record. This describes the OT Device type \(function\) and other OT-specific attributes.

Each OT Device in the CMDB can be distinguished as having an “OT Device Details” reference \[cmdb\_ot\_entity reference field\] to a specific OT Device details \[cmdb\_ot\_entity table\] record. This is a bi-directional reference; the ot\_device reference on the cmdb\_ot\_entity table references the CI record. If the cmdb\_ot\_entity reference of a given CI record is **not** empty, the CI is considered to be an OT Device.

For example, an HMI \(Human Machine Interface\) OT Device could be composed in at least two different ways.

1.  A computer CI with an OT Device detail record describing its “OT Device type” as HMI.
2.  An HMI CI with an OT Device detail record describing its “OT Device type” also as HMI.

![OT Device records include a record in the cmdb_ot_entity table.](../image/ot-asset-ci-class.png)

In this way, a list of HMIs can be derived and a list of all computers in an enterprise can also be derived.

For more details on the OT data model, see [Implementing the CSDM framework for Operational Technology](https://www.servicenow.com/docs/access?context=ot-use-case-product-view&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US).

You can use the added classes as any other CMDB class. Applications such as Discovery for Operational Technology, and Service Graph Connector for Operational Technology \(Excel\) use these class extensions to populate CIs and discover various technologies and software. To learn more, see:

-   [Service Graph Connector for Microsoft Excel](https://www.servicenow.com/docs/access?context=service-graph-connector-for-OT-excel&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)
-   [IT Discovery for OT Networks](https://www.servicenow.com/docs/access?context=discovery-for-operational-technology&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)

**Note:** In Operational Technology, CIs used on an OT network to automate an industrial process are often referred to as  OT Devices. This term shouldn’t be confused with an Device record commonly used in the practice of Asset Management.

## Operational Technology \(OT\) schema structure​

![Relationships and references in Operational Technology schema.](../image/ClassOperationTechnology.png)

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. See the class columns table for further details about the columns added for each class. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

CMDB CI Class Models: Release 1.69.0 adds the following classes for Operational Technology \(OT\).

<table id="table_u4h_gdc_h2c"><thead><tr><th>

Class

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Firmware Installation \[cmdb\_firmware\_install\]

</td><td>

Firmware associated with the OT device.

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Additional information related to the OT device that's populated with the available OT integrations and captured as Key value pairs.

</td></tr><tr><td>

Software Instance \[cmdb\_sam\_sw\_install\]

</td><td>

Captures the software installed on the OT device if Software Asset Management isn't available. **Note:** If Software Asset Management is installed and entitled, the software installed data is available in the Software Installation related list.

</td></tr></tbody>
</table>CMDB CI Class Models: Release 1.59.0 adds the following classes for OT.

|Class|Extends|Description|
|-----|-------|-----------|
|OT System Service \[cmdb\_ci\_ot\_system\_service\]|cmdb\_ci\_ot\_system|Category of technology and systems that are used to manage, control, and monitor physical processes, machinery, and industrial operations.|

CMDB CI Class Models: Release 1.56.0 adds the following classes for OT.

|Class|Extends|Description|
|-----|-------|-----------|
|Quality Inspection Control System \[cmdb\_ci\_ot\_qics\]|cmdb\_ci\_ot\_control|Control systems that assist specifically in quality and inspection functions.|

CMDB CI Class Models: Release 1.30 adds the following classes for OT.

|Class|Extends|Description|
|-----|-------|-----------|
|CNC \[cmdb\_ci\_ot\_cnc\]|cmdb\_ci\_ot\_control|Computer Numerical Control, used for automated control of machining tools such as drills, lathes, mills, and for 3D printers.|
|DCS \[cmdb\_ci\_ot\_dcs\]|cmdb\_ci\_ot\_control|Distributed Control System. Achieves control using intelligence distributed about the controlled process, rather than by a centrally located single unit.|
|DPU \[cmdb\_ci\_ot\_dpu\]|cmdb\_ci\_ot\_control|Distributed Processing Units. ICS on a dedicated network, with each DPU handling thousands of points of I/O.|
|EWS \[cmdb\_ci\_ot\_ews\]|cmdb\_ci\_ot\_supervisory|Engineering Workstation. A computing platform for configuration, maintenance, and diagnostics of ICS applications and other control system equipment.|
|Historian \[cmdb\_ci\_ot\_historian\]|cmdb\_ci\_ot\_supervisory|Data Historian. A centralized database supporting data analysis for industrial processes.|
|HMI \[cmdb\_ci\_ot\_hmi\]|cmdb\_ci\_ot\_supervisory|Human-Machine Interface. Hardware or software through which an operator interacts with a controller.|
|IED \[cmdb\_ci\_ot\_ied\]|cmdb\_ci\_ot\_control|Intelligent Electronic Device. Receives or sends data/control from or to an external source for power grids.|
|Industrial Actuator \[cmdb\_ci\_ot\_industrial\_actuator\]|cmdb\_ci\_ot\_field\_device|Component of a machine that is responsible for moving and controlling a mechanism, such as opening a valve.|
|Industrial Drive \[cmdb\_ci\_ot\_industrial\_drive\]|cmdb\_ci\_ot\_field\_device|Equipment used to control the speed of machinery. It can be a mechanical electromechanical, hydraulic, or electronic device.|
|Industrial 3D Printer \[cmdb\_ci\_ot\_industrial\_3d\_printer\]|cmdb\_ci\_ot\_control|Device used in additive manufacturing for the construction of a three-dimensional object from a CAD model, or a digital 3D model.|
|Industrial Robot \[cmdb\_ci\_ot\_industrial\_robot\]|cmdb\_ci\_ot\_field\_device|Robotic system used for manufacturing.|
|Industrial Sensor \[cmdb\_ci\_ot\_industrial\_sensor\]|cmdb\_ci\_ot\_field\_device|Sensor device used to monitor the health of equipment|
|Network Gear \[cmdb\_ci\_netgear\]|cmdb\_ci\_hardware|Network gear is an electronic device which is required for communication and interaction between devices on a computer network.|
|Operations Technology \[cmdb\_ci\_ot\]|cmdb\_ci\_hardware|Base class for Operational Technology, used for industrial control. For instance, in manufacturing.|
|OPC Client \[cmdb\_ci\_ot\_opc\_client\]|cmdb\_ci\_ot\_supervisory|Software module that enables applications to acquire data from an OPC Server or conduct supervisory control using an OPC Server.|
|OPC Server \[cmdb\_ci\_ot\_opc\_server\]|cmdb\_ci\_ot\_control|Software module that enables applications to provide their data to the outside world using OPC.|
|OT Control Module \[cmdb\_ci\_ot\_control\_module\]|cmdb\_ci\_ot\_control|Module such as a PLC or DCS connected to an OT Control System.|
|OT Control System \[cmdb\_ci\_ot\_control\]|cmdb\_ci\_ot|Base Class for industrial control systems \(ICS\), usually at Purdue Model Level 1 or 2.|
|OT Supervisory System \[cmdb\_ci\_ot\_supervisory\]|cmdb\_ci\_ot|Base class for supervisory systems, usually at Purdue Model Level 2 or 3.|
|PLC \[cmdb\_ci\_ot\_plc\]|cmdb\_ci\_ot\_control|Programmable Logic Controller. Used to control OT Devices.|
|Protocol Converter \[cmdb\_ci\_protocol\_converter\]|cmdb\_ci\_hardware\_network\_gear|Device used to convert standard or proprietary protocol of one device to the protocol suitable for the other device or tools to achieve the interoperability.|
|RTU \[cmdb\_ci\_ot\_rtu\]|cmdb\_ci\_ot\_control|Remote Terminal Unit. Special purpose data acquisition and control unit designed to support DCS and SCADA remote stations|
|SCADA Client \[cmdb\_ci\_ot\_scada\_client\]|cmdb\_ci\_ot\_supervisory|Supervisory Control and Data Acquisition. Client that enables an operator to manage a SCADA server.|
|SCADA Server \[cmdb\_ci\_ot\_scada\_server\]|cmdb\_ci\_ot\_control|Supervisory Control and Data Acquisition. System capable of gathering and processing data and applying operational controls over long distance.|

## Class columns

CMDB CI Class Models: Release 1.30 adds the following columns to the respective classes.

|Added columns|Description|
|-------------|-----------|
|firmware\_version|​Firmware version reported by discovery source.|
|hardware\_version|​Hardware version reported by discovery source.|

|Added columns|Description|
|-------------|-----------|
|has\_module|​true/false value describing if the system has modules, such as chassis / blade architecture.|
|backplane\_name|System-reported string name or number for the backplane.|
|backplane\_id|System-reported unique ID for the backplane|

|Added columns|Description|
|-------------|-----------|
|slot\_number|Reported slot in the control system this module is using.|
|module\_type|Module type reported by the discovery source.|

|Added columns|Description|
|-------------|-----------|
|device\_type|List that describes if the device provides input, output, or both to the parent control system.|

|Added columns|Description|
|-------------|-----------|
|display\_name|Name of the OT system.|
|isa\_entity\_site|Site where the OT system is located.|

## Form view

All Operational Technology \(OT\) extension classes have a "Default view" form view that includes the OT Device Details attribute at the top of the form. The following table lists the other classes that have the **Operational Technology \(OT\)** view on their form context menu. This is the default form view for users with the cmdb\_ot\_viewer role for the following classes.

|Class|Description|
|-----|-----------|
|base hardware \[cmdb\_ci\_hardware\]|Base class for hardware.|
|base computer \[cmdb\_ci\_computer\]|An extension of the Hardware table, capturing computer properties.|
|base server \[cmdb\_ci\_server\]|Base class for all types of servers.|
|linux server \[cmdb\_ci\_linux\_server\]|Server running Linux software.|
|windows server \[cmdb\_ci\_win\_server\]|A server running Microsoft Windows Server operating system.|
|IoT Device base class \[cmdb\_ci\_iot\]|Parent table that contains Internet of Things device types.|
|IP Firewall and extended classes \[cmdb\_ci\_ip\_firewall\]|Contains all network firewalls.|
|IP Router \[cmdb\_ci\_ip\_router\]|Specialization of the Network Gear \[cmdb\_ci\_netgear\] table.|
|IP Switch \[cmdb\_ci\_ip\_switch\]|Specialization of the Network Gear \[cmdb\_ci\_netgear\] table.|
|Protocol Converter \[cmdb\_ci\_protocol\_converter\]|Device used to convert standard or proprietary protocol of one device to the protocol suitable for the other device or tools to achieve the interoperability.|

Classes not included in the table do not have the Operational Technology \(OT\) view by default. For any additional classes required, you can add the Operational Technology \(OT\) view to the form context menu. For more information about form context menu options, see [Form context menu](https://www.servicenow.com/docs/access?context=c_FormContextMenu&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Roles and Access Control Logic \(ACLs\)

The following roles are associated with the Operational Technology \(OT\) \[cmdb\_ci\_ot\] classes and associated tables that follow:

-   **Admin \(cmdb\_ot\_admin\)**

    Can create, read, update, and delete OT records. An admin can also edit the OT Device Type on the OT Device form, and manage specific configurations on the OT entity tables.

-   **Editor \(cmdb\_ot\_editor\)**

    Can create, read, update, and delete OT Device records.

-   **Viewer \(cmdb\_ot\_viewer\)**

    Can read OT Device records.


**Note:** For the cmdb\_ci\_ot and cmdb\_ot\_entity tables:

-   A user must have one of these three OT roles to view OT Devices.
-   IT users with an assigned itil role are restricted from viewing OT Devices in the cmdb\_ci\_ot table, and records in the cmdb\_ot\_entity table. IT users are still able to see IT asset classes, such as Computer, Installed Software.

OT customers may want to restrict access to OT Devices from users with an IT \(itil\) only role, for both a viewer and an admin role.

## Key relationship structures

Use the following key relationships as important guidelines when creating Operational Technology \(OT\) CIs:

**OT Entity**

Since any CI class may be found on an OT network, the OT Entity table \[cmdb\_ot\_entity\] captures additional attributes required in an OT Environment:

<table id="table_wmf_f32_s4b"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business criticality

</td><td>

Business criticality assigned in the discovery source.

</td></tr><tr><td>

OT Device

</td><td>

Reference to the CI that is on the OT network.

</td></tr><tr><td>

OT Device type

</td><td>

The function of the OT Device, regardless of CI class.-   For a dedicated HMI appliance, the CI is in the cmdb\_ci\_ot\_hmi class, and the OT Device type should be HMI.
-   For a computer performing the function of an HMI, the CI is in the cmdb\_ci\_computer class and the OT Device type should be HMI

</td></tr><tr><td>

Purdue level

</td><td>

Purdue level of the OT Device.

</td></tr><tr><td>

Zone

</td><td>

Zone assigned to the OT Device, usually used in the context of a zone/conduit model.

</td></tr><tr><td>

IRE criterion attribute \(ire\_criterion\)

</td><td>

Acts as a criterion attribute for an OT entity-related entry.

</td></tr></tbody>
</table>The OT Entity is a related list added to the Operational Technology \(OT\) \[cmdb\_ci\_ot\] table and extended tables. If you want to view OT entity metadata on an existing CI class, first add the related list to the form.

**OT Entity Type**

The OT Entity Type \[cmdb\_ot\_entity\_type\] table tracks the type of OT Device that an OT or non-OT CI is performing the function of. It serves as a necessary part of the Purdue level data model, and extends the Application File \[sys\_metadata\] table.

The ServiceNow AI Platform includes records representing common OT Device types of OT Device CIs. The OT Entity Type table attributes include:

|Attribute|Description|
|---------|-----------|
|Label|Display name of a specific OT Device type.|
|Name|Value used to identify a specific OT Device type.|
|OT table|Value used for auto-populating the Type field for the OT entity record \[cmdb\_ot\_entity\] of an OT Class CI.|
|Parent|Parent type of a specific type, which is a reference to a record in the same table \[cmdb\_ot\_entity\_type\].|

**OT Class Mapping Template**

The OT Class Mapping Template \[ot\_class\_mapping\_template\] table extends the Application File \[sys\_metadata\] and is used by OT Service Graph Connectors \(SGCs\) to classify a device into the correct CI class based on the source data.

Each SGC can extend the OT Class Mapping Template table and create a child class in the SGC application. Doing so defines the SGC-specific device classification details. For example, the Excel SGC Class Mapping \[excel\_sgc\_class\_mapping\] table is a child of the OT Class Mapping Template created in the Service Graph Connector for Microsoft Excel application scope, which stores the classification details specific for the Service Graph Connector for Microsoft Excel.

**Note:** The OT Class Mapping Template doesn't store any classification detail records. The child tables specific to each SGC store the classification records for an SGC to use.

The OT Class Mapping Template table attributes include:

<table id="table_chx_yvt_wdc"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Class

</td><td>

The class of the source CI.

</td></tr><tr><td>

Target CMDB class

</td><td>

The expected ServiceNow class that for the CI.

</td></tr><tr><td>

OT Device type

</td><td>

The category type that the OT Device is classified as. The Device type is also the function that the Device plays on the OT network. For example:An IT Device, such as a server, can be converted to an OT Device, and the function it plays on the network is an HMI. Therefore, its class is **server** and its Device type is **HMI**.

**Note:** In some cases, there are OT Devices with no OT function or OT Devices where the Device type is unknown. For OT Devices with no OT function, select **No OT Function**. For OT Devices where the Device type is unknown, select **Unknown**.

</td></tr><tr><td>

Allow OS classification

</td><td>

When set to **True**, if an operating system is found on the CI, the target is switched away from this table's target class to a ServiceNow class that matches its OS.For example, if Historian is the target class but Windows Server OS is found in the payload, the CI is classified as a Windows Server CI and its OT device type is set to Historian.

</td></tr><tr><td>

Active

</td><td>

When checked, the class mapping is set to **Active** and considered during device classification.

</td></tr></tbody>
</table>**Serial number**

During CI identification, the Identification and Reconciliation Engine \(IRE\) processes search for a serial number in two locations. One is the CI serial number attribute, and the other is the Serial Number \[cmdb\_serial\_number\] table, with reference back to the Operational Technology \(OT\) \[cmdb\_ci\_ot\] table.

-   It stores any serial number of any type other than system serial number, and only in the Serial Number table \(and not in the server CI attribute\).
-   If the system serial number is available, it stores it in both the Serial Number attribute of the CI and in the Serial Number table.
-   The Serial Number table is a many-to-one relationship, linking back to the Operational Technology \(OT\) CI. This table has a Type field for specifying the type of the serial number.
-   For Operational Technology \(OT\), use the string value **system** for the serial number type to ensure proper reconciliation across various sources.

**Network adapter**

Use the Network Adapter \[cmdb\_ci\_network\_adapter\] class to store network adapters.

1.  Set the MAC Address attribute to be the MAC address value.
    -   Format the string with colon separators between octets and lower case hexadecimal characters with padded zeros.
    -   For example, 'f8:f2:1e:00:d4:66'.
2.  Set the Name attribute in the Network Adapter class to be the same as the MAC Address.
3.  In the CI Relationship \[cmdb\_rel\_ci\] table, create an Owned By:Owns relationship to the associated Hardware CI.
4.  Using the CI with a reference to the associated Hardware CI, specify a reference from the Network Adapter \[cmdb\_ci\_network\_adapter\] table.

**IP Address**

Use the IP Address \[cmdb\_ci\_ip\_address\] class to store IP addresses.

1.  Store an IP address value in the IP Address attribute, and in the Name attribute to avoid empty Name attributes.
    -   Store an IPv4 IP address value using the format 'NNN.NNN.NNN.NNN', with decimal-based octets and period separators. Non-conforming values should be considered invalid and cleansed to null values.
    -   Store an IPv6 IP address value using lower case hexadecimal with colon separators. Non-confirming values should be considered invalid and cleansed to null values.
2.  Set the Netmask attribute to the IP address.
3.  Set the Name attribute in the Network Adapter class to be the same as the MAC Address.
4.  In the CI Relationship \[cmdb\_rel\_ci\] table, create an Owned By::Owns relationship to the associated Hardware CI.
5.  In the CI Relationship \[cmdb\_rel\_ci\] table, create an Owned By::Owns relationship to the associated Hardware CI.
6.  For the IP address, specify a reference to the Network Adapter \[cmdb\_ci\_network\_adapter\] table, using the Configuration Item with a reference to the associated Hardware CI.
7.  To ensure that base system identification rules work properly, also store the IP address in the associated Network Adapter class.

**Network adapter and IP address**

Use the IP Address \[cmdb\_ci\_ip\_address\] class to store IP addresses.

1.  Store the MAC address of the network adapter installed on a server, in the Network Adapter \[cmdb\_ci\_network\_adapter\] class.
2.  Store the IP address in the IP Address \[cmdb\_ci\_ip\_address\] class.

    **Note:** Do not store the MAC address or the IP address in the Operational Technology \(OT\) \[cmdb\_ci\_ot\] table. The default Operational Technology \(OT\) form is configured to display the IP address from the Network Adapter table.


**Backup Storage Information**

Use the Backup Storage Information \[cmdb\_backup\_storage\_information\] class to create backup records that identify the device in internal or external backup services. The Backup Storage Information table includes the following attributes:

|Attributes|Description|
|----------|-----------|
|Backup Configuration Status|Indicates whether the CI has been configured in the backup service or appliance with relevant policies.|
|Discovery Source|Discovery source of the backup record.|
|Backup Service|Reference to the Common Service Data Model Technical Service hosting external and internal backup system, services, or appliances|
|Managed By|Email ID of the user responsible for managing the backup.|
|Last Successful Backup|Date and time of the last successful backup made for a device.|
|Backup Source ID|Backup service record for a device, which identifies the device in external or internal backup services. Backup source id can include host\_id, vcenter\_id, instance\_id, db\_id.|
|Recovery Point Objective|Amount of time that can elapse between backups and the amount of data lost.|
|Execution Mode|Indicates whether the backup is configured to run automatically on a periodic basis, or if it is manually executed on an as-needed basis.|
|Last Backup Attempt|Date and time of the last backup attempt made for a device.|
|Backup Source|Details of the backed up CI. This table holds the backup status details for the referenced CI.|
|Managed By Group|Primary support group responsible for managing the backup.|
|Domain|ID of the domain to which the instance belongs.|

## Key reference structures

Use the following key references are important guidelines when creating Operational Technology \(OT\) records:

-   When creating computer or server records for OT Devices that are running on computers or servers, see the following topics:
    -   [Computer \[cmdb\_ci\_computer\] class](class-computer.md)
    -   [Server \[cmdb\_ci\_server\] class](class-server.md)
-   The Manufacturer and Model ID attributes are reference attributes to the Company \[core\_company\] and Product Model \[cmdb\_model\] tables respectively.
-   The Owned By, Assigned To, Managed By, and Supported By attributes are reference attributes to the User \[sys\_user\] table. The Change Group and Support Group attributes are reference attributes to the Group \[sys\_user\_group\] table.

## Identification rules

The ServiceNow AI Platform contains a predefined identification rule for the Operational Technology \(OT\) classes. That identification rule has the following key identifier entries, listed in priority order:

1.  Identifier entry that uses the identification specified in Serial Number \[cmdb\_serial\_number\] as the lookup table. The Serial Number table is a many-to-one reference from the serial number back to the server CI​.

    Optional conditions to filter the records during identification and reconciliation.

    **Note:** For lookup identification rules, you must complete the mandatory conditions under **Advanced Configuration**.

2.  Identifier entry that is specified in the Serial Number attribute in the CI.
3.  Identifier entry that is specified in the Mac Address attribute in the Network Adapter table.

    Optional conditions to filter the records during identification and reconciliation.

4.  Identifier entry for the Name attribute.
    -   If Serial Number and MAC Address are not available, then the Name \(which is usually the system reported hostname\) attribute is used.
    -   If both Serial Number and Name are not available, and only MAC Address is available, use MAC Address as the name of the CI. Using the MAC Address as the name of the CI ensures that you don't create an empty CI.
5.  Identifier entry that uses a product instance identifier \(PID\) on the CI.

**Note:** To learn more, see [CMDB Identification and Reconciliation \(IRE\)](c_CMDBIdentifyandReconcile.md).

**Reclassifying IT devices on your OT network**

Beginning with the Xanadu release, you can create a Network Adapter identifier on the OT identification rule to reclassify IT devices on your OT network. Creating a Network Adapter identifier on the OT identification rule overwrites the Hardware identification rule's Network Adapter identifier entry. To do this, complete the following actions:

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
2.  Under **Hardware** in the **CI Classes** menu, select the **Operational Technology \(OT\)** class.
3.  Under the **Class Info** menu, select **Identification Rule**.
4.  Under **Identifier Entries**, select **Add**.
5.  In the New Identifier Entry pop-up dialog box, choose **Use attributes from another table \(Lookup table\)** and select **Next**.
6.  In the Create Identifier Entry dialog box, complete the following steps:
    1.  Select **Hardware table** from **Search On Table** drop-down list.
    2.  Enter **400** in the **Priority** field.
    3.  Select **Network Adapter** from the **LookUP Table** from drop-down list.
    4.  Select **Mac Address** from the **Criterion Attributes** drop-down list.
    5.  Select **Save**.

**Note:** IT devices on an OT network are not reclassified automatically. If you want to automatically reclassify IT devices to OT, you must upgrade to Xanadu or the latest ServiceNow AI Platform version with the latest CMDB CI Class Models.

## Related entries

Related entries for OT identification rules allow OT Service Graph Connectors to create related records, such as OT Device records, backup records, and so on. The Operational Technology \[cmdb\_ci\_ot\] class rule contains the following related entries:

-   Backup Storage Information \[cmdb\_backup\_storage\_information\]
-   External system metadata \[cmdb\_key\_value\_v2\]
-   OT Device \[cmdb\_ot\_entity\]
-   Firmware Installation \[cmdb\_firmware\_install\]
-   Key Value \[cmdb\_key\_value\]
-   Software Instance \[cmdb\_software\_instance\]

The OT Control Module \[cmdb\_ci\_ot\_control\_module\] rule contains the following related entries:

-   Backup Storage Information \[cmdb\_backup\_storage\_information\]
-   OT Device \[cmdb\_ot\_entity\]
-   Firmware Installation \[cmdb\_firmware\_install\]
-   Key Value \[cmdb\_key\_value\]
-   Software Instance \[cmdb\_software\_instance\]

## OT Device Network Connection data model

The OT Device Network Connection data model leverages the OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table to identify source CIs and destination CIs. Identifying this data allows you to identify the device-to-device connections in your OT environment.

**Note:** The OT Device Network Connection table is available with the Industrial Core plugin. For more information about the Industrial Core plugin, see [Industrial Core plugin](https://www.servicenow.com/docs/access?context=industrial-core-plugin&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US).

The OT Device Network Connection \[sn\_ot\_device\_network\_connection\] table references the CI relationships \[cmdb\_rel\_ci\] table with the Connects to :: Connected by relationship type. The device-to-device connections in CI relationships and the metadata of how the source and destination communicate are stored.

**Note:** This data is populated with the available OT integrations and cannot be manually created.

The OT Device Network Connection table is populated using data from the following CMDB tables.

**Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]**

The following attributes in the Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|IP Address|ip\_address|
|Managed Network|managed\_network|
|Is Broadcast|is\_broadcast|
|Is Conflict|is\_conflict|
|Is DHCP|is\_dhcp|
|Is DNS|is\_dns|
|Is Managed|is\_managed|
|Is Reserved|is\_reserved|
|Name|name|

**IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]**

The following attributes in the IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\] table are populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Parent Pool|parent\_pool|
|CIDR|cidr|
|Managed Network|managed\_network|

**Managed Network \[cmdb\_ci\_managed\_network\]**

The following attribute in the Managed Network \[cmdb\_ci\_managed\_network\] table is populated by collected data:

|Attribute label|Attribute name|
|---------------|--------------|
|Name|name|
|Contained by CI|contained\_by\_ci|

The OT Device Network Connection table also uses the following Identification Reconciliation Engine \(IRE\) rule. The IRE rule on the OT Device Network Connection table can help Service Graph Connectors align with a standardized way to create connection records.

-   Identifier name: OT Device Network Connection
-   Applies to: sn\_ot\_device\_network\_connection
-   Independent: true
-   Identifier entries:
    -   Source IP Address
    -   Destination IP Address
    -   Destination Port
    -   Source Managed Network
    -   Destination Managed Network

## Deprecated classes

CMDB CI Class Models: Release 1.30 soft deprecated \(not removed, but marked as follows\) with the release of the OT class model:

|Class|Description|
|-----|-----------|
|Human Machine Interface \[cmdb\_ci\_hmi\]|OT Devices moved to cmdb\_ci\_ot to support broader use cases. Use cmdb\_ci\_ot\_hmi instead.|
|Manufacturing Device \[cmdb\_ci\_manufacturing\]|OT Devices moved to cmdb\_ci\_ot to support broader use cases. Use cmdb\_ci\_ot as the base class or other generic child classes as appropriate.|
|Programmable Logic Controller \[cmdb\_ci\_plc\]|OT Devices moved to cmdb\_ci\_ot to support broader use cases. Use cmdb\_ci\_ot\_plc instead.|

A script has been provided to migrate records from these classes to the new class tables. The admin role is required to perform the following tasks:

1.  Navigate to **System Definition** &gt; **Script Includes**
2.  Find the record named **OTDevicesMigrationUtils**.
3.  Navigate to **Definition** &gt; **Script Includes** &gt; **.**
4.  In the background window, copy and paste the provided script.
5.  Select the appropriate scope and run the script.

## Troubleshooting

The following are some troubleshooting tips:

|Problem|Suggested resolution|
|-------|--------------------|
|Unable to see OT Device menu items|Ensure that the logged in user has been assigned the appropriate roles. To learn more, see the preceding Roles section.|
|Error creating or updating an OT Device record|Allow only one OT Device record \(cmdb\_ot\_entity\) per CI.|

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

The [CMDB CI Class Models](cmdb-ci-class-models.md) adds class models that extend the CMDB class hierarchy, including:

-   Class descriptions
-   Identification rules
-   Identifier entries
-   Dependent relationships, if applicable.

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

