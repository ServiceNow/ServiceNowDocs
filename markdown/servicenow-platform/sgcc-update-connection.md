---
title: Update a connection for a Service Graph Connector in SGC Central
description: Update a connection configured for a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 1
breadcrumb: [Managing connections, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Update a connection for a Service Graph Connector in SGC Central

Update a connection configured for a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.

## Before you begin

Role required: SGC-admin or admin

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../../configuration-management/image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  Select **All connections**.

3.  Select the **Installed** tab.

4.  Select a connection from the **Connection** column.

    **Note:** When you select a connection, the application scope changes to the selected connector type.

5.  On the **Details** tab, review and modify the details for a connection.

6.  Select **Update and test connection**.

7.  Select a tab to view further details of the connection, such as data sources, import schedules, and any errors.

    Additional tabs might appear depending on the connector type.


## What to do next

If there are any errors and the Service Graph Connector diagnosis skill is enabled, you can diagnose the error using Now Assist. To learn more, see [Diagnose a processing error in SGC Central](sgcc-diagnose-proc-errors.md);

