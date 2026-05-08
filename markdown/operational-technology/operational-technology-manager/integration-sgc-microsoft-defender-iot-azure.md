---
title: Service Graph Connector for Microsoft Defender for IoT \(Azure\)
description: Integrate Microsoft Defender for IoT with the ServiceNow Operational Technology Manager application to automate import of OT devices and sensor appliances.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Integrate, Operational Technology Manager, Operational Technology]
---

# Service Graph Connector for Microsoft Defender for IoT \(Azure\)

Integrate Microsoft Defender for IoT with the ServiceNow® Operational Technology Manager application to automate import of OT devices and sensor appliances.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Supported versions

Supports Microsoft Defender for IoT sensor versions:

-   22.2.3.22
-   22.2.5.9

## Use cases

You can use the Service Graph Connector for Microsoft Defender for IoT \(Azure\) with the ServiceNow® Operational Technology Manager application to import OT devices and sensor appliances.

## Guided setup

The guided setup for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) provides an organized sequence of tasks to configure the integration on your instance. To access the guided setup, see [Configure guided setup](../task/configuring-sgc-microsoft-d4iot-azure.md).

## CMDB integrations dashboard

The Integration Commons for CMDB store app provides a dashboard with a central view of the status, processing results, and processing errors of all installed integrations. You can see metrics for all integration runs. You can filter the view to a specific CMDB integration, a specific time duration, or a specific integration run. For more details about monitoring integrations in the CMDB Integrations Dashboard, see Integration Commons for CMDB.

## Data mapping

Data from the Microsoft Defender for IoT \(Azure\) data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete the setup, you can configure the integration to periodically pull data from the Microsoft Defender for IoT \(Azure\) application.

The following table lists the data sources included for a Microsoft Defender for IoT \(Azure\) project and the corresponding staging tables where the imported data is loaded.

|Data source|Staging table|
|-----------|-------------|
|SG-OT Azure D4IoT Devices Import|SG-OT Azure D4IoT Devices Import \[sn\_msftd4iotazsgc\_sg\_ot\_azure\_d4iot\_devices\_import\]|
|SG-OT Azure D4IoT Sensors Import|SG-OT Msft D4IoT Sensors Import \[sn\_msftd4iotazsgc\_sg\_ot\_azure\_d4iot\_sensors\_import\]|

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

For more information on where data is saved when pulling data from a Microsoft Defender for IoT \(Azure\) project, see [CMDB classes targeted](../reference/sgc-microsoft-d4iot-azure-classes.md).

-   **[Configure the Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../task/configuring-sgc-microsoft-d4iot-azure.md)**  
Use the guided setup for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to lead you through the integration steps.
-   **[Validate NIDS sensors](../task/validate-nids-appliances-sgc-msft-d4iot-azure.md)**  
Validate the Network IDS \(NIDS\) sensors once they're imported to prepare for the device import. Sensors only pass the validation if they aren't in learning mode as such sensors are not eligible for device import.
-   **[Accessing the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\)](sgc-cmdb-msft-d4iot-azure.md#)**  
You can access the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\) in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.
-   **[Import OT devices using the Standard mode of discovery](../task/actively-scan-device-data-msft-azure.md)**  
Use the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to import Operational Technology \(OT\) devices discovered through the Standard mode of discovery from Microsoft Defender for IoT.
-   **[CMDB classes targeted in the Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../reference/sgc-microsoft-d4iot-azure-classes.md)**  
When you complete the guided setup, you can configure the integration to periodically pull data from a Service Graph Connector for Microsoft Defender for IoT \(Azure\) \(Azure\) project. The data is saved in tables that extend from the Configuration item \[cmdb\_ci\] table.
-   **[Attribute mapping and classification for Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../reference/attribute-mapping-sgc-msft-d4iot-azure.md)**  
The following tables describe the attribute mapping and classification for sensors and devices.

**Parent Topic:**[Operational Technology Manager Integrations](otm_integrations.md)

