---
title: Discovery timelines
description: A Discovery timeline generates a graphical display of a Discovery Status record, including information about each probe and sensor that was used in the discovery.A Discovery Timeline generates a graphical display of a Discovery Status record, including information about each probe, sensor, and pattern running.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Discovery status, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery timelines

A Discovery timeline generates a graphical display of a Discovery Status record, including information about each probe and sensor that was used in the discovery.

Use Discovery Timelines to display the following:

-   The flow of [probes and sensors](c_DiscoveryProbesAndSensors.md), including those that are used with [patterns](c-UsingPatternsForHorizontalDiscovery.md#) through a discovery.
-   The duration of each probe and sensor that ran during a discovery, and the proportion of time required for queuing and processing.
-   Tooltips containing additional data about a probe and sensor.
-   Records from the ECC Queue.

## Size of discoveries in the timeline

View timelines for an entire discovery or for individual devices in a discovery. By default, the maximum size discovery that you can display in a timeline is 300 entries in the ECC Queue \(150 probes and 150 sensors\). To display larger discoveries, change the default setting in the glide.discovery.timeline.max\_entries property.

## Example Discovery Timelines

This example shows the Discovery timeline for the first two phases of Discovery \(Port scan and Classification\):

![Discovery early phases on the timeline](../image/disco-timeline-early-phases.png "Discovery (early phases) on the timeline")

In this example, the Shazzam probe and sensor run, followed by the Unix classifier probe and sensor. The classifier calls the Horizontal Pattern probe, which runs a specific pattern.

**Parent Topic:**[Discovery status](c_DiscoveryStatus.md)

## View the Discovery timeline

A Discovery Timeline generates a graphical display of a Discovery Status record, including information about each probe, sensor, and pattern running.

### Before you begin

Role required: discovery\_admin or admin

### About this task

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Status**.

2.  Select a Discovery from the record list.

3.  Click the **Show Discovery Timeline** Related Link.

4.  Clear the warning, and then select the **Devices** Related List.

5.  Click the IP address of a device.

6.  In the Device record, click the **Show Discovery Timeline** Related Link.

    The Discovery timeline for that device appears.

    ![Discovery Timeline](../image/DiscoveryTimeline.png "Discovery Timeline")

7.  Use the pink slider at the bottom of the timeline to change the perspective.

    1.  Move the slider from right to left to view all the tasks on a long timeline.

    2.  Adjust the end points of the slider to change the magnification.

        A narrow slider zooms in on the spans and provides a more detailed view of complex timelines. A wide slider pulls the view out and makes more of the timeline visible on the screen.

8.  Use the selector range at the top of the screen to adjust the visible time frame.

9.  To limit the timeline to the length of the Discovery, click **Max**.

    The time scale adjusts automatically to the length of the Discovery. The available time scale range is from one day to 1 year.

    Tooltips

    Discovery timelines display probe and sensor performance data and CI information in tooltips. Hover your cursor over a span to view this data.

    Probes are displayed by black spans. The queue time for a probe is shown as a silver bar within the span, and the processing time is represented by the remaining space.

    Sensor spans are red, and the queue time is shown as a green bar. Selected spans of any type display in yellow.

    ![Discovery Timeline Shazzam Sensor](../image/DiscoveryTimelineShazzamSensor.png "Discovery Timeline Shazzam Sensor")

    ECC Queue

    Double-click a span to open the ECC Queue record for that probe or sensor.

    ![Discovery Timeline ECC Queue](../image/DiscoveryTimelineECCQueue.png "Discovery Timeline ECC Queue")


