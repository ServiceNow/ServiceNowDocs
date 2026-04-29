---
title: Accessing the connection details of the Service Graph Connector Integration for Claroty CTD
description: You can access the connection details of the Service Graph Connector Integration for Claroty CTD in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.Access the details of a Claroty CTD connection configured for the Service Graph Connector Integration for Claroty CTD.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector Integration for Claroty CTD, Integrate, Operational Technology Manager, Operational Technology]
---

# Accessing the connection details of the Service Graph Connector Integration for Claroty CTD

You can access the connection details of the Service Graph Connector Integration for Claroty CTD in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.

With the CCF, you can access all the connections used by the Service Graph Connector Integration for Claroty CTD. The connection details include the connection alias, connection properties, data sources, and scheduled data imports associated with a connection. You can also test the connection. For more information, see [Accessing the connection details of Service Graph Connectors](https://www.servicenow.com/docs/access?context=integration-commons-conn-fw&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Service Graph Connector Integration for Claroty CTD](sgc-cmdb-integration-claroty-ctd.md)

## Access the details of a Claroty CTD connection

Access the details of a Claroty CTD connection configured for the Service Graph Connector Integration for Claroty CTD.

### Before you begin

Role required: admin

### About this task

There are application modules available to navigate to the data sources, system properties, and scheduled data imports for the Service Graph Connector Integration for Claroty CTD separately. However, the common connection framework \(CCF\) makes it possible to gather all the related data sources and scheduled data imports created for Claroty CTD in one place. You can also test the connection to the source \(Claroty CTD\) using the related links section.

### Procedure

1.  Ensure that the application scope is set to the **Service Graph Connector Integration for Claroty CTD** application by using the application picker.

2.  Navigate to **All** &gt; **Service Graph Connector for Claroty CTD** &gt; **Claroty CTD SGC Connection**.

3.  On the Service Graph Connections page, select **SG-OT Claroty CTD Default Connection**.

4.  To access the system properties, select the **Service Graph Connection Properties** tab.

5.  To access the data sources, select the **Service Graph Connection Data Sources** tab.

6.  To access the scheduled data imports, select the **Service Graph Connection Scheduled Data Imports** tab.

7.  To test your connection with the Claroty CTD platform, select the **Test Connection** related link.

    You can test your connection at any time. When the connection test is complete, you can find the status and suggestions for troubleshooting the failed steps under **Status** and **Suggestion** on the same page respectively.


