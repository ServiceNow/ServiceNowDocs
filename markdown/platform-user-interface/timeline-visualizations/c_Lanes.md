---
title: Lanes, markers, and panels
description: Lanes, markers, and panels are the fundamental elements of a timeline visualization. appear in the 3D view only.
locale: en-US
release: xanadu
product: Timeline Visualizations
classification: timeline-visualizations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Use Timeline Visualization, Timeline Visualizations, Personalize your experience, Configure user experiences]
---

# Lanes, markers, and panels

Lanes, markers, and panels are the fundamental elements of a timeline visualization. appear in the 3D view only.

**Note:** Lanes and markers are available in the 3D view only. A panel in the 2D view always represents a single record, while panels in 3D view may represent one or more records.

## Lanes

A lane is a channel in which activities are grouped. A visualization can display up to eight lanes at a time. While viewing a visualization, you can use the Settings pane to show or hide individual lanes.

**Note:** The number of items displayed in a lane depends on the **Max items per lane** and **Max items per lane 2d** settings on [Timeline Visualization form](../task/t_CreateATimelineVisualization.md).

## Markers

Markers are horizontal lines that cross all lanes and identify a transition to the next month.

## Panels

Panels in both 2D and 3D views are color coded according to values that the administrator selects during the initial setup.

![3D panel](../image/3DPanelAnno.png)

![2D panel](../image/2DPanelAnno.png)

In 2D view, panels are grouped by month and stacked in chronological order, from the earliest date to the latest date. By default, the 2D view opens with the current month displayed on the left side of the visualization. You can print visualizations from the 2D view using the browser's print option. In 3D view, panels are grouped in lanes and ordered by date, from earliest to latest. The date that appears on the panel determines its placement in 2D and 3D view. The date displayed is based on a value the timeline administrator selects during initial setup.

Panels appear in the CIO Roadmap according to the planned completion date for the project. In 3D view, projects with the same planned date of completion are consolidated into a single panel. In 2D view, projects with the same planned date of completion are displayed as individual panels.

Panel headers in the CIO Roadmap are color coded based on project state. However, in 3D view, if a panel represents more than one project, the panel header is colored black. The Settings pane contains a key showing each available project state and the corresponding color.

**Note:** Activating timeline visualizations doesn't activate predefined CIO roadmap. You require PPM \(com.snc.financial\_planning\_pmo\) plugin to use CIO roadmap.

To view additional information about a panel:

-   Click a panel for a single record while in 2D or 3D view to open a summary window that contains additional information. Click the heading in the summary window to open the full record.
-   Press the Shift key and then click a panel to open the full record.
-   Click a panel that represents multiple records to open a list of those records. Click a record number to open the full record.

The timeline administrator can configure the information that appears in summary windows.

**Parent Topic:**[Use Timeline Visualization](c_UseTimelineVisualizations.md)

**Related topics**  


[Personalize Timeline Visualizations](../reference/r_PersonalizeTimelineVisualizations.md)

[Use the slider and slider track](c_UseTheSliderAndSliderTrack.md)

[View timeline visualization](../task/t_ViewTimelineVisualization.md)

[Work with timeline visualizations](../reference/r_WorkWithTimelineVisualizations.md)

