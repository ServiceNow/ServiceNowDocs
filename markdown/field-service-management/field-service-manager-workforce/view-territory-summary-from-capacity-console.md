---
title: View data in capacity console
description: The Capacity Console is a visualization tool designed to address common organizational challenges related to resource availability and capacity utilization. It enables real-time visibility into capacity, identifies bottlenecks, and enables quick adjustments to meet changing demands, helping organizations optimize their operations effectively.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Capacity Console, Capacity, Workforce, Use, Field Service Management]
---

# View data in capacity console

The Capacity Console is a visualization tool designed to address common organizational challenges related to resource availability and capacity utilization. It enables real-time visibility into capacity, identifies bottlenecks, and enables quick adjustments to meet changing demands, helping organizations optimize their operations effectively.

## Before you begin

Role required: fsm\_adv\_cap\_mgmt.wm\_capacity\_planner, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_capacity\_mg.wm\_capacity\_read

## About this task

When you open the Capacity Console, the calendar appears to present the capacity of various territories and data from multiple demand channels. The other benefits are:

-   Real-time Insights: Gain immediate visibility into resource utilization and capacity allocation for each territory.
-   Informed decision-making: Identify underutilized or overutilized resources to optimize task assignments.
-   Selectable filters: Use filters and preferences to tailor the data view to your specific needs.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM configurable workspace** &gt; **Capacity console**.

2.  In the **Territory** filter, select the territories.

3.  In the **Demand Channel** filter, select the demand channels.

4.  Select the **Group by** filter and choose either territory or demand channel.

    The data view can be grouped either by territory or demand channel, enabling the capacity planner to switch perspectives easily. For example, grouping by territory shows capacity for each territory, broken down by demand channels, while grouping by demand channel shows data for each channel and its territories.

5.  Use the unit filter to choose between **Hours** for hour-based capacity assignments \(for example, agent schedules and hour-type definitions\) or **Tasks** for task-based capacity assignments, focusing on task distribution.

6.  Use the advanced filter to view data specific to territories and demand channels based on performance.

    Choose either of the following.

    -   Underutilized \(Orange\): Displays days and demand channels with significant underutilization, enabling users to make targeted decisions. Less than 25% of capacity is used.
    -   Optimally used \(Green\): Highlights areas with optimal usage, helping users maintain efficiency. Optimal utilization falls between 25% and 75%.
    -   Overutilized \(Blue\): Identifies days and channels where capacity is exceeded, aiding in resource reallocation. More than 75% of capacity is over used.
    -   No Capacity \(Blank\): No capacity is defined for the selected criteria.
7.  Select **Save filters**.

    Selections remain intact when you log in again or refresh the session.

8.  Select the week using the calendar.

9.  Choose the week view or two-week view for a broader perspective for capacity planning.

    The default view is week-view.


## Result

The capacity data appears in the calendar based on the applied filters.

**Related topics**  


[Using the Capacity Console](../concept/capacity-and-reservation-management-console.md)

[View territory and demand channel summary in the contextual side panel](view-territory-summary-in-capacity-console.md)

[Update capacity value and reservation for a territory in capacity console](update-reservation-rule-in-capacity-console.md)

[Activate Field Service Capacity console](capacity-console-plugin.md)

