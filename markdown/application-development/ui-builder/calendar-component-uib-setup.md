---
title: Calendar component setup
description: The Calendar component enables you to visualize time related events in various calendar views.Configure the appearance and the contents of the Calendar component.Select event handlers to configure the events provided with the Calendar component. Event handlers work with data resources to link the Calendar actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/calendar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 18
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Calendar component setup

The Calendar component enables you to visualize time related events in various calendar views.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Calendar that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "calendar-content-tree.png"\] Alt text: Shows the calendar component in the content tree in UI Builder with the content slots collapsed

2.  Select the Calendar component, using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appears in the panel on the right.

    \[Omitted image "calendar-config-panel.png"\] Alt text: Shows the config panel for the Calendar component


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Calendar component properties

Configure the appearance and the contents of the Calendar component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_pb2_ybf_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Events\[events\]

</td><td>

Array of events to display on the calendar.Object properties:

-   `id`: Unique identifier for the event
-   `title`: Event title
-   `description`: Event description
-   `bgColor`: The background color to use for the event. Accepts color names, hex code, or theme variables like `--now-color_selection--primary-2`.
-   `start`: Event's start date. Supports UTC MS, GlideDate, and ISO date formats.
-   `end`: Event's end date. Supports UTC MS, GlideDate, and ISO date formats.
-   `startMS`: Start time in milliseconds.
-   `endMS`: End time in milliseconds.
-   `gradientColor1`: Color of striped pattern to use. Accepts color names, hex codes, or theme variables.
-   `gradientColor2`: Color of second striped pattern to use. Accepts color names, hex codes, or theme variables.
-   `childEvents`: Configuration of events within a parent event. Supported in timeline-based views.
    -   `title`: Child event title.
    -   `additionalProperties`: Additional properties for the child event like `bgColor`, `description`, `start`, and `end`.
-   `contextMenuOptions`: List of additional event-related options. This context menu appears when the user right-clicks the event.
    -   `id`: Unique identifier for the context menu option.
    -   `label`: Menu option text.
    -   `disabled`: To disable the menu option, set to **true**.
-   `order`: The order in which to display the event in case there are overlapping events. Higher value takes priority.
-   `group`: The category in which to place the event. Group name must match the section ID in timeline sections.

Default:

```json
[
    {
        "id": "0",
        "title": "Demo day - Right click for context menu",
        "description": "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It ha",
        "bgColor": "nds-orange",
        "start": "2024-02-08 04:00:01",
        "end": "2024-02-08 18:00:00",
        "startMS": 1707364801000,
        "endMS": 1707415200000,
        "childEvents": [
            {
                "title": "ITSM",
                "bgColor": "#78b0cc",
                "start": "2024-02-08 07:30:01",
                "end": "2024-02-08 09:45:00",
                "startMS": 1707377401000,
                "endMS": 1707385500000
            },
            {
                "title": "ITBM",
                "bgColor": "#ecdf93",
                "start": "2024-02-08 11:15:01",
                "end": "2024-02-08 12:45:00",
                "startMS": 1707390901000,
                "endMS": 1707396300000
            },
            {
                "title": "CSM",
                "bgColor": "#28b353",
                "start": "2024-02-08 14:00:01",
                "end": "2024-02-08 16:00:00",
                "startMS": 1707400801000,
                "endMS": 1707408000000
            }
        ],
        "contextMenuOptions": [
            {
                "id": "e2_li1"
            },
            {
                "id": "e2_li2"
            },
            {
                "id": "e2_li3"
            },
            {
                "id": "e2_li4",
                "disabled": true
            },
            {
                "id": "e2_li5"
            }
        ],
        "order": 3000,
        "group": "Hardware"
    },
..
..
{
        "id": "40",
        "title": "Event 22",
        "start": "2024-02-15 00:00:00",
        "end": "2024-02-16 00:00:00",
        "startMS": 1707955200000,
        "endMS": 1708041600000,
        "group": "Hardware"
    },
    {
        "id": "event-four",
        "title": "2 Day event",
        "bgColor": "rgb(255, 51, 51)",
        "start": "2024-02-08 00:00:01",
        "end": "2024-02-08 23:59:59",
        "startMS": 1707350401000,
        "endMS": 1707436799000,
        "gradientColor1": "rgb(14, 120, 196)",
        "gradientColor2": "rgb(104, 171, 218)"
    }
]
```

</td></tr><tr><td>

Popover enabled\[popoverEnabled\]

</td><td>

Enables property when the popover content opens on an event click.

</td></tr><tr><td>

Popover content state\[PopoverContentState\]

</td><td>

Set to ready when popover content is ready in the slot.

</td></tr><tr><td>

Focused event ID\[focusedEventId\]

</td><td>

ID of the event to auto focus on in the view.

</td></tr><tr><td>

External event\[externalEvent\]

</td><td>

Event information dragged from an external source to calendar.

</td></tr><tr><td>

Enable new button\[enableNewButton\]

</td><td>

Shows a new button on the header.

</td></tr><tr><td>

Security\[security\]

</td><td>

Calendar global security choices.-   `readOnly`: Makes the calendar read only with no edit options. Default is **false**.

**Note:** Select is always enabled.

-   `allowCreate`: Enables creating event. Default is **true**.
-   `allowMove`: Enables moving an event. Default is **true**.
-   `allowResize`: Enables resizing an event. Default is **true**.

</td></tr></tbody>
</table><table id="table_ztx_qzb_twb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available views\[availableViews\]

</td><td>

Array of required views as strings.

</td></tr><tr><td>

Current view\[currentView\]

</td><td>

Current selected view.

</td></tr><tr><td>

View settings\[viewSettings\]

</td><td>

Configures view attributes. Attributes supported by all the views include: DAY, WEEK, COLUMN, TIMELINE\_DAY, TIMELINE\_WEEK.-   `hideAgendaView`: Visibility of the Agenda view. When **true** hides Agenda view from contextual panel.
-   `snapGranularity`: Number of minutes that events are moved. Defaults are TIMELINE\_DAY **15** and TIMELINE\_WEEK **480**.
-   `splitRow`: Number of sub grid rows or columns the base view provider is based on. The default value is **2** attributes supported by DAY, WEEK, and COLUMN views.

 Attributes supported by the COLUMN \(Base view provider on which DAY and WEEK are based\).

 -   `timeRowSpan`: Time scale in minutes. The default value is **60**, 24 markers of 1 hour each are seen on the time scale.
-   `numberOfDays`: Number of days to be shown from first day of the week. DAY view default is **1**. WEEK view default is**7**.
-   `firstDayOfWeek`: First day of the week as number 0 through 6, where 0 is Sunday, 1 is Monday, 2 is Tuesday, and so on. Default is **0** \(Sunday\).
-   `minEventRowHeight`: Assigns the minimum height for the event row in pixels. Can be as low as **24** pixels. Default is **50** pixels.

 Attributes supported by TIMELINE\_DAY, TIMELINE\_WEEK.

 -   `groupBy`: Assigns a grouping attribute to an event. Events with the same `groupBy` value are displayed in the same row. Default is `group`. Other options are any values defined for the events `group` property; the default grouping identifier for the event.
-   `animation`: Enables animation while rendering events. The default value is **false** \(disables\).
-   `noScrolling`: Enables scrolling. When **true**, the columns in a calendar try to fit in the viewable area and disable the ability to scroll horizontally. Default is **false**.
-   `eventHeight`: Assigns height of calendar events in pixels. Assign initial height or dynamically change the height of all the events. Can be between **20** pixels and **100** pixels unless you change using the `minEventHeight` and `maxEventHeight`. Default is **20** pixels.
-   `minEventHeight`: Assigns the minimum height of calendar events in pixels. Can be as low as **1** pixel. Default is **20** pixels.
-   `maxEventHeight`: Assigns the maximum height of calendar events in pixels. Can be as high as **500** pixel. Default is **100** pixels.
-   `sectionHeaderHeight`: Assigns the height of the section header in pixels. The minimum value is **0** pixels. There's no maximum value. Default is **40** pixels.
-   `titleWidth`: Specifies the width of the section title in pixels. The minimum value is **0**. There's no maximum value. Default is **240** pixels.
-   `minimumEventSpan`: Controls the minimum width \(in milliseconds \(ms\)\) of the event pixels shown on event hover.
-   `templates`: Specifies the key value pair of templates to be rendered inside the TIMELINE view. Each key is an object of type `{ type : 'component' | 'macroponent', value: string}`.

For component, the value should be seismic component and should present in `sys_ux_macroponent`.

For macroponent, the value should be a valid `sys_id` of macroponent.

Valid keys are: `mainGrid`, `timeScaleGrid`, `sectionHeadTitle`, `sectionHeadBody`, `rowTitle`, `rowBody`, and `eventBody`.


</td></tr></tbody>
</table>An example payload:

`{ mainGrid: { type: 'component', value: "sn-now-calendar-demo-timeline-main-grid-template" }, timeScaleGrid: { type: 'component', value: 'sn-now-calendar-demo-timeline-header-view' }, sectionHeadTitle: { type: 'component', value: 'sn-now-calendar-demo-timeline-section-title' }, sectionHeadBody: { type: 'component', value: 'sn-now-calendar-demo-timeline-section-head-body' }, rowTitle: { type: 'component', value: 'sn-now-calendar-demo-timeline-row-head-imgs' }, rowBody: { type: 'macroponent', value: '8326c59290879050f8774b0ebd42e4b3' }, eventBody: { type: 'component', value: "sn-now-calendar-demo-timeline-event-body" } }`

<table id="table_zxq_fdf_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View settings \(continued\)\[viewSettings\]

</td><td>

Attributes supported by TIMELINE\_DAY, TIMELINE\_WEEK.

 `timeRowSpan`: Time duration for each column in minutes. In the TIMELINE\_DAY view, the minimum value is `5` minutes. In the TIMELINE\_WEEK view, the minimum value is `1`day. In Timeline configurable views, the minimum is `1` day or if xUnitName is defined, then 1 xUnitName unit and there's no limit on maximum value. Default is `60` minutes.

 Attribute supported by DAY, WEEK, WORK\_WEEK, and MONTH.

 `timeRowSpan`: Time duration for each column in minutes. The minimum value is `1` minute. The maximum value is `1440` minutes. The only condition is `(86400/60) % timeRowSpan === 0`

 Attributes supported by TIMELINE\_DAY, TIMELINE\_WEEK, and TIMELINE\_CONFIGURABLE\_COLUMN.

 `xStep`: Follows the same rules as `timeRowSpan`. Numerical value in interval, for which time scale should be drawn.

 -   `xSize`: Number of intervals in the given time scale. For DAY view, it's set to `1` day and no restrictions for other views.
-   `xStart`: Numerical value at which the interval scale starts. Default is `0` and there are no restrictions on maximum value.

</td></tr></tbody>
</table>Example:

`{\"DAY\":{\"snapGranularity\":15,\"splitRow\":2},\"WEEK\":{\"snapGranularity\":15,\"splitRow\":2},\"work_week\":{\"numberOfDays\":5,\"snapGranularity\":15,\"splitRow\":2},\"TIMELINE_DAY\":{\"animation\":false,\"groupBy\":\"group\",\"snapGranularity\":15,\"splitRow\":2,\"timeRowSpan\":60},\"TIMELINE_WEEK\":{\"animation\":false,\"groupBy\":\"group\",\"snapGranularity\":480,\"splitRow\":3},\"TIMELINE_MONTH\":{\"hideSidebarOnLoad\":true,\"columnUnit\":\"weeks\",\"columnTimeframe\":1,\"columnsCount\":4,\"noScrolling\":false,\"enableColumnNavigation\":true,\"viewLabel\":\"4 Weeks\"}}`

<table id="table_unz_y1c_twb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Mark spans\[markSpans\]

</td><td>

Array of indicators on the Calendar region where the use case indicates something special. This property can also be blocked for event operations.

</td></tr><tr><td>

Split multi day event\[splitMultiDayEvent\]

</td><td>

Specifies whether a multi-day event is always shown in the week or month view of the Calendar.

</td></tr><tr><td>

Timeline sections\[sections\]

</td><td>

Array of timeline section objects.Required attributes:

 -   `id`: Unique identifier for a section.
-   `title`: Title of the section.
-   `showHeader`: Header display for the section. The default value is **true**, show the header.
-   `isCollapsed`: State of section header.

Default value: **false**

-   `bgColor`: Background color of the section. Format can only be HEX code.
-   `textColor`: Color of text of the section. Format can only be HEX code.
-   `children`: Child sections containing the section details.

</td></tr><tr><td>

Timeline vertical lines\[timelineVerticalLines\]

</td><td>

Dates where vertical lines are to be drawn on a timeline. -   `utcMS`: Date in UTC milliseconds.
-   `inlineStyle`: Inline style attributes applicable to an HTML div in camel case.

</td></tr></tbody>
</table><table id="table_kd5_33f_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Context date\[contextDate\]

</td><td>

Selected date on the calendar.

</td></tr><tr><td>

Available timezones\[availableTimezones\]

</td><td>

Time zones available.

</td></tr><tr><td>

Time zone\[timezone\]

</td><td>

Name of timezone where events are shown.

</td></tr><tr><td>

Time format\[timeFormat\]

</td><td>

Time display format option.

</td></tr><tr><td>

Locale\[locale\]

</td><td>

Applicable locale. The accepted values are moment locales. Complete translation on an instance is achieved by moment locale and translations together.The following value map provides the language code mapping to moment locale language code:

 `{"en":"en", "es": "es", "it": "it", "et": "et", "zt": "zh-cn", "xl": "x-pseudo", "fi": "fi", "pb": "pt-br", "pl": "pl", "fr": "fr", "ko": "ko", "pt": "pt", "ja": "ja", "ru": "ru", "tr": "tr", "zh": "zh-cn", "sv": "sv", "he": "he", "nb": "nb", "hu": "hu", "cs": "cs", "de": "de", "th": "th", "fq": "fa-ca", "nl": "nl"}`

</td></tr><tr><td>

Date picker templates\[datePickerTemplates\]

</td><td>

Template for date picker that replaces the default content.

</td></tr><tr><td>

First day of week\[firstDayOfWeek\]

</td><td>

First day of the week represented as an integer. For example, 0-Sunday, 1-Monday, or 6-Saturday. Default: **0-Sunday**.

</td></tr><tr><td>

Date format\[dateFormat\]

</td><td>

Date display format option.Default: **YYYY-MM-DD**

</td></tr><tr><td>

Agenda view date format\[agendaViewDateFormat\]

</td><td>

Agenda view date format option.Default: **ddd, MMM D**

Example: Wed, Apr 3

</td></tr></tbody>
</table><table id="table_epw_flf_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contextual panel items\[contextualPanelItems\]

</td><td>

Custom actionable icons to appear on the calendar flyer.

</td></tr><tr><td>

Manage contextual panel open/close behavior\[manageContextualPanel\]

</td><td>

When set to **true**, overrides the default opening/closing behavior of the contextual panel.Default: **false**

</td></tr><tr><td>

Configuration aria\[configAria\]

</td><td>

Aria label of the calendar.-   `ariaTitle`: Aria title for the calendar.
-   `ariaBodyTitle`: Aria title for the section below the header.

</td></tr><tr><td>

Customizable labels\[customizableLabels\]

</td><td>

Custom calendar labels.

</td></tr><tr><td>

Hide keyboard shortcuts\[hideKeyboardShortcuts"\]

</td><td>

When set to **true**, keyboard shortcuts are hidden.Default: **false**

</td></tr><tr><td>

Hotkeys\[hotkeys\]

</td><td>

Array of custom hot keys for the Calendar section.-   `eventName`: Unique identifier for the event.
-   `selector`: CSS selector to identify the event.
-   `keyCode`: Integer ASCII code of the Key.
-   `view`: View where this selector is applicable.
-   Next key: `{keyName: string, description: string}`Next and Previous keys and their description.
-   Previous key: `{keyName: string, description: string}`

</td></tr><tr><td>

Mutlicolumn config\[multiColumnConfig\]

</td><td>

Available in the timeline views. JSON object with the configuration of the columns in the left-side of the timeline view. Supports maximum three columns.Object properties:

-   `width`: Width of all columns as a percentage of the total calendar's width. Must be a number.
-   `column`: Array with configuration of individual columns' width relative to the other columns that are part of the multiple column configuration.
    -   `width`: Width of the column relative to the other additional columns in the multiple column configuration as a percentage. These must add up to 100.
    -   `minWidth`: Minimum width of the column to maintain during screen or calendar resizing as pixels. Uses 30px as default if not specified.

Default value: \{\}

Example:

```json
{
	width: 20, 
	columns: [
		{width: 30, minWidth: 10},
		{width: 40, minWidth: 15},
		{width: 30}
	]
}
```

Based on the example above, if the calendar width is 1000px:

-   The total width of all the left columns combined is 20% of the calendar's width: 200px.
-   The first column's width is 30% of the total space allocated to the left columns, that is 60px, and minimum width is 10px.
-   The second column's width is 40% of the total space allocated to the left columns, that is 80px, and minimum width is 15px.
-   The third column's width is 30% of the total space allocated to the left columns, that is 60px; there is no minimum width so the default 30px is used

**Note:** Use this property to configure the relative width of the columns, width of each column, and the minimum width. To configure the information displayed in these columns, configure the slots **title-column-1**, **title-column-2**, and **title-column-3** in the UIB panel.

</td></tr><tr><td>

Hide header\[hideHeader\]

</td><td>

To hide the calendar header, set to **true**.Default: **false**

</td></tr><tr><td>

Hide settings\[hideSettings\]

</td><td>

To hide the settings button in the calendar header, set to **true**. Calendar settings include options to add multiple timezones and keyboard shortcuts.Default: **false**

</td></tr><tr><td>

Enable new calendar click\[enableNewCalendarClick\]

</td><td>

Option to enable click events on calendar views.

</td></tr></tbody>
</table>## Calendar component events

Select event handlers to configure the events provided with the Calendar component. Event handlers work with data resources to link the Calendar actions to the data you want to display to your users.

The Events tab shows the events used by the Calendar component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

\[Omitted image "calendar-events.png"\] Alt text: Shows a partial list of the events included with the Calendar component in UI Builder

### Event handlers

Event handlers work with data resources to link the Calendar actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_lhc_sgr_nnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional timezone added/removed

</td><td>

Action that is dispatched when additional timezones are selected or deselected.Payload: An array with the `value` and `displayValue` of the timezones selected or deselected.

</td></tr><tr><td>

Calendar initialized

</td><td>

Action that is dispatched when Calendar is initialized.

</td></tr><tr><td>

Context date changed

</td><td>

Action that is dispatched when the current selected date changes on the Calendar.Payload:

-   `fromMS`: Old selection date in UTC milliseconds.
-   `toMS`: New selection date in UTC milliseconds.

</td></tr><tr><td>

Contextual panel view selected

</td><td>

Action that is dispatched when one of the icons in flyer is selected.Payload includes: `viewId`: Contextual panel view that's displayed. This is tied to the id attribute set in property contextualPanelItems.

</td></tr><tr><td>

Drag end for new event

</td><td>

Action that is dispatched when a drag operation to create a new event ends.Payload:

-   `startDateMS`: Start date of event creation requested in UTC milliseconds.
-   `endDateMS`: End date of event creation requested in UTC milliseconds.
-   `group`: Section id where the event belongs.
-   `dragDistance`: Distance in milliseconds for which the new event was dragged.

</td></tr><tr><td>

Event clicked

</td><td>

Action that is dispatched when an event is selected.Payload:

-   `event`: Event object that is selected.
-   `chunkStartDateMS`: If an event is split, the start date part of the event selected in UTC milliseconds.
-   `chunkEndDateMS`: If an event is split, the end date part of the event selected, in UTC milliseconds.

</td></tr><tr><td>

Event context menu item selected

</td><td>

Action that is dispatched when user presses and holds an empty cell or an event and selects an item from the drop-down. Payload:

-   `item`: One of the item objects passed in `event.contextMenuOptions`.
-   `event`: Event which the user selected.
-   `row`: Information of the selected row as an object.
-   `timestamp`: Time stamp at which the empty cell was selected.

**Note:** When the user performs this operation on an event, `row` and `timestamp` in the payload are null. When the user performs this operation on an empty cell, `event` is null.

</td></tr><tr><td>

Event double clicked

</td><td>

Action that is dispatched when a calendar grid is selected to create a new event.Payload:

-   `newStartMS`: Start date of event requested, in UTC milliseconds.
-   `newEndMS`: End date of event requested, in UTC milliseconds.
-   `group`: Section id where the event belongs.

</td></tr><tr><td>

Event moved

</td><td>

Action that is dispatched when an event is moved via a drag operation.Payload:

-   `event`: Event object that's being moved.
-   `difference`: Difference in milliseconds to current position. Can be negative or positive.
-   `newStartMS`: New start date in UTC milliseconds.
-   `newEndMS`: New end date in UTC milliseconds.
-   `group`: New section id where the event belongs that is populated in case of grouped timeline.

</td></tr><tr><td>

Event operation rejected by blocked span

</td><td>

Action that is dispatched when blocked span rejects drag or re-size operation.Payload:

-   `causingBlockedSpan`: Definition causing the rejection.
-   `event`: Event that was rejected.
-   `occurrenceDateStartMS`: Start date of the blocked span instance in UTC milliseconds.
-   `occurrenceDateEndMS`: End date of the blocked span instance in UTC milliseconds.
-   `operation`: Type of operation that was rejected. For example, move, re-size, or create.

</td></tr><tr><td>

Event resized

</td><td>

Action that is dispatched when the start or end dates of an event are changed by resizing.Payload:

-   `event`: Event object that's being re-sized.
-   `startDateMS`: Start date of event after re-size in UTC milliseconds.
-   `endDateMS`: End date of event after re-size in UTC milliseconds.

</td></tr><tr><td>

Generic template event

</td><td>

Generic event dispatched by child component.

</td></tr><tr><td>

Grid clicked for new event

</td><td>

Action that is dispatched when a Calendar grid is selected for new event creation.Payload:

-   `startDateMS`: Start date of event creation requested in UTC milliseconds.
-   `endDateMS`: End date of event creation requested in UTC milliseconds.
-   `group`: Section id where the event belongs.

</td></tr><tr><td>

Grid double clicked

</td><td>

Action that is dispatched when an empty cell or grid is selected.Payload:

-   `endTimeMS`: End date of the selected cell in UTC milliseconds.
-   `row`: Information of the selected row as an object.
-   `startTimeMS`: Start date of the selected cell in UTC milliseconds.

**Note:** In the timeline view, the payload for this event contains the date and time information along with the contextual information.

</td></tr><tr><td>

Multi event selected

</td><td>

Action that is dispatched when multiple events are selected using the CTRL, CMD, OR Shift keys.Payload:

-   `selectedEvents`: Array of selected event objects.
-   `actionKeyReleased`: Boolean indicator showing the release status of the action key used to select the multiple events.
-   `escapeKeyPressed`: Boolean indicator showing the use of escape key.
-   `nonSelectionClickDetected`: Boolean indicator showing whether the user selected or interacted with any portion of the calendar other than a selectable event.

</td></tr><tr><td>

Popover closed

</td><td>

Action that is dispatched when popover provided with the Calendar closes. The payload is always empty.Payload: `{}`

</td></tr><tr><td>

Popover opened

</td><td>

Action that is dispatched when popover provided with the Calendar opens up.Payload includes `event`: Event object that is displayed in the popover.

</td></tr><tr><td>

Range updated

</td><td>

Action that is dispatched when the range of dates visible on Calendar changes.Payload:

-   `startMS`: Start date seen in view in UTC milliseconds.
-   `endMS`: End date seen in view in UTC milliseconds.
-   `columnNavigationDirection`: Indicator for the column navigation icon.

</td></tr><tr><td>

Scroll end

</td><td>

Action that is dispatched when the end of the calendar is reached. The payload is always empty.Payload: `{}`

</td></tr><tr><td>

Size changed

</td><td>

Action that is dispatched when the host size is changed.Payload: `size` with the identifier for the updated host size.

</td></tr><tr><td>

Timezone changed

</td><td>

Action that is dispatched when the timezone is changed from the timezone picker.Payload:

-   `from`: The old timezone
-   `to`: The new timezone

</td></tr><tr><td>

Timeline section toggled

</td><td>

Action that is dispatched when a section of the timeline is toggled.Payload includes `section`: Section that was selected.

</td></tr><tr><td>

Title column resized

</td><td>

Action that is dispatched when the title column is re-sized.Payload:

-   `width`: New width of the column relative to the total calendar width as a percentage.
-   `resizedColumn`: Index of the column being re-sized.
-   `newColumnWidths`: Array containing the new width of each column as a percentage relative to the total width of all columns.

</td></tr><tr><td>

Toolbar button clicked

</td><td>

Action that is dispatched when any toolbar button is selected.Payload: `actionName` with the name of the action corresponding to the button selected.

</td></tr><tr><td>

View changed

</td><td>

Action that is dispatched when the view is changed.Payload:

-   `from`: Old view
-   `to`: New view

</td></tr></tbody>
</table>