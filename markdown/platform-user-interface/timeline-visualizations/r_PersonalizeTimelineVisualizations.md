---
title: Personalize Timeline Visualizations
description: You can configure settings for timeline visualizations like lane and panel conditions, colors, and labels.
locale: en-US
release: zurich
product: Timeline Visualizations
classification: timeline-visualizations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use Timeline Visualization, Timeline Visualizations, Personalize your experience, Configure user experiences]
---

# Personalize Timeline Visualizations

You can configure settings for timeline visualizations like lane and panel conditions, colors, and labels.

## Personalization

Open the Settings pane and click **Configure**. Complete the form as appropriate \(see table\).

![Visualization personalization](../image/VisualizationPersonalization.png "Visualization personalization")

<table id="table_ghn_tlk_5q"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lane conditions

</td><td>

Condition builder used to create filters and apply sorting to values that are used as lanes in 3D view visualizations. For example, if you set \[Name\] \[is not\] \[IT\] as a lane condition for the CIO Roadmap, then IT no longer appears as a lane in the roadmap, nor does it appear as a lane option in the Settings pane. Removing the filter restores the IT lane to the visualization and to lane options in the Settings pane.

 To order the results, specify sorting based on relevant field names. For example, to order the portfolio names so that they appear in reverse alphabetical order on the CIO Roadmap, set the sort fields to \[Name\] \[z to a\].

</td></tr><tr><td>

Panel conditions

</td><td>

Condition builder used to create filters and apply sorting to values that are used as panels in the visualization. For example, if you set \[State\] \[is one of\] \[Pending, Open, Work in Progress\] as the panel condition for the CIO Roadmap, only projects that are in one of those states appear on the roadmap.

</td></tr><tr><td>

Panel color key

</td><td>

Field from the Panel table that contains values used for color coding the information displayed. The field selected here determines the values that are available in the Label fields on the form.

 The CIO Roadmap uses State, which is a field in the Project table. Panels on the CIO Roadmap are color coded according to the project state, which can be Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Skipped.

 Examples of other fields that are suitable for this selection include Priority, Risk, and Approval.

</td></tr><tr><td>

Label 1

 Label 2

 Label 3

 Label 4

</td><td>

Values to be color coded. The values available are determined by the Panel color key field. For example, the CIO Roadmap is based on the Project table and has the Panel color key' set to the State field, which contains the values Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Closed Skipped.

 You can set specific colors for up to four values from the selected field. Other values are shown in the Default color.

</td></tr><tr><td>

Default color

</td><td>

Color applied to values that are not selected for labels. For example, the CIO Roadmap color codes and creates labels for the values Pending, Open, Work in Progress, and Closed Complete. The additional values, Closed Incomplete and Closed Skipped, use the default color.

</td></tr><tr><td>

Color 1

 Color 2

 Color 3

 Color 4

</td><td>

Colors that correspond to each of the Label field values. For example, if Label 1 is the Pending state, and Color 1 is red, then panels for projects in the pending state are red.

</td></tr></tbody>
</table>**Note:**

-   Activating timeline visualizations doesn't activate predefined CIO roadmap. You require PPM \(com.snc.financial\_planning\_pmo\) plugin to use CIO roadmap.
-   If the **Max items per lane** field is set to more than `1000`, you may observe a delay when displaying the timeline data using Internet Explorer \(IE\) as the browser.

## The Settings pane

Element names in the Settings pane vary based on the table and fields used to create the visualization.

![CIO roadmap settings pane](../image/CIORoadmapSettingsPaneSm.png)

The Settings pane contains the following elements:

|Element|Description|
|-------|-----------|
|Key|Identifies the type of information that is color coded on the timeline, such as state or priority. It also lists the color assigned to each possible value, such as pending state and open state.|
|Configure|Allows you to personalize a visualization by creating filters on lane information and panel information, specifying sort order for results, and reassigning panel colors. These changes affect your view of the visualization only.|
|View|Allows you to switch between 2D and 3D view.|
|View &lt;table&gt; List|Opens a separate browser tab showing the complete record list for the associated table.|
|Portfolio|Allows you to click lane names to add or remove them from the visualization. While the visualization is in 2D view, the Settings pane displays a Show all &lt;records&gt; button that allows you to override lane filters applied to the initial setup.|

**Parent Topic:**[Use Timeline Visualization](../concept/c_UseTimelineVisualizations.md)

**Related topics**  


[Lanes, markers, and panels](../concept/c_Lanes.md)

[Use the slider and slider track](../concept/c_UseTheSliderAndSliderTrack.md)

[View timeline visualization](../task/t_ViewTimelineVisualization.md)

[Work with timeline visualizations](r_WorkWithTimelineVisualizations.md)

