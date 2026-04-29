---
title: Viewing connections for a Service Graph Connector in SGC Central
description: You can view installed and draft connections that were added using Service Graph Connectors within the SGC Central view of the Service Graph Workspace or CMDB Workspace.View the details of an installed connection that was added using a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.View the details and resume setting up draft connections.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing connections, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing connections for a Service Graph Connector in SGC Central

You can view installed and draft connections that were added using Service Graph Connectors within the SGC Central view of the Service Graph Workspace or CMDB Workspace.

The following connection types are available for viewing:

-   Installed connection \(see [View an installed connection in SGC Central](sgcc-viewing-installed-connection.md#).\)
-   Draft connection \(see [View a draft connection in SGC Central](sgcc-viewing-installed-connection.md#).\)

## View an installed connection in SGC Central

View the details of an installed connection that was added using a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.

### Before you begin

Role required: SGC-admin or admin

### Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  Select **All connections**.

3.  Select the **Installed** tab.

4.  Review the list of installed connections.

5.  Select a connection from the **Connection** column to view the details, data sources, import schedules, and errors associated with the connection.

    **Note:** When you select a connection, the application scope changes to the selected connector type.


## View a draft connection in SGC Central

View the details and resume setting up draft connections.

### Before you begin

Role required: SGC-admin or admin

### Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  Select **All connections**.

3.  Select the **Drafts** tab.

4.  Review the list of draft connections.

5.  Complete setting up the draft connections.

    -   Select **Configure** to continue where a Service Graph Connector was last configured within SGC Central.
    -   Select **Resume setup** to set up a single instance connector for the first time.
    **Note:** When you select a connection, the application scope changes to the selected connector type.


