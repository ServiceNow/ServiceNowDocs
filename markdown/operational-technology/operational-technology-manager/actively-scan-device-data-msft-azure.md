---
title: Import OT devices using the Standard mode of discovery
description: Use the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to import Operational Technology \(OT\) devices discovered through the Standard mode of discovery from Microsoft Defender for IoT.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(Azure\), Integrate, Operational Technology Manager, Operational Technology]
---

# Import OT devices using the Standard mode of discovery

Use the Service Graph Connector for Microsoft Defender for IoT \(Azure\) to import Operational Technology \(OT\) devices discovered through the Standard mode of discovery from Microsoft Defender for IoT.

## Before you begin

Role required: admin

## About this task

Standard mode uses an active search to discover additional information about the identified OT devices to supplement the existing device information. The devices identified during standard mode aren't associated with the passive sensor. To import these devices and assign them to a site, you can use the **Site Mappings** table. The table is populated using an automatic scheduled job. After the scheduled job is executed, the system populates the sites from the Source system in the table.

The **Site Mappings** table allows the admin to perform site mappings between the Microsoft Defender for IoT \(Azure\) site, where this data resides, and the ServiceNow ISA entity site \[cmdb\_ci\_ot\_isa\_entity\]. When the data is imported through the Service Graph Connector for Microsoft Defender for IoT \(Azure\), the devices are assigned to the correct site in the ISA entity site \[cmdb\_ci\_ot\_isa\_entity\].

## Procedure

1.  Navigate to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Site Mappings**.

2.  Select **New**.

3.  On the form, fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |ISA Entity Site|Site name for your ISA Entity site.|
    |Azure D4IoT Site|Site name for your Azure D4IoT site.|
    |Location|Location of the Azure D4IoT Site|
    |Approval group|Group that can approve requests related to the site.|
    |Azure D4IoT Site URL|
    |Assigned to|User that the site is assigned to.|
    |Change group|Group that is assigned change requests related to the site.|
    |Company|Company that runs the site.|
    |Managed by|User that manages the site.|
    |Managed by group|Group that manages the site.|
    |Owned by|User that owns the site.|
    |Support group|Group that is contacted when issues are encountered.|
    |Supported by|User that is contacted when issues are encountered.|
    |Network type|Network type of site. For example, **OT**.|
    |Correlation ID|Unique ID that identifies the correlation on the local system.|

4.  Select **Submit**.


## Result

Once the Site Mappings record is created and you perform the device import, devices are imported through the sensor and active scan. The devices are then assigned to an ISA entity \[cmdb\_ci\_ot\_isa\_entity\] site in ServiceNow.

**Note:** The metadata information from the site record, such as Assigned to and Owned by, are copied to the imported devices using the Service Graph Connector's system properties. For more information about the system properties for the Service Graph Connector for Microsoft Defender for IoT \(Azure\), see [Configure guided setup](configuring-sgc-microsoft-d4iot-azure.md).

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(Azure\)](../concept/integration-sgc-microsoft-defender-iot-azure.md)

