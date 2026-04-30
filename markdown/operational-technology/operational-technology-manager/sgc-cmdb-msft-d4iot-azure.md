---
title: Accessing the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\)
description: You can access the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\) in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.Access the details of a Microsoft Defender for IoT \(Azure\) connection configured for the Service Graph Connector Integration for Claroty CTD.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2025-04-07"
reading_time_minutes: 2
breadcrumb: [Service Graph Connector for Microsoft Defender for IoT \(Azure\), Integrate, Operational Technology Manager, Operational Technology]
---

# Accessing the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\)

You can access the connection details of the Service Graph Connector for Microsoft Defender for IoT \(Azure\) in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.

With the CCF, you can access all the connections used by the Service Graph Connector for Microsoft Defender for IoT \(Azure\). The connection details include the connection alias, connection properties, data sources, and scheduled data imports associated with a connection. You can also test the connection. For more information, see [Accessing the connection details of Service Graph Connectors](https://www.servicenow.com/docs/access?context=integration-commons-conn-fw&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Service Graph Connector for Microsoft Defender for IoT \(Azure\)](integration-sgc-microsoft-defender-iot-azure.md)

## Access the details of a Microsoft Defender for IoT \(Azure\) connection

Access the details of a Microsoft Defender for IoT \(Azure\) connection configured for the Service Graph Connector Integration for Claroty CTD.

### Before you begin

Role required: admin

### About this task

There are application modules available to navigate to the data sources, system properties, and scheduled data imports for the Service Graph Connector for Microsoft Defender for IoT \(Azure\) separately. However, the common connection framework \(CCF\) makes it possible to gather all the related data sources and scheduled data imports created for Microsoft Defender for IoT \(Azure\) in one place. You can also test the connection to the source \(Microsoft Defender for IoT \(Azure\)\) using the related links section.

### Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Microsoft Defender for IoT \(Azure\) application by using the application picker.

2.  Navigate to **All** &gt; **Service Graph for MSFT D4IoT \(Azure\)** &gt; **Azure SGC Connection**.

3.  On the Service Graph Connections page, select **SG-OT Azure SGC Default Connection** record.

4.  To access the system properties, select the **Service Graph Connection Properties** tab.

5.  To access the data sources, select the **Service Graph Connection Data Sources** tab.

6.  To access the scheduled data imports, select the **Service Graph Connection Scheduled Data Imports** tab.

7.  To test your connection with the Microsoft Azure platform, select the **Test Connection** related link.

    You can test your connection at any time. When the connection test is complete, you can find the status and suggestions for troubleshooting the failed steps under **Status** and **Suggestion** on the same page respectively.


