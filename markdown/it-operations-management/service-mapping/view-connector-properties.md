---
title: View CI connection attributes in an application service map in classic Service Mapping
description: You can view attributes of connections between configuration items \(CIs\).
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Application service analysis and maintenance using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View CI connection attributes in an application service map in classic Service Mapping

You can view attributes of connections between configuration items \(CIs\).

## Before you begin

Role required: service\_mapping\_admin or service\_mapping\_user

## About this task

You can view the following information for each connection:

-   The source and target CIs of this connection displayed in the Context \(right-click\) menu.
-   A complete list of all attributes collected about the connection in the Properties pane.

By default, Service Mapping merges connection lines for the same CI to declutter an application service map. It helps to make the map more readable.

![Merged connection lines](../image/MapAddOptionsMergeEdgesExample.png "Merged connection lines")

Each connection type has different attributes. For a merged connection line, all underlying connections are listed.

The way an service instance map displays connection attributes depends on the following factors:

-   [Views you configure for CIs](t_ConfigurePropertyDisplay.md) define which connection attributes appear in the Properties pane of the map.
-   Connection lines on the map depend on the [view you select for the map](modify-map-view.md).
-   Attributes available for viewing also depend on the Service Mapping setup, for more information see description of [components installed with Service Mapping](../reference/components-installed-with-service-mapping.md).

## Procedure

1.  Open the service instance map.

    1.  Navigate to **All** &gt; **CSDM** &gt; **Manage Technology Management Services** &gt; **Service Instance**.

    2.  Select the needed service instance.

    3.  On the service instance page, select **View Map**.

2.  View connection attributes as follows:

<table id="table_trf_3h2_jx"><thead><tr><th>

To view

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

The source and target CIs of a regular connection

</td><td>

Right-click the connection.![View the source and target CIs of a regular connection.](../image/ConnectorRightClick.png)

</td></tr><tr><td>

\(Available for application services discovered with Service Mapping\) The source and target CIs for a merged connection

</td><td>

-   Right-click the merged connection line with a number and select the relevant connection.

![View the source and target CIs of a merged connection.](../image/MergeConnectorRightClick.png)

Or

-   If a segment of a connection line is shared by more than one merged connections, there is no indication that it is a merged line.

Right-click the connection line coming out or going into a CI, and select the relevant connection.

![View the source and target CIs of a merged connection.](../image/MergedConnectorsSegmentsToFrom.png)

</td></tr><tr><td>

The source and target CIs for a connection if the spanning tree view is enabled. The spanning tree view simplifies an service instance map concealing most of the connection lines.

</td><td>

1.  Click the CI whose connections you want to view.

All concealed connections for this CI appear on the map.

2.  Right-click the relevant connection line.

![View the source and target CIs of a connection in the spanning tree view.](../image/ConnectorsSpanningTree.gif)

</td></tr><tr><td>

Detailed attributes of a regular connection in the **Properties** pane

</td><td>

Click the connection line.

</td></tr><tr><td>

\(Available for application services discovered with Service Mapping\) Detailed attributes of a merged connection in the **Properties** pane.

</td><td>

Click the merged connection line indicated by a number.

 All underlying connections are displayed separately in the **Properties** pane.

![View detailed attributes of a merged connection.](../image/MergeConnectorDetailedProperty.png)

</td></tr><tr><td>

Detailed attributes of a connection segment shared by more than one merged connection in the **Properties** pane.

</td><td>

Right-click the connection line coming out or going into a CI, select the relevant connection, and then choose **Select edge**.

![View detailed attributes of a connection segment shared by more than one merged connection.](../image/MergedConnectorsSegments.gif)

The detailed attributes are displayed in the **Properties** pane.

 **Note:** Shared segments do not have an indication that it is a merged line.

</td></tr><tr><td>

\(Available for application services discovered with Service Mapping\) Detailed properties of a connection in the **Properties** pane, when the spanning tree view is enabled.The spanning tree view simplifies an service instance map concealing most of the connection lines.

</td><td>

1.  Click the CI whose connections you want to see.

All concealed connections for this CI appear on the map.

2.  Click the required connection line.

![View detailed attributes of a connection if the spanning tree is enabled.](../image/SpanningTreeConnectorDetailedProperties.png)

</td></tr><tr><td>

\(Available for application services discovered with Service Mapping\) Traffic-based connections for a CI. **Note:** You can see traffic-based connections for a CI, even if you disabled the traffic-based discovery for an service instance the CI is part of.

</td><td>

1.  Right-click the CI whose traffic-based connections you want to check.
2.  Select **Show traffic based connections**.

The Traffic Based Connections List opens displaying the information in [Traffic Based Connections List table](view-connector-properties.md#table_cmh_vy5_f1b).

3.  Click **Close** when finished viewing this list.


</td></tr><tr><td>

Manually added connection.You can either add a connection or a CI manually. In both cases, the connection you manually add an entry point to the next tier of the application flow.

</td><td>

Click the manually added connection.

 The **Properties** pane shows Manual Endpoint under **Endpoint Type**.

 ![View manually added connection.](../image/MapManualCIConnectionProperty.png)

</td></tr></tbody>
</table><table id="table_cmh_vy5_f1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP

</td><td>

The IP address of the application connected to the selected CI.

</td></tr><tr><td>

Port

</td><td>

The port on the selected CI that is used to communicate to the other application.

</td></tr><tr><td>

Process

</td><td>

The ID of the process in the selected CI.

</td></tr><tr><td>

Already on map

</td><td>

-   **Yes** — if this connection shows on the map.
-   **No** — if this connection is not part of the service instance and not on the map.


</td></tr><tr><td>

System decision

</td><td>

The setting defines if Service Mapping keeps the discovered traffic-based connection or removes it. The value comes from the algorithm that Service Mapping uses.

</td></tr><tr><td>

User decision

</td><td>

\(Optional\) The setting overrides the System decision setting, which defines if Service Mapping keeps the discovered traffic-based connection or removes it. For example, if the System decision setting for a connection is Keep, and you want to remove this connection, select `Remove`.

</td></tr></tbody>
</table>
**Parent Topic:**[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

