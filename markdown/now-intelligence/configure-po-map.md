---
title: Configure a Process Mining map on a dashboard
description: Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Configure a Process Mining map on a dashboard

Map the different states that are part of your process and the transitions between those states. See which states the objects of the process are in and the speed with which they change state.

## Before you begin

You should be familiar with Process Mining and Process projects. For more information, see [Process Mining](../../../administer/process-mining/concept/process-mining.md).

The relevant Process project must already exist.

Role required: sn\_process\_optimization\_analyst

## About this task

The Process Mining Map component enables users to visualize how a process is being executed for a particular data set that is being analyzed. For example, you can show users the number of records for a specific date range, business area, and region.

This component offers similar content on any dashboard that you get from process maps in the Process Mining Workspace. For more information about process maps, see [Process details page](../../../administer/process-mining/concept/project-view-screen.md).

## Procedure

1.  Create a dashboard, or navigate to a dashboard that you are allowed to edit.

    For more information, see [Create a dashboard with the in-line editor](../../dashboards/task/create-db-in-ac.md).

2.  Select **Edit** to enter editing mode.

3.  Expand **Add new element** and scroll down to Process Mining - Map.

    When you select this element, it is added to the dashboard, and its configuration panel opens.

4.  Under **Header and border**, set whether the map shows a header or a border, along with the chart title in the header and a description.

5.  Under **Data** in the Process Mining - Map configuration panel, select a Process Mining project.

    You can only select a Process Mining project that you can access.

6.  For the map to follow filters on the dashboard, select **Follow filters**.

    For more information, see [Applying filters to Process Mining maps](../concept/applying-filters-to-process-optimization-maps.md).

7.  Set the percentage of connections to show.

    Connections are lines that show how the subjects of the mapped process change states. These lines end in arrows to show the direction of the change. They also have boxes that show the number of records that followed that path and the average time they spent in the earlier state before moving. For example, if a box in the middle of a connection says 505/5d, ![Details box in the middle of a connection](../image/po-map-connection-detail.png) 505 records have followed this change in state, and the average time in the earlier state was 5 days.

    The most frequent changes are shown first. So if you accept the default 20%, only the 20% most frequent changes between states are shown. Too low a number results in too little data being shown on the map. Too high a number turns the map into a mass of spaghetti, with many rare changes between states that you might not care about.

8.  Set the percentage of activities to show.

    Activities, or nodes, are the possible states of the subject of the process. For example, if you are looking at Incidents, an incident can be in the Assigned state or the Work in progress state. Too many activities can clutter the map, but generally show as many as you can.

9.  Animate the map by turning on **Case follow simulation**.

    When **Case follow simulation** is active, the solid lines of the connections are replaced by moving dashed lines. The speed at which the dashes move represents the speed at which objects move from one state to the next. The thickness of the dashes shows the relative amounts of traffic.

    ![Process Mining map animated to show process flow speed](../image/po-map-animation.gif)

10. Specify the header and border settings, such as the title and description.


## What to do next

Outside of editing mode, a user can expand the settings ![Cogwheel](../../performance-analytics/image/Cogwheel.png) on the map. In these settings, they can adjust the connection and activities percentages and turn animation on and off.

![A user adjusting map configuration settings on the fly](../image/po-map-adjust-runtime.gif)

**Related topics**  


[Process Mining](../../../administer/process-mining/concept/process-mining.md)

[Analyst workbench page](../../../administer/process-mining/concept/analyst-workbench-dashboard.md)

[Refining a process map](../../../administer/process-mining/concept/analyze-data.md)

