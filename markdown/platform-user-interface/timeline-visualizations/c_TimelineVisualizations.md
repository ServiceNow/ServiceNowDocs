---
title: Timeline Visualizations
description: A timeline visualization is a representation of an organization's activities over time.
locale: en-US
release: yokohama
product: Timeline Visualizations
classification: timeline-visualizations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Personalize your experience, Configure user experiences]
---

# Timeline Visualizations

A timeline visualization is a representation of an organization's activities over time.

Typically, timeline visualizations are useful for quickly assessing the impact of future strategic and operational activities such as change requests and projects. Timeline visualizations come in two varieties: a two-dimensional \(2D\) view where activities are grouped by month, and a three-dimensional \(3D\) view where activities are grouped in lanes. Both views are interactive, and the 2D view can be printed.

Timeline administrators, users with the timeline\_admin role, can set up visualizations to represent ITSM-related activities, such as incidents, problems, changes, and projects. Timeline administrators or users with the timeline\_user role can personalize their timeline visualizations from the Settings pane in the visualization.

The CIO Roadmap timeline visualization shows your organization's projects grouped by portfolios. Organizational leaders can use the CIO Roadmap to monitor and evaluate the status of current and upcoming projects.

**Note:** Activating timeline visualizations does not activate predefined CIO roadmap. You require PPM \(com.snc.financial\_planning\_pmo\) plugin to use CIO roadmap.

## Key terms for timeline visualizations

-   **Lane**

    A logical grouping of items on the 3D timeline visualization. For example, one lane might show pending projects while another lane shows open projects.

-   **Panel**

    A block that represents an item record in a 2D timeline visualization, or a block that represents one or more item records in a 3D timeline visualization.

-   **Summary view**

    A pop-up window that appears when a user clicks a panel in either the 2D or 3D timeline visualization. The summary view contains additional information about the record. Timeline administrators configure the information that appears in the summary view.

-   **Marker**

    A bar indicating the start of a month in a 3D timeline visualization.

-   **Slider**

    A tool used to control the time period seen in a 3D visualization.

-   **Slider track**

    An alternative view of the panels displayed in both the 2D and 3D timeline visualization.


![Timeline elements.](../image/CIORoadmap2DAnno.png) ![Timeline lanes.](../image/CIORoadmap3DAnno.png)

-   **[Activate Timeline Visualization](../task/t_ActivatingTimelineVisualization.md)**  
An administrator can activate the Timeline Visualization plugin \(com.snc.timeline\_visualization\) to access the functionality.
-   **[Create a Timeline Visualization](../task/t_CreateATimelineVisualization.md)**  
Set up timeline visualizations for the organization's leaders by creating a timeline that provides visual representations of the organization's operational and strategic activities.
-   **[Create a Timeline Visualization view](../task/t_CreateATimelineVisualizationView.md)**  
The timeline visualization view determines which record details appear in the pop-up summary window when a user clicks a panel.
-   **[Planning Your Timeline Visualization](c_PlanningYourTimelineVisualization.md)**  
Before creating a timeline visualization, you should have a clear idea of the information that you want to display.
-   **[Use Timeline Visualization](c_UseTimelineVisualizations.md)**  
Timeline Visualization provides a high-level view of an organization's strategic and operational activities over time.

**Parent Topic:**[Personalize your experience](../../../administer/general/concept/personalize-your-experience.md)

