---
title: Inflow and outflow analysis: node star diagram
description: View the process graph as a node star diagram in the Process Map component on dashboards. The node star diagram explicitly displays the activities that are coming into the selected node and the activities that are going out of the selected node.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Process Mining, Platform Analytics]
---

# Inflow and outflow analysis: node star diagram

View the process graph as a node star diagram in the Process Map component on dashboards. The node star diagram explicitly displays the activities that are coming into the selected node and the activities that are going out of the selected node.

When you view a process graph in the Process Map component on dashboards, and want to know the details of one node in the graph, you must use the node star diagram.

To know more about configuring a Process Mining map to view the process graph in the PAR dashboard, see [Configure Process Mining map in PAR dashboard](../task/config-dashboard.md). For more information about Platform Analytics \(PAR\) dashboards, see [Exploring Platform Analytics dashboards](../../../use/dashboards/reference/ac-elements.md).

The following process graph displays details about the reassignment analysis.

![Process graph](../image/process-graph.png)

Select any node of the process graph and the graph changes to the node star diagram displaying all the incoming and outgoing arcs from the selected node. When you select the **Process graph** button again, the entire graph is displayed as a process graph. You can also apply a view based on the activity definitions for the project. Multi-dimensional maps are supported on the Platform Analytics dashboards. You can also run work notes analysis from Platform Analytics dashboards. For more information about work notes analysis, see [Working with work notes using Now Assist](worknotes.md).

If you select PO Group 10, a node star diagram similar to the following figure is displayed. You can view the records assigned to PO Group 10. You can also view the records that are assigned from PO Group 10 to other groups.

![Star node diagram](../image/summary-insights-dashboard2.png)

You can filter either by the outgoing or incoming records.

![star node diagram filter](../image/process-graph-filter.png)

If you filter by **Incoming**, all the records that are assigned to PO Group 10 are displayed. If you’re the manager for PO group 10, you can see which groups are assigning how many records to your group. You may then focus on fixing any issues that you see.

![Incoming records](../image/process-graph-incoming.png)

If you filter by **Outgoing**, all the records that are assigned by PO Group 10 to other groups are displayed. If you’re the manager for PO group 10, you can see how many records have been reassigned from PO Group 10 to which groups. You may then focus on fixing any issues that you see.

![Outgoing records](../image/process-graph-outgoing.png)

You can filter on transitions too. Select any arc, a window is displayed with the details of the transition.

If you select PO Group 60, you see a window similar to the following.

![Filter on transition](../image/node-transition.png)

Select **Filter on transition**. The node star diagram displays results only for that one transition. As the image shows that PO Group 60 assigned records to PO Group 10. PO Group 10 then assigned the records to PO Group 16. PO Group 16 then assigned the records to PO Group 10. Finally, the records were closed.

![Filter on transition result](../image/node-transition-filter.png)

Select any node or arc, the **Show records** button is displayed. Select the **Show records** button. A scheduled task starts. After the scheduled task is complete, select **View result** in the Scheduled Tasks pane.

**Parent Topic:**[Using Process Mining](use-process-mining.md)

