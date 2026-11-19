---
title: Gantt Chart component setup
description: The Gantt Chart is a commonly used graphical depiction of a project schedule. It’s a type of bar chart that shows the start and finish dates of various project elements such as planning and dependencies.Configure the behavior and personalization settings of your Gantt Chart component with these properties.Select event handlers to configure the events provided with the Gantt Chart component. Event handlers work with data resources to link the Gantt Chart actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/gantt-chart-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 20
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Gantt Chart component setup

The Gantt Chart is a commonly used graphical depiction of a project schedule. It’s a type of bar chart that shows the start and finish dates of various project elements such as planning and dependencies.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Gantt Chart that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "gantt-chart-component-content-tree.png"\] Alt text: Gantt Chart component in the content tree.

2.  Select the Gantt Chart component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Gantt Chart label you created for your component in the content tree.
    The configuration options appear in the setup panel on the right.

    \[Omitted image "gantt-chart-component-config-options.png"\] Alt text: Gantt Chart component configuration options.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Gantt Chart component properties

Configure the behavior and personalization settings of your Gantt Chart component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Configuration types and sections

Gantt Chart configuration is divided based on type of capability required and section of affected part. The Gantt Chart types and sections help to find the required properties easily and configure them.

-   **Gantt Chart configuration types**

    Gantt Chart configuration is divided into three types, Basic, Standard, and Advanced.

    -   Basic: The Basic type configuration needs a minimum of setup and data to operate, as it’s a read-only Gantt mode. Basic type has a constrained set of features.
    -   Standard: The Standard type configuration includes more than what is necessary, but also has a few features that can be changed. The Standard type is meant for users who want more than absolutely necessary features but don't want to spend much time for configuring everything.
    -   Advanced: The Advanced type configuration includes all the properties and is intended for advanced users who are at ease and want complete control over every aspect of the Gantt Chart. It also includes some advanced properties to change the appearance and functionality of the Gantt Chart.
    |Feature|Gantt Chart type|
    |-------|----------------|
    | |Basic|Standard|Advanced|
    |Columns|Yes|Yes|Yes|
    |Tasks|Yes|Yes|Yes|
    |Timeline bar|Yes|Yes|Yes|
    |Gantt Chart edit mode|No|Yes|Yes|
    |Dependency lines|No|Yes|Yes|
    |Baseline|No|Yes|Yes|
    |Define weekends and holidays|No|Yes|Yes|
    |Tweak popover contents|No|Yes|Yes|
    |Adjust row heights|No|No|Yes|
    |Control side panel contents|No|No|Yes|
    |Define custom Zoom levels \(Day, Hours, Minute etc.\)|No|No|Yes|
    |Add new rows on the timeline|No|No|Yes|

-   **Gantt Chart configuration sections**

    Gantt Chart configuration is divided into seven sections to make it easier for the users to find configuration based on the usage group. Some properties are dynamically shown or hidden based on the other properties or configuration type selection to guide you through the setup process.

    -   Type: Configuration for the chart type, such as read-only and layout selection.
    -   Label: Configuration for the chart's label and sidebar, such as title, subtitle, and sidebar.
    -   Value: Configuration for the chart's value settings, such as column configuration, record details, context menu options, and dependencies.
    -   Styles: Configuration for the chart's styling, such as changing the color of the timeline bar and milestones.
    -   Settings: Configuration for the chart's behavior changes. The setting section is further divided into two subsections, Grid settings and Timeline settings.
        -   Grid Settings: Configuration includes Grid section behavior changes, such as sorting and grid side width.
        -   Timeline Settings: Configuration includes Timeline section behavior changes, such as showing the current, start or end date for a project, and changing the zoom level.
    -   Advanced Control: Configuration includes advanced use case settings, such as changing scales and calendar data.
    **Note:** If all the properties are hidden in a section based on the Gantt Chart type and/or any other dependent properties, the section itself is hidden.


|Field|Property|Description|
|-----|--------|-----------|
|Read-only Gantt Chart|readonly|Option to make the Gantt Chart read-only.|
|Gantt chart layout|layout|Layout for the Gantt Chart. Available options are **Grid**, **Timeline**, and **Grid and Timeline**.|
|Hierarchy|hasHierarchy|Option to specify whether the data set has a hierarchy.|

|Field|Property|Description|
|-----|--------|-----------|
|Enable toolbar|enableToolbar|Option to activate the toolbar section.|
|Toolbar placement|toolbarPlacement|Position of the toolbar. Available options are **Top** and **Right**.|
|Help button|displayHelpButton|Option to activate the chart's help panel for instructions and shortcuts.|
|Show row count|showRowCountOnToolbar|Option to display the records count next to the toolbar title. This property is available only when the **Toolbar placement** option is set to **Top**.|
|Toolbar title|toolbarTitle|Title of the toolbar. When the **Toolbar placement** option is set to **Top**, the title of the toolbar is displayed.|
|Toolbar subtitle|toolbarSubtitle|Subtitle of the toolbar. When the **Toolbar placement** option is set to **Top**, the subtitle of the toolbar appear below the title.|

<table id="table_t1g_v5m_3wb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Gantt columns

</td><td>

columns

</td><td>

Option to configure the columns array on the table side of the Gantt Chart. Each column has its own data model. For more details, see the Columns sample snippet.Columns are the important building block for defining columns in the Gantt Chart, which are used to display tabular data on the left side of the chart.

-   `name`: Unique name of the column.
-   `label`: Title of the column shown on the header of the column.
-   `width`: Width of the column in pixel.
-   `minWidth`: Minimum width maintained for the column when resized.
-   `section`: Alignment of the columns. The available options for aligning the columns are **Center**, **Left**, and **Right**.
-   `type`: Type of the column that defines the column's behavior in terms of ad-hog operations, such as sorting, grouping, filtering, and displaying. The available options are **string**, **text**, **number**, **date**, **datetime**, **reference**, **currency**, **glide\_list**, **boolean**, **percent**, **avatar**, **avatar\_group**, **choice**, **progress**, **avatar\_select**, and **avatar\_group\_select**.
-   `timeVariantGroup`: Option to group the subcolumns \(level 2\).

Populate this field only when all columns have the same value defined in the **timeVariantGroup** and **timeVariantChild** columns. If the timeVariantGroup columns have children \(level 3\) which are common across the other timeVariant columns, you must define this property in their child columns.

-   `hidden`: Option to hide or show the column from the view.
-   `sortable`: Option to make the column sortable.
-   `hideable`: Option to make the column hideable.
-   `groupable`: Option to allow the records to be grouped by the column.
-   `editable`: Option to make the column values editable for the record.
-   `filterable`: Option to make the column filterable.
-   `isClickable`: Option to make the column clickable \(a link type\). This is applicable only for the text, string, number type of the columns.
-   `copyPaste`: Option to enable the copy and paste context menu for the columns.
-   `subColumn`: Children subcolumn for the column grouping.
-   `hideCurrencySymbol`: Option to hide the currency symbol for the column.
-   `displayCompactCurrency`: Option to display the compact format for the currency. For example, B and T \(B=Billion and T=Trillion\).
-   `enableSmartCellBackground`: Option to grey out the read-only cell.
-   `aggregation`: Aggregation criteria for the column. In case of grouping, an aggregated value is shown on the total row at the bottom if the total row is enabled.
-   `cellContextMenu`: Option to enable or disable the context menu for the column cells.
-   `enableIndicator`: Option to show the indicator icon on the columns to show extra information. For example, showing critical task, dropping cost, type of records and so on.
-   `indicatorPosition`: Position of the indicator.
-   `choices`: The extra options for the column filtering and editing if the column is of choice type. This object includes value, displayValue, color, icon, and criteria \(in case some option is of dynamic nature\).
-   `coloredFields`: Option to define cell background color if the cell need to be colored to declare some extra meaning. This object includes criteria and colorCode for color.

</td></tr><tr><td>

Record list

</td><td>

tasks

</td><td>

List of records to be shown on Gantt Chart for data model of individual task. The object must contain id, startDate, endData, and key matching with the column name. A parent key must be present and the key value must match the parent id to create a hierarchical link between the data.

Except for id and parent, all other key values must be in the format `{value: "", displayValue: ""}`, where displayValue specifies which value must be presented and the value is used internally for the calculation purpose for various column types.

To pass additional information required for the calculation or identification in multiple events and to be identified on the consumer side, record data must have a \_metadata key with the type is object.

</td></tr><tr><td>

Row context menu items

</td><td>

rowContextMenuItems

</td><td>

Options of the row context menu define the options that need to be displayed on the row context menu action button to enable extra functionality for the Gantt Chart \(such as CRUD options on cells\)

 Object structure:

-   `id`: Unique identification of the menu item.
-   `label`: Label name of the menu item.
-   `icon`: Icon of the menu item.
-   `criteria`: Criteria for which the menu item to be shown on the record. This property enables optional menu item on certain records.

</td></tr><tr><td>

Cell context menu items

</td><td>

cellContextMenuItems

</td><td>

Options for the cell context menu define the options that need to be displayed on the cell context menu action button to enable extra functionality for the Gantt Chart \(such as CRUD options on cells\).Object structure:

-   `id`: Unique identification of the menu item.
-   `label`: Label name of the menu item.
-   `icon`: Icon of the menu item.
-   `criteria`: Criteria for which the menu item to be shown on the record. This property enables the optional menu item on certain records.

**Note:** Right-clicking a cell displays the same options if the right-click context menu is enabled.

</td></tr><tr><td>

Record dependencies links

</td><td>

links

</td><td>

List of dependencies between the records.Object structure:

-   `id`: Unique identification of the dependency record.
-   `source`: ID of the task that the dependency starts from.
-   `target`: ID of the task where the dependency will end.
-   `type`: Type of the dependency. There are four types supported; finish to start \(fs\), start to finish \(sf\), finish to finish \(ff\), start to start \(ss\).

</td></tr><tr><td>

Timeline bar baselines

</td><td>

baselinesInfo

</td><td>

Baseline map for showing baseline on the timeline bar.Object structure:

-   `name`: Name of the baseline.
-   `Description`: A detailed description of the baseline.
-   `Color`: Color of the baseline on the timeline.

</td></tr><tr><td>

Timeline start date

</td><td>

startDate

</td><td>

Start date of the project's timeline.

</td></tr><tr><td>

Timeline end date

</td><td>

endDate

</td><td>

End date of the project's timeline.

</td></tr><tr><td>

Holidays dates

</td><td>

holidays

</td><td>

List of holidays with dates.

</td></tr><tr><td>

Weekends

</td><td>

weekends

</td><td>

Days of the week that are considered as weekends.

</td></tr><tr><td>

Custom legend items to be shown in legend panel

</td><td>

customLegendItems

</td><td>

Option to manage the list of custom legend items to be shown in the legend side panel.

</td></tr></tbody>
</table>-   **Columns sample snippet**

    ```
    [
      {
        "label": "Name",
        "name": "text",
        "type": "text",
        "resize": true,
        "hidden": false,
        "hideable": false,
        "cellContextMenu": true,
        "editable": true
      },
      {
        "label": "Priority",
        "name": "priority",
        "type": "number",
        "hidden": false,
        "editable": true
      },
      {
        "label": "Story Points",
        "name": "story_point",
        "type": "number",
        "hidden": false,
        "editable": true,
        "aggregation": {
          "aggregateType": "SUM"
        }
      },
      {
        "label": "Start Date",
        "name": "startDate",
        "type": "date",
        "hidden": false,
        "editable": true
      },
      {
        "label": "End Date",
        "name": "endDate",
        "type": "date",
        "hidden": false,
        "editable": true
      }
    ]
    
    ```

-   **Records sample snippet**

    ```
    [{
        "id": "1bc72a0bdb8c881025c85a35dc9619d3",
        "text": {
          "value": "Workday to Payroll Automation",
          "displayValue": "Workday to Payroll Automation"
        },
        "number": {
          "value": "PRJ0010009",
          "displayValue": "PRJ0010009"
        },
        "parent": null,
        "startDate": {
          "value": "2019-07-22 02:30:00",
          "displayValue": "2019-07-22 02:30:00"
        },
        "endDate": {
          "value": "2020-03-28 00:00:00",
          "displayValue": "2020-03-28 00:00:00"
        },
        "state": {
          "value": "Draft",
          "displayValue": "Draft"
        }
      },
      {
        "id": "1ec797a2dbd80010f777526adc961980",
        "text": {
          "value": "Planning",
          "displayValue": "Planning"
        },
        "number": {
          "value": "PRJTASK0010131",
          "displayValue": "PRJTASK0010131"
        },
        "parent": "1bc72a0bdb8c881025c85a35dc9619d3",
        "startDate": {
          "value": "2019-09-10 15:00:00",
          "displayValue": "2019-09-10 15:00:00"
        },
        "endDate": {
          "value": "2019-11-25 16:00:00",
          "displayValue": "2019-11-25 16:00:00"
        },
        "state": {
          "value": "Draft",
          "displayValue": "Draft"
        }
      }]
    
    ```


|Field|Property|Description|
|-----|--------|-----------|
|Bar style config|barStyles|Option to set the bar's style and color as required.|
|Enable colorBy feature|enableColorBy|Option to enable color-by feature for Gantt Chart.|
|Color-by column|colorByColumn|Option to specify on which column the color-by feature should be enabled on.|
|Color-by field map|colorByMap|Map of the column value to its respective timeline bar color.|

|Field|Property|Description|
|-----|--------|-----------|
|Sort by|sortBy|Option to sort the records' data by column and order.|
|Grid width \(%\)|gridWidth|Table side width in percentage.|
|Row height \(pixel\)|rowHeight|Row height in pixels.|
|Enable reorder columns|enableReorderColumns|Option to enable the drag and drop feature for rearranging the columns.|
|Row group|rowGroup|Option to enable the grouping feature.|
|Enable columns pinning|enableColumnsPinning|Option to allow the user to pin the required columns to the left or right side.|
|Enable row selection checkbox|enableRowSelectionCheckbox|Option to show the row selection check box to select multiple rows at the same time.|
|Enable preview record icon|enablePreviewRecordIcon|Option to enable the preview record button to view the record details outside of the Gantt Chart.|
|Enable reorder row|enableReorderRows|Option to reorder rows to change the parent, rank, or other properties.|
|Reorder row label source column|reorderRowsLabelSourceColumn|Specifies which column values should be visible when reordering the rows.|
|Enable reset column options|enableResetColumns|Option to reset the column changes from the default.|
|Enable cell context menu on right-click|enableCellContextMenuOnRightClick|Option to enable the right-click cell context menu.|
|Enable drag to reorder columns|enableDragToReorderColumns|Option to enable drag and drop feature for reordering a column.|
|Display child task count|displayChildTasksCount|Option to display the child count in the primary column.|
|Enable context menu icon on rows|enableRowContextMenu|Option to display the context menu icon on the row.|
|Manage column show hide feature|manageColumnShowHide|Option to display or hide the columns for lazy data loading when a user changes the column configuration.|
|Apply records filter on grid on load|recordsFilter|An encoded query to filter grid when it is loaded for the first time.|
|Manage column personalization|manageColumnPersonalization|Option to manage the display of Gantt Chart's view when you click the personalize column action.|

<table id="table_y2h_hvm_3wb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date format

</td><td>

dateFormat

</td><td>

Date format for the timeline section.

</td></tr><tr><td>

Date time format

</td><td>

dateTimeFormat

</td><td>

Date and time format for the timeline section.

</td></tr><tr><td>

Timezone for current date

</td><td>

timeZone

</td><td>

Timezone of the current user.

</td></tr><tr><td>

Week starts on

</td><td>

weekStartsOn

</td><td>

Day the week starts on.

</td></tr><tr><td>

Show current date on Timeline

</td><td>

showCurrentTimeLine

</td><td>

Displays a straight line for the current date in the timeline section.

</td></tr><tr><td>

Show start and end of Timeline

</td><td>

showStartEndTimeline

</td><td>

Option to show the project's start and end time on the timeline.

</td></tr><tr><td>

Show label on timeline bar

</td><td>

showBarLabel

</td><td>

Option to show the record label on the timeline bar.

</td></tr><tr><td>

Can move task

</td><td>

canMoveTask

</td><td>

Option to reposition the tasks to alter the start and end dates.This property is available only when the **Configuration type** option is set to **Essential**.

</td></tr><tr><td>

Can resize task

</td><td>

canResizeTask

</td><td>

Option to resize the tasks to change their duration.This property is available only when the **Configuration type** option is set to **Essential**.

</td></tr><tr><td>

Can show baselines

</td><td>

canShowBaselines

</td><td>

Option to show the baseline on the timeline.

</td></tr><tr><td>

Show baseline toggle

</td><td>

showBaselinesToggle

</td><td>

Option to show baseline toggle on the setting panel.

</td></tr><tr><td>

Can create dependency

</td><td>

canCreateDependency

</td><td>

Allows users to create dependencies between tasks on the timeline bar.This property is available only when the **Configuration type** options is set to **Essential**.

</td></tr><tr><td>

Show switch layout

</td><td>

showSwitchLayout

</td><td>

Option to enable switching the layout.

</td></tr><tr><td>

Can show critical path

</td><td>

canShowCriticalPath

</td><td>

Option to show the critical path on the timeline.

</td></tr><tr><td>

Allowed dependency type

</td><td>

allowedDependencyTypes

</td><td>

Option to specify which dependency types can be created. For example, start to finish, finish to start, and so on.

</td></tr><tr><td>

Timeline zoom level

</td><td>

zoomLevel

</td><td>

Option to provide the timeline's default zoom level. The available options are **Day**, **Week**, **Month**, **Quarter**, **Year**, and **Autofit**.

</td></tr><tr><td>

Display an additional timeline unit while resize

</td><td>

displayAdditionalTimelinesUnit

</td><td>

Option to add more timeline units when the timeline is resized if required, keeping the width of each bottom unit fixed. Otherwise, the timeline base unit is modified while the start and end remain fixed.

</td></tr><tr><td>

Timeline popover config

</td><td>

timelinePopoverConfig

</td><td>

Option to set the necessary information for the timeline bar pop over.

</td></tr><tr><td>

Baseline popover config

</td><td>

baselinePopoverConfig

</td><td>

Option to set the necessary information for the baseline bar pop over.

</td></tr><tr><td>

Show critical path

</td><td>

showCriticalPath

</td><td>

Task dependencies that conflict are displayed as a critical path in the timeline section.

</td></tr><tr><td>

Enable timeline indicator

</td><td>

enableTimelineIndicator

</td><td>

Option to enable indicators on the timeline bar.

</td></tr><tr><td>

Show external task dependencies

</td><td>

showExternalDependency

</td><td>

Option to display the external tasks in the Gantt Chart. The external tasks aren’t directly related to the project or activity being managed by the Gantt Chart, but these tasks may have an impact on the progress or completion of the project.

</td></tr><tr><td>

Show Help panel

</td><td>

displaySettingsHelpPanel

</td><td>

Option to show a help panel for settings.

</td></tr><tr><td>

Task layers

</td><td>

taskLayers

</td><td>

Phases of tasks that are displayed on top of the timeline bar.

</td></tr></tbody>
</table>|Field|Property|Description|
|-----|--------|-----------|
|Settings primary panel|settingsPrimaryPanel|Option to set the primary panel to swap the Timeline and Columns locations using the personalize toolbar.|
|Zoom level options|zoomLevelOptions|Configurations that could be made to the timeline's zoom levels to add more levels of zoom.|
|Calendar data|calendarData|If the calendar data is available, a gantt chart will be plotted using calendar data to show the user supplied calendar, such as fiscal or PI period.|
|Show side panel|showSidePanel|Option to show the side panel.|
|Selected side panel to open|selectedSidePanel|Option to choose which side panel to be opened. The available options are **Settings Panel** and **Help Panel**.|

-   **Gantt Chart dynamic properties**

    Some of the properties appear based on the specific values in dependent properties. Some of these properties are listed below.

    -   If the readOnly property is disabled, the following properties are available for configuration:
        -   canMoveTask
        -   canResizeTask
        -   canCreateDependency
        -   displayAddTaskBelowinTimeline
        -   displayIndentinTimeline
    -   If the toolbar is enabled and the placement is set to top, the following properties are available for configuration:
        -   toolbarTitle
        -   toolbarSubtitle
        -   showRowCountOnToolbar

### What is the criteria and how to write one

Criteria are conditional sentences on task objects that combine several statements to filter out eligible tasks and apply conditional options, such as cell coloring, context menu addition, and read-only cells.

Format for the statements is `<fieldname><comparison><value>`

Criteria are multiple statements combined like `<statement1><combination operator><statement2>…`

Comparison can be `=, >, <, >=, <=` with literal mathematically meanings.

Only And is supported as combination operator and can be used as using `^` symbol.

For example, “`state.value=Draft`” on example list of tasks.

## Gantt Chart component events

Select event handlers to configure the events provided with the Gantt Chart component. Event handlers work with data resources to link the Gantt Chart actions to the data you want to display to your users.

The Events tab shows the events used by the Gantt Chart component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Gantt Chart actions to the data you want to display to your users. Expand the event in the list and add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|NOW\_GANTT\#GRID\_RESIZED|Action dispatched when the Grid panel is resized.|
|NOW\_GANTT\#TIMELINE\_ZOOM\_CHANGED|Action dispatched when the timeline zoom level is changed \(for example, day to month\).|
|NOW\_GANTT\#LINK\_ADDED|Action dispatched when a dependency is created.|
|NOW\_GANTT\#LINK\_CLICKED|Action dispatched when you click the dependency link.|
|NOW\_GANTT\#LINK\_MOUSEOVER|Action dispatched when you mouse over on a dependency link.|
|NOW\_GANTT\#LINK\_MOUSEOUT|Action dispatched when you mouse out on a dependency link.|
|NOW\_GANTT\#LINK\_RIGHT\_CLICKED|Action dispatched when you right-click the dependency link.|
|NOW\_GANTT\#LINK\_DELETE\_REQUESTED|Action dispatched when there’s a backspace key up event on the timeline-links.|
|NOW\_GANTT\#TASK\_MOVED|Action dispatched when the task moved from one location to another.|
|NOW\_GANTT\#TASK\_RESIZED|Action dispatched when the task bar is resized.|
|NOW\_GANTT\#TASK\_BAR\_RIGHT\_CLICKED|Action dispatched when you right-click the task bar.|
|NOW\_GANTT\#TASK\_BAR\_CLICKED|Action dispatched when you click the task bar.|
|NOW\_GANTT\#COLUMNS\_UPDATED|Action dispatched when one of the properties, widths, hidden, section, order of one or more than one column is changed.|
|NOW\_GANTT\#SORT\_CHANGED|Action dispatched when the sort order or sorting column is changed.|
|NOW\_GANTT\#FILTER\_CHANGED|Action dispatched when the column filter is changed.|
|NOW\_GANTT\#ROW\_EDIT\_STARTED|Action dispatched when editing is enabled with the rowEdit and editMode options, and the cell is double-clicked.|
|NOW\_GANTT\#PREVIEW\_RECORD\_ICON\_CLICKED|Action dispatched when you click the Preview icon.|
|NOW\_GANTT\#ROW\_SELECTED\_SET|Action dispatched when the row selection is toggled.|
|NOW\_GANTT\#ALL\_ROWS\_SELECTED|Action dispatched when all rows are selected.|
|NOW\_GANTT\#ALL\_ROWS\_UNSELECTED|Action dispatched when all rows are unselected.|
|NOW\_GANTT\#DISPLAY\_BAR\_LABELS|Action dispatched when setting for the display bar label is toggled|
|NOW\_GANTT\#ROW\_EXPAND\_SET|Action dispatched when the row expansion is changed.|
|NOW\_GANTT\#ALL\_ROWS\_EXPANDED|Action dispatched when you click **Expand all**.|
|NOW\_GANTT\#ALL\_ROWS\_COLLAPSED|Action dispatched when you click **Collapse all**.|
|NOW\_GANTT\#DISPLAY\_DEPENDENCY\_LINES|Action dispatched when setting for the display dependency lines is toggled.|
|NOW\_GANTT\#COLUMNS\_RESET|Action dispatched when you click **Reset columns**.|
|NOW\_GANTT\#TASKS\_PASTED|Action dispatched after pasting the copied values.|
|NOW\_GANTT\#ROW\_ORDER\_CHANGED|Action dispatched after reordering the rows.|
|NOW\_GANTT\#INSERT\_COPIED\_ROWS|Action dispatched when you click **Insert copied rows** after copying the rows.|
|NOW\_GANTT\#TIMELINE\_INDENT\_TASK\_REQUESTED|Action dispatched when you click the Indent task icon in the timeline.|
|NOW\_GANTT\#ROW\_CONTEXT\_MENU\_ITEM\_CLICKED|Action dispatched when you click the Row context menu item.|
|NOW\_GANTT\#CELL\_CONTEXT\_MENU\_ITEM\_CLICKED|Action dispatched when you click the Cell context menu item.|
|NOW\_GANTT\#RECORD\_UPDATED|Action dispatched when a record or task is updated.|
|NOW\_GANTT\#TIMELINE\_ZOOM\_IN\_CHANGED|Action dispatched when the timeline zoom in changed.|
|NOW\_GANTT\#CRITICAL\_PATH\_VISIBILITY\_CHANGE\_REQUESTED|Action dispatched when critical path visibility changes are requested.|
|NOW\_GANTT\#LAYOUT\_CHANGED|Action dispatched when layout is changed from side panel.|
|NOW\_GANTT\#CLOSE\_SIDEPANEL|Action dispatched when the settings and help side panel is closed.|
|NOW\_GANTT\#OPEN\_SIDEPANEL|Action dispatched when the settings and help side panel is opened.|
|NOW\_GANTT\#TIMELINE\_ADD\_TASK\_BELOW\_REQUESTED|Action dispatched when you click the Add task icon bellow the timeline bar.|
|NOW\_GANTT\#CELL\_SELECTED|Action dispatched when you select a Gantt chart's cell.|
|NOW\_GANTT\#TASK\_DATA\_UPDATED|Action dispatched when the task data updated using editing.|
|NOW\_GANTT\#TEXT\_LINK\_CLICKED|Action dispatched when you click content that is of link type.|
|NOW\_GANTT\#COLUMNS\_CONFIG\_UPDATED|Action dispatched when column show hide is managed and user changes the column configuration.|
|NOW\_GANTT\#PERSONALIZE\_COLUMN\_REQUESTED|Action dispatched when personalize column action is requested from the header context menu.|
|NOW\_GANTT\#COLUMN\_HIDE\_REQUESTED|Action dispatched when hide columns action is performed from the header context menu.|
|NOW\_GANTT\#CELL\_CLICKED|Action dispatched when you click any cell.|
|NOW\_GANTT\#CELL\_BLURRED|Action dispatched when you blur any cell.|

