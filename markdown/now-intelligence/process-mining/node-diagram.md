---
title: Inflow and outflow analysis: node star diagram
description: View the process graph as a node star diagram. The node star diagram explicitly displays the activities that are coming into the selected node and the activities that are going out of the selected node.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/now-intelligence/process-mining/node-diagram.html
release: yokohama
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Process Mining, Process Mining, Platform Analytics]
---

# Inflow and outflow analysis: node star diagram

View the process graph as a node star diagram. The node star diagram explicitly displays the activities that are coming into the selected node and the activities that are going out of the selected node.

When you view a process graph, and want to know the details of one node in the graph, you must use the node star diagram.

The following process graph displays details about the reassignment analysis.

\[Omitted image "process-graph.png"\] Alt text: Process graph

Select any node of the process graph and the graph changes to the node star diagram displaying all the incoming and outgoing arcs from the selected node. When you select the **Process graph** button again, the entire graph is displayed as a process graph.

If you select PO Group 10, a node star diagram similar to the following figure is displayed. You can view the records assigned to PO Group 10. You can also view the records that are assigned from PO Group 10 to other groups.

\[Omitted image "summary-insights-dashboard2.png"\] Alt text: Star node diagram

You can filter either by the outgoing or incoming records.

\[Omitted image "process-graph-filter.png"\] Alt text: star node diagram filter

If you filter by **Incoming**, all the records that are assigned to PO Group 10 are displayed. If you’re the manager for PO group 10, you can see which groups are assigning how many records to your group. You may then focus on fixing any issues that you see.

\[Omitted image "process-graph-incoming.png"\] Alt text: Incoming records

If you filter by **Outgoing**, all the records that are assigned by PO Group 10 to other groups are displayed. If you’re the manager for PO group 10, you can see how many records have been reassigned from PO Group 10 to which groups. You may then focus on fixing any issues that you see.

\[Omitted image "process-graph-outgoing.png"\] Alt text: Outgoing records

You can filter on transitions too. Select any arc, a window is displayed with the details of the transition.

If you select PO Group 60, you see a window similar to the following.

\[Omitted image "node-transition.png"\] Alt text: Filter on transition

Select **Filter on transition**. The node star diagram displays results only for that one transition. As the image shows that PO Group 60 assigned records to PO Group 10. PO Group 10 then assigned the records to PO Group 16. PO Group 16 then assigned the records to PO Group 10. Finally, the records were closed.

\[Omitted image "node-transition-filter.png"\] Alt text: Filter on transition result

Select any node or arc, the **Show records** button is displayed. Select the **Show records** button. A scheduled task starts. After the scheduled task is complete, select **View result** in the Scheduled Tasks pane.

**Parent Topic:**[Using Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/now-intelligence/process-mining/use-process-mining.md)

