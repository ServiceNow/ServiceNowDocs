---
title: Using Timeline in Investigation Canvas
description: The Timeline feature of the Investigation Canvas within the Threat Intelligence Security Center \(TISC\) empowers analysts to visualize, create, and edit timeline events associated to entities during investigations. This capability significantly enhances the effectiveness of temporal analysis.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-11-06"
reading_time_minutes: 4
breadcrumb: [Working with Investigation Canvas, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Using Timeline in Investigation Canvas

The Timeline feature of the Investigation Canvas within the Threat Intelligence Security Center \(TISC\) empowers analysts to visualize, create, and edit timeline events associated to entities during investigations. This capability significantly enhances the effectiveness of temporal analysis.

## Before you begin

This functionality streamlines the analysis process by representing the events in a chronological view and also supports quick decision making and more efficient threat response.

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  Go to **Investigation Canvases** &gt; **All Canvases**.

4.  Select any canvas record.

    Another option to navigate to a canvas record is from a case, which is explained as in the following step.

5.  Go to **Case Management** &gt; **All Cases**.

6.  Open any case record.

    **Note:** When creating a case, you’re required to either create a canvas or link an existing one. After linking, the canvas actions including the option to add timeline will be automatically available in the user interface.

7.  Go to **Investigation Canvas** section on the selected canvas record.

8.  Select the **Show Timeline** ![Show timeline](../image/tisc-timeline-toggle-icon.png) toggle icon to display the timeline section.

    The timeline section is hidden and you must make sure to select the **Show Timeline** option.

    ![Show timeline toggle on the investigation canvas](../image/tisc-show-timeline-section.png "View Timeline icon on the investigation canvas")

    The following screen shot illustrates the timeline components on the investigation canvas:

    |Component Number|Component Name|Description|
    |----------------|--------------|-----------|
    |01|Range indicator|Represents an event that is currently happening or previously happened during the determined period.|
    |02|Event indicator|Annotation line that represents the specific moment an event happened during the determined period of time|
    |03|Icon|Visual representation of a specific event type|
    |04|Pop over|a pop over displays when you select the timeline. a tooltip displays when users hover over the timeline.|
    |05|Grouped events|Automatically appears when two or more events are visually grouped because they are positioned too close in the current view.|
    |06|Zoom out control|Moves timeline view to earlier times and events on the timeline|
    |07|Zoom in control|Moves timeline view to later times and events on the timeline|
    |08|Timeline backward control|Moves backward through time, showing the same time range as the current view|
    |09|Legend control|Drop down that shows and hides the legend|
    |10|Timeline labels|Date labels that dynamically change or update to reflect the section of the timeline in view|
    |11|Timeline forward control|Moves forward through time, showing the same time range as the current view.|
    |12|Start Date|The start date and time that the event was opened for a case.|
    |13|End Date|The end date and time that the event is closed. The time is shown by the number of minutes and hours.|

    ![Timeline events](../image/tisc-timeline-events.png)

9.  Select the **Start Date** and **End Date**.

10. Select **Apply** to apply the changes or **Reset** to reset if you've to choose a different timeline.

    The canvas may contain multiple events. To focus on a specific event or a subset of events within a particular time period, set the desired date range and click **Apply**.

    Once applied, the timeline view will then zoom in to display only the filtered events, enabling focused analysis and easier investigation of relevant activity.

    From the Canvas perspective, each node can have multiple events. Select the node and right click on the node to either choose **Show Details** or **Open Record**, the application displays the form view of that record.

    ![Canvas Show node details](../image/tisc-show-details-canvas.png)

    In addition, within the form, navigate to the **Related Records** section where an entry called **Timeline Events** has been added. This provides a detailed view of all the timeline events associated with that particular node, linking the canvas visualization.

    ![Related Records - Timeline events](../image/tisc-timeline-related-records.png)

    Within the **Timeline Events** section, you can see the events associated with the selected node. Using this section, you have the option to **Add** or **Remove** an event from the node.

    ![Canvas - Adding timeline events to the related records](../image/tisc-add-timeline-library-record.png)

    This functionality provides direct control over which events are linked to a node and by complementing the visualization on the Canvas.

    **Important:** **Default events for Observables:** Certain events are automatically displayed for specific observables. For example, File observables include the **First Seen** and **Last Seen** fields.

    The system property `sn_sec_tisc.timeline_node_fields` provisioned in the base system that determines which fields are displayed on the timeline.

    By default, it contains the first\_seen and last\_seen fields. You can modify this property to add new fields or remove the existing ones based on your requirements.

    -   When a file observable is added to the Canvas, these events are shown by default.
    -   These default events are not driven by configuration and they appear automatically based on the values populated in the observables record.
    -   If **First Seen** and **Last Seen** contain values, then the corresponding events are displayed on the Canvas without any additional setup.

-   **[Adding Timeline Events to the Canvas](tisc-add-timeline-events.md)**  
Add timeline events to the investigation canvas by adding the related entities to the canvas.

**Parent Topic:**[Working with Investigation Canvas](../concept/tisc-investigation-canvases.md)

