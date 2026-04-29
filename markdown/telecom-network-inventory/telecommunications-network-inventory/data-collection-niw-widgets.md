---
title: Data collection and refresh for the Network Inventory Workspace widgets
description: Learn how the Telecommunications Network Inventory data that appears on the Network Inventory Workspace landing page is collected and refreshed.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Define inventory records, Use, Telecommunications Network Inventory]
---

# Data collection and refresh for the Network Inventory Workspace widgets

Learn how the Telecommunications Network Inventory data that appears on the Network Inventory Workspace landing page is collected and refreshed.

To increase the responsiveness and speed of the Network Inventory Workspace, a scheduled job runs once a day to collect the count data that appears on the landing page. This job collects this data from the Configuration Management Database \(CMDB\) Groups \[cmdb\_group\] table.

Each landing page section, or widget, has a Configuration Management Database \(CMDB\) group that is assigned to it, and it provides the count data that you see. For example, the Network sites overview widget contains the counts for the total number of your sites, and for your sites that are currently in maintenance. The Network entities by category widget contains the counts for each category of network equipment that your organization has, such as the interface cards and connections.

## CMDB Groups table

The CMDB Groups table contains the Component Item \(CI\) records on which the count totals in each landing page widget are based. When the scheduled job runs on the CMDB Group database, it performs the following actions:

1.  Evaluates the query condition that is stated in the CMDB group and then collects the count data. Administrative users with certain assigned roles can define and apply the specific conditions that it uses for these queries to collect the count data for the landing page. To learn more, see [Customizing the content in your Network Inventory Workspace widgets](customizing-content-in-your-network-inventory-workspace-widgets.md).
2.  Generates records in the CMDB Group Metadata \[sn\_cmdb\_ws\_group\_metadata\] table.
3.  By using the collected data in the CMDB Group Metadata table, it refreshes each count that appears on the landing page.

**Parent Topic:**[Reviewing and updating your network inventory with the Network Inventory Workspace](tni-workspace.md)

**Related topics**  


[Network Inventory Workspace](exploring-network-inventory-workspace.md)

