---
title: Task Planner component setup
description: The Task Planner is used to provide a single view of project tasks in a list and timeline format. The component is a combination of the sn-datagrid and now-gantt components.Configure Task Planner declarative actions and buttons with these properties.Select event handlers to configure the actions \(events\) provided with the Task Planner component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/task-planner-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Task Planner component setup

The Task Planner is used to provide a single view of project tasks in a list and timeline format. The component is a combination of the `sn-datagrid` and `now-gantt` components.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Task Planner that differentiates it from other components in the [content tree](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "task-planner-component-content-tree.png"\] Alt text: Task Planner component in the content tree.

2.  Select the Task Planner component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Task Planner label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Task Planner component properties

Configure Task Planner declarative actions and buttons with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_yqj_kj1_j4b"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Toolbar title

</td><td>

toolbarTitle

</td><td>

Title of the toolbar.

</td></tr><tr><td>

Show row count

</td><td>

showRowCount

</td><td>

Option to show the number of project tasks for the selected project.

</td></tr><tr><td>

Show help

</td><td>

showHelp

</td><td>

Option to show the help button on the toolbar.

</td></tr><tr><td>

Columns

</td><td>

columns

</td><td>

List of column configurations for rendering on Gantt.

</td></tr><tr><td>

Tasks

</td><td>

Tasks

</td><td>

List of tasks for rendering on Gantt.

</td></tr><tr><td>

Baselines List

</td><td>

baselines

</td><td>

List of baselines for rendering on Gantt.

</td></tr><tr><td>

Baseline Items List

</td><td>

baselineItems

</td><td>

List of baseline names to show on Gantt

</td></tr><tr><td>

Zoom level

</td><td>

zoomLevel

</td><td>

Defines zoom level configuration for the timeline. Available options are: -   **Day and Month**
-   **Month and Quarter**
-   **Quarter and Year**
-   **Year**
-   **autofit**

</td></tr><tr><td>

Date Format

</td><td>

dateFormat

</td><td>

Format for displaying the dates in the date fields. For example, Start Date and End Date.

</td></tr><tr><td>

Date time format

</td><td>

dateTimeFormat

</td><td>

Format for displaying the date and time.

</td></tr><tr><td>

Time zone

</td><td>

timeZone

</td><td>

User's time zone.

</td></tr><tr><td>

Enable read only view

</td><td>

readOnly

</td><td>

Option to view the Task Planner in read-only mode.

</td></tr><tr><td>

Show Preview record icon

</td><td>

previewRecordIcon

</td><td>

Option to preview the project or project task record.

</td></tr><tr><td>

Show current timeline

</td><td>

hideCurrentTimeLine

</td><td>

Option to show the current date on timeline that is shown in the vertical line.

</td></tr><tr><td>

Show start and end timeline

</td><td>

showStartEndTimeline

</td><td>

Option to show start and end date of the project task on timeline.

</td></tr><tr><td>

Allow move task

</td><td>

canMoveTask

</td><td>

Option for allowing moving a project task in the Gantt.

</td></tr><tr><td>

Settings panel configurations

</td><td>

settingsPanel

</td><td>

Option for adding additional tab in the settings panel and customising settings panel tab labels.

</td></tr><tr><td>

Allow task duration change

</td><td>

canResizeTask

</td><td>

Option for allowing changing the duration of a project task.

</td></tr><tr><td>

Allow dependency creation on Gantt Chart

</td><td>

canCreateDependency

</td><td>

Option to allow creation of dependency on the Gantt.

</td></tr><tr><td>

Allow switching layout

</td><td>

canSwitchLayout

</td><td>

Option to switch layout from the column config menu.

</td></tr><tr><td>

Gantt chart layout

</td><td>

layout

</td><td>

Option to choose between the Gantt Chart layouts. Available options are: -   **Grid and Timeline**
-   **Grid**
-   **Timeline**

</td></tr><tr><td>

Timeline popover config

</td><td>

timelinePopoverConfig

</td><td>

Configuration for timeline pop over details such as width, fields, and title.

</td></tr><tr><td>

Enable auto save

</td><td>

isAutoScheduledSave

</td><td>

Option to enable auto-save for Task Planner.

</td></tr><tr><td>

Enable reorder row

</td><td>

reorderRows

</td><td>

Option to enable reordering the project task rows.

</td></tr><tr><td>

Reorder row label source column

</td><td>

reorderRowsLabelSourceColumn

</td><td>

Specifies which column values should be visible when reordering the rows.

</td></tr><tr><td>

Tables for which warning duration is applicable

</td><td>

statusProcessEntities

</td><td>

Tables for which warning duration is applicable.

</td></tr><tr><td>

Duration in day\(s\) to show attention require status

</td><td>

warningStatusDuration

</td><td>

Duration in days to show that attention is required for the user based on the status of the project task.

</td></tr><tr><td>

Status Choice

</td><td>

statusChoices

</td><td>

Option to define choices for the status column of the project task. For example, Green, Yellow, and Red.

</td></tr><tr><td>

Child table name

</td><td>

childEntity

</td><td>

Child table for the selected project.

</td></tr><tr><td>

State config

</td><td>

stateConfig

</td><td>

Option to define state for the state column of the project task. For example, Open, Pending, Work in progress, and Closed Complete.

</td></tr><tr><td>

Auto save interval

</td><td>

autoSaveInterval

</td><td>

Interval in milliseconds for auto-saving the project workspace data.

</td></tr><tr><td>

Save batch size

</td><td>

saveBatchSize

</td><td>

Size of the batch that will be saved at a time for the project task.

</td></tr><tr><td>

Grid width

</td><td>

gridWidth

</td><td>

Width of grid part in Gantt.

</td></tr><tr><td>

Delete batch size

</td><td>

deleteBatchSize

</td><td>

Size of the batch that will be deleted at a time for the project task.

</td></tr><tr><td>

Hide Time Component

</td><td>

hideTimeComponent

</td><td>

Hides the time value for all the date\_time fields.

</td></tr><tr><td>

Task dependencies

</td><td>

dependencies

</td><td>

List of dependency between project tasks.

</td></tr><tr><td>

Work schedule

</td><td>

workSchedule

</td><td>

Schedule of the project. Default value is 10 years \(based on the values of the properties, `com.snc.schedule_loader.project_management.cache_years_before` and `com.snc.schedule_loader.project_management.cache_years_after`\).

</td></tr><tr><td>

On-demand work schedule

</td><td>

onDemandWorkSchedule

</td><td>

On-demand schedule of the project for the selected range beyond the values of the properties, `com.snc.schedule_loader.project_management.cache_years_before` and`com.snc.schedule_loader.project_management.cache_years_after`.

</td></tr><tr><td>

Date/DateTime Scheduling

</td><td>

workScheduleStrategy

</td><td>

Date/Time schedule configuration.

</td></tr><tr><td>

Hide timeline

</td><td>

hideTimeline

</td><td>

Option to hide the Gantt timeline in the project workspace.

</td></tr><tr><td>

Disable save event

</td><td>

suspendSaveEvent

</td><td>

Option to disable the save event in auto-save mode when the Save API is busy.

</td></tr><tr><td>

Last saved at

</td><td>

lastSavedAt

</td><td>

Timestamp when the data was last saved in the database in user-display format.

</td></tr><tr><td>

Last saved tasks

</td><td>

lastSavedTasks

</td><td>

Project tasks that were saved successfully last time in the database.

</td></tr><tr><td>

Retrigger Save

</td><td>

retriggerSave

</td><td>

Option to execute the save event again when the Save API fails.

</td></tr><tr><td>

Sub project meta data

</td><td>

subProjectMetadata

</td><td>

Option to send the metadata of a sub project to the parent project.

</td></tr><tr><td>

Blacklisted actions

</td><td>

blackListedActions

</td><td>

List of actions that are available to exclude. Excluded actions aren't available to the user.

</td></tr><tr><td>

Force Save

</td><td>

forceSave

</td><td>

If auto-save is false, then the Save option is shown.

</td></tr><tr><td>

Project Preferences

</td><td>

projectPreferences

</td><td>

JSON object of project preferences.

</td></tr><tr><td>

Hours in a day

</td><td>

hoursInADay

</td><td>

Defines hours in a day for the project task based on schedule.

</td></tr><tr><td>

Max duration\(in days\) allowed for a task

</td><td>

maxTaskDuration

</td><td>

Defines the max duration allowed for a project task or the overall project.

</td></tr><tr><td>

Displays Resource Panel

</td><td>

showResourcePanel

</td><td>

Displays the bottom resource panel grid.

</td></tr><tr><td>

Resource Columns

</td><td>

resourceGridColumns

</td><td>

List of column configurations for rendering the resource grid.

</td></tr><tr><td>

Resource Assignments

</td><td>

resourceAssignments

</td><td>

List of assignments for rendering the resource grid.

</td></tr><tr><td>

Resource config

</td><td>

resourceGridConfig

</td><td>

Resource grid configuration.

</td></tr><tr><td>

Last saved grid assignments

</td><td>

lastSavedGridAssignments

</td><td>

Last updated assignments in the database.

</td></tr><tr><td>

Resource Allocations

</td><td>

resourceAllocations

</td><td>

Allocation data for each resource assignment.

</td></tr><tr><td>

Can create project task

</td><td>

canCreateTask

</td><td>

Option to allow users to create project task on planner.

</td></tr><tr><td>

Is ResourceAssignment Aligned

</td><td>

IsResourceAssignmentAligned

</td><td>

Indicates whether all resource assignments are aligned with the project.

</td></tr></tbody>
</table>## Task Planner component events

Select event handlers to configure the actions \(events\) provided with the Task Planner component.

The Events tab shows the events used by the Task Planner component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Task Planner actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|SN\_TASK\_PLANNER\#DATA\_SAVED|Action dispatched when the user saves the updated task data.|
|SN\_TASK\_PLANNER\#COLUMN\_RESET|Action dispatched when the user resets the columns.|
|SN\_TASK\_PLANNER\#TIMELINE\_ZOOM\_CHANGED|Action dispatched when timeline precision is changed.|
|SN\_TASK\_PLANNER\#SUMMARY\_TOGGLED|Action dispatched when display summary task is toggled in the settings panel.|
|SN\_TASK\_PLANNER\#BAR\_LABELS\_TOGGLED|Action dispatched when bar labels toggled in the settings panel.|
|SN\_TASK\_PLANNER\#DEPENDECY\_LINES\_TOGGLED|Action dispatched when display dependency lines toggled in the settings panel.|
|SN\_TASK\_PLANNER\#CRITICAL\_PATH\_TOGGLED|Action dispatched when show critical path toggled in the settings panel.|
|SN\_TASK\_PLANNER\#SCHEDULE\_REQUESTED|Action dispatched when the user fetches an on-demand schedule when a schedule is not available.|
|SN\_TASK\_PLANNER\#COLUMN\_UPDATED|Action dispatched when the columns are updated.|
|SN\_TASK\_PLANNER\#DATA\_REF\_REQUESTED|Action dispatched when the user refreshes the data.|
|SN\_TASK\_PLANNER\#PREVIEW\_RECORD\_ICON\_CLICKED|Action dispatched when the user clicks the preview record icon.|
|SN\_TASK\_PLANNER\#REALIGN\_ASSIGNMENTS\_TO\_TASK|Action dispatched when realign assignments to task is requested.|
|SN\_TASK\_PLANNER\#DIRTY\_DATA\_EXISTED|Action dispatched when either dirty data existed or queued.|
|SN\_TASK\_PLANNER\#PLAN\_CLOSED|Action dispatched when the project is closed.|
|SN\_TASK\_PLANNER\#PRIMARY\_COLUMN\_CELL\_LINK\_CLICKED|Action dispatched when you click the primary column's cell.|
|SN\_TASK\_PLANNER\#LINK\_CLICKED|Action dispatched when the user clicks the dependency link.|
|SN\_TASK\_PLANNER\#CREATE\_BASELINE\_REQUESTED|Action dispatched to open or create a baseline.|
|SN\_TASK\_PLANNER\#APPLY\_BASELINE\_BTN\_CLICKED|Action dispatched to show the selected baselines.|
|SN\_TASK\_PLANNER\#CREATE\_TASK\_DEPENDENCY|Action dispatched to open or create a task dependency.|
|SN\_TASK\_PLANNER\#COMPONENT\_CONNECTED|Action dispatched when the SN\_TASK\_PLANNER component is connected.|
|SN\_TASK\_PLANNER\#COMPONENT\_TREE\_RENDERED|Action dispatched when the SN\_TASK\_PLANNER component tree is rendered.|
|SN\_TASK\_PLANNER\#GRID\_RESIZED|Action dispatched when the grid is resized.|
|SN\_TASK\_PLANNER\#SERVER\_ACTION|Action dispatched to save the SN\_TASK\_PLANNER component actions.|
|SN\_TASK\_PLANNER\#ADD\_EXTERNAL\_DEPENDENCY|Action dispatched when you click the Add external dependency context menu.|
|SN\_TASK\_PLANNER\#OPEN\_PROJECT|Action dispatched when you click the View project context menu.|
|SN\_TASK\_PLANNER\#APPROVE\_OR\_REJECT\_RELATIONS|Action dispatched when approve or reject relations context menu action is clicked.|
|SN\_TASK\_PLANNER\#SHOW\_ALLOCATION\_HEATMAP|Action dispatched when the Allocation Heatmap is toggled.|
|SN\_TASK\_PLANNER\#HEATMAP\_VIEW\_CHANGED|Action dispatched when the Heatmap view is changed.|
|SN\_TASK\_PLANNER\#NOW\_RESIZABLE\_PANE\_SIZES\_CHANGED|Action dispatched when the sizes of the panes are changed.|
|SN\_TASK\_PLANNER\#BOTTOM\_GRID\_REFRESH\_ICON\_CLICKED|Action dispatched when you click the Grid refresh icon.|
|SN\_TASK\_PLANNER\#ALLOCATION\_HEATMAP\_CELL\_CLICKED|Action dispatched when you click the Allocation Heatmap cell.|
|SN\_TASK\_PLANNER\#SHOW\_ACTUALS\_TOGGLED|Action dispatched when Show actuals is toggled.|
|SN\_TASK\_PLANNER\#EFFORT\_TYPE\_VIEW\_CHANGED|Action dispatched when Effort type view is changed.|
|SN\_TASK\_PLANNER\#VIEW\_STORIES\_FOR\_AGILE\_TASK|Action dispatched when view stories is clicked for agile phase type tasks.|
|SN\_TASK\_PLANNER\#SIDE\_PANEL\_CLOSED|Action dispatched when side panel is closed.|
|SN\_TASK\_PLANNER\#EXTEND\_RESOURCE\_ASSIGNMENT|Action dispatched when extend is selected on a resource assignment.|
|SN\_TASK\_PLANNER\#MOVE\_RESOURCE\_ASSIGNMENT|Action dispatched when move is selected on a resource assignment.|
|SN\_TASK\_PLANNER\#DATA\_DISPATCH|Action dispatched when dataRequested value is set.|
|SN\_TASK\_PLANNER\#COLUMN\_PERSONALIZE\_REQUESTED|Action dispatched when column personalization is requested.|
|SN\_TASK\_PLANNER\#ASSIGN\_RESOURCE\_ASSIGNMENT|Action dispatched when assign work is selected on a resource assignment.|

