---
title: Components of project workbench
description: The project workbench displays project information in two distinct areas. The top pane displays the project visualization, and the bottom pane displays phase details in a list view or visual task board. There is also a header above the workbench that includes several buttons and controls.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Using Project workbench - Legacy, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Components of project workbench

The project workbench displays project information in two distinct areas. The top pane displays the project visualization, and the bottom pane displays phase details in a list view or visual task board. There is also a header above the workbench that includes several buttons and controls.

The project workbench scales to fit the available browser height. If necessary, scroll bars are added to display the workbench details.

## Header

The header is a gray bar that runs across the top of the project workbench.

The first time a user accesses the project workbench from the Project menu, the header displays the following components:

After a project is opened, the header displays additional components, depending on the type of project selected.

-   Back \(![screenshot for back icon](../image/ProjectWorkbenchBackIcon.png)\): takes the user to the Project form to view the project details.
-   **Select Project**: displays the current project name. Click the down arrow to select a new project.
-   Add phase icon \(![screenshot for Add phase icon](../image/ProjectWorkbenchAddPhaseIcon.png)\): adds a phase or milestone to the timeline.
-   **Apply Template**: opens a dialog box for setting a start date and adding a template to the project. This button appears for new or blank projects that have no phases.
-   **Manage Stories**: under the Options icon \(![screenshot for Options icon](../image/elipsis_icon.png)\) displays the story backlog for this project.
-   **List**: under the Options icon \(![screenshot for Options icon](../image/elipsis_icon.png)\) displays additional details in list view about the currently selected phase. This button appears if a project has one or more phases.
-   **VTB**: under the Options icon \(![screenshot for Options icon](../image/elipsis_icon.png)\) displays additional details in the Visual Task Board about the currently selected phase. This button appears if a project has one or more phases.

## Timeline

The top pane of the project workbench displays the project timeline. The timeline uses monthly or quarterly markers to represent time. If the duration of a project is less than 500 days, these markers represent months and if the duration is greater than 500 days, these markers represent quarters.

The project timeline displays the following project information:

-   Project name: the name assigned to the project. Point to the project name to see a message about the project date calculation method used for this project.
-   Percentage complete: the percentage of the project that has been completed. This percentage is based on the duration and the percentage complete of the individual phases.
-   Project start and end dates: the dates specified in the **Planned start date** and **Planned end date** fields for this project.
-   Project phases: colored bars that represent the different phases of the project.
-   Milestones: colored and dynamic circles on the timeline that represent important dates in the project life cycle.

**Phases in timeline**

A project phase is represented in the timeline by a horizontal bar. The bar is connected to the timeline by a thin vertical line that indicates the phase start date. The name of the phase appears just above the horizontal bar. Project phases are stacked in the timeline by start date, phase, and the earliest start date appearing at the top. If there are phases than can fit on the timeline, a scroll bar appears on the right side.

The color of the horizontal bar changes incrementally to reflect the completion percentage of the phase. The percentage completion is calculated based on the phase type:

-   **Waterfall**: includes project tasks. The completion percentage is based on the number of project tasks that have been completed.
-   **Agile**: includes stories. The completion percentage is based on the number of story points that have been completed.
-   **Test**: includes test cases. The completion percentage is based on the number of test cases that have been completed.

The available phases depend on how Project Management is installed. When Project Management is installed as a standalone app, the project manager can only create and edit the Waterfall phase type. When Project Management is installed as part of the Project Portfolio Management \(PPS\), the project manager can create and edit all phase types \(Waterfall, Agile, and Test\).

When you point to a phase, the cursor changes from an arrow to a hand and a pop-up window displays the phase name and the start and end dates. Clicking a phase in the timeline displays the corresponding task information in the bottom pane of the project workbench.

**Milestones in timeline**

Milestones indicate important dates in a project and are represented along the timeline by colored circles. Three colors are available for milestones: green, yellow, and red. The project manager determines how the colors are used.

Pointing to a milestone changes the cursor from an arrow to a hand and displays a pop-up window with the short description and planned start date.

Select a milestone to update the milestone information. You can also drag a milestone along the timeline to change the date. Milestones can be dragged to any point on the timeline within the boundaries of the project start and end dates.

## Detail view

The bottom pane of the project workbench displays detailed information for the phase currently selected in the timeline. The information displayed varies by the phase type selected:

-   **Waterfall**: displays the project tasks associated with the phase.
-   **Agile**: displays the stories assigned to the phase.
-   **Test**: displays the test cases for the testing phase.

Information in the bottom pane can be displayed in list view or in a visual task board. The **List** and **VTB** buttons in the Project Workbench header control how this information is displayed.

**Parent Topic:**[Using Project workbench - Legacy](c_ProjectWorkbench.md)

**Related topics**  


[Access the project workbench](../task/t_AccessTheProjectWorkbench.md)

[Project calculation](c_ProjectWorkbenchProjectCalc.md)

[Managing Project workbench](c_UsingProjectWorkbench.md)

