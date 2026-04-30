---
title: Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)
description: Integrate Microsoft Defender for IoT \(On-premises Management Console\) with the ServiceNow Operational Technology Manager application to automate import of sensor appliances, OT devices, and network connections.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate, Operational Technology Manager, Operational Technology]
---

# Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)

Integrate Microsoft Defender for IoT \(On-premises Management Console\) with the ServiceNow® Operational Technology Manager application to automate import of sensor appliances, OT devices, and network connections.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Microsoft Defender for IoT \(On-premises Management Console\) version: 10.5.2  or later

## Use cases

You can use the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) with the ServiceNow® Operational Technology Manager application to import sensor appliances, OT devices, and network connections.

## Guided setup

The guided setup for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure guided setup](../task/configuring-sgc-microsoft-d4iot-on-prem.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US#section_fxg_lh4_blb).

## Data mapping

Data from the Microsoft Defender for IoT \(On-premises Management Console\) data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete the setup, you can configure the integration to periodically pull data from the Microsoft Defender for IoT \(On-premises Management Console\) application.

The following table lists the data sources included for a Microsoft Defender for IoT \(On-premises Management Console\) project and the corresponding staging tables where the imported data is loaded.

|Data source|Staging table|
|-----------|-------------|
|SG-OT Microsoft D4IoT Connections Import|SG-OT Msft D4IoT Connections Import \[sn\_msftd4iotsgc\_sg\_ot\_msft\_d4iot\_connections\_import\]|
|SG-OT Microsoft D4IoT Devices Import|SG-OT Msft D4IoT Devices Import \[sn\_msftd4iotsgc\_sg\_ot\_msft\_d4iot\_devices\_import\]|
|SG-OT Microsoft D4IoT Sensors Import|SG-OT Msft D4IoT Sensors Import \[sn\_msftd4iotsgc\_sg\_ot\_msft\_d4iot\_sensors\_import\]|

The imported data from the staging tables is then inserted into the following target tables:

-   AIX Server \[cmdb\_ci\_aix\_server\]
-   Computer \[cmdb\_ci\_computer\]
-   Configuration Item \[cmdb\_ci\]
-   DCS \[cmdb\_ci\_ot\_dcs\]
-   ESX Server \[cmdb\_ci\_esx\_server\]
-   EWS \[cmdb\_ci\_ot\_ews\]
-   External System Metadata \[cmdb\_key\_value\_v2\]
-   Game Console \[cmdb\_ci\_game\_console\]
-   Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]
-   Historian \[cmdb\_ci\_ot\_historian\]
-   HMI \[cmdb\_ci\_ot\_hmi\]
-   HP-UX Server \[cmdb\_ci\_hpux\_server\]
-   HVAC Equipment \[cmdb\_ci\_hvac\]
-   HyperV Server \[cmdb\_ci\_hyper\_v\_server\]
-   IED \[cmdb\_ci\_ot\_ied\]
-   Industrial Actuator \[cmdb\_ci\_ot\_industrial\_actuator\]
-   Industrial Drive \[cmdb\_ci\_ot\_industrial\_drive\]
-   Industrial Robot \[cmdb\_ci\_ot\_industrial\_robot\]
-   Industrial Sensor \[cmdb\_ci\_ot\_industrial\_sensor\]
-   IoT Device \[cmdb\_ci\_iot\]
-   IP Address \[cmdb\_ci\_ip\_address\]
-   IP Camera \[cmdb\_ci\_ip\_camera\]
-   IP Firewall \[cmdb\_ci\_ip\_firewall\]
-   IP Phone \[cmdb\_ci\_ip\_phone\]
-   Linux Server \[cmdb\_ci\_linux\_server\]
-   Netgear \[cmdb\_ci\_netgear\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Network Intrusion Detection System \[cmdb\_ci\_nids\]
-   Operational Technology \(OT\) \[cmdb\_ci\_ot\]
-   OSX Server \[cmdb\_ci\_osx\_server\]
-   OT Control Module \[cmdb\_ci\_ot\_control\_module\]
-   OT Control System \[cmdb\_ci\_ot\_control\]
-   OT Device Details \[cmdb\_ot\_entity\]
-   OT Field Device \[cmdb\_ci\_ot\_field\_device\]
-   PLC \[cmdb\_ci\_ot\_plc\]
-   Printer \[cmdb\_ci\_printer\]
-   RTU \[cmdb\_ci\_ot\_rtu\]
-   Serial Number \[cmdb\_serial\_number\]
-   Server \[cmdb\_ci\_server\]
-   Server \[cmdb\_ci\_server\]
-   Solaris Server \[cmdb\_ci\_solaris\_server\]
-   Source \[sys\_object\_source\]
-   Unix Servercmdb\_ci\_unix\_server\]
-   Uninterruptible Power Supply \(UPS\) \[cmdb\_ci\_ups\]
-   Wireless Access Point \[cmdb\_ci\_wap\_network\]

For more information on where data is saved when pulling data from a Microsoft Defender for IoT \(On-premises Management Console\) project, see [CMDB classes targeted](../reference/sgc-microsoft-d4iot-on-prem-classes.md).

-   **[Configure the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)](../task/configuring-sgc-microsoft-d4iot-on-prem.md)**  
Use the Guided Setup for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\) to lead you through the integration steps.
-   **[CMDB classes targeted in the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)](../reference/sgc-microsoft-d4iot-on-prem-classes.md)**  
When you complete the guided setup, you can configure the integration to periodically pull data from a Microsoft Defender for IoT \(On-premises Management Console\) project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
-   **[Attribute mapping and classification for the Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)](../reference/attribute-mapping-sgc-msft-d4iot-on-prem.md)**  
The following tables describe the attribute mapping and classification for sensors and devices.

**Parent Topic:**[Operational Technology Manager Integrations](otm_integrations.md)

