---
title: Timeline component setup
description: Timeline shows different activities in chronological order spread over a set time range. In a case record, agents can see a time line view of case activity. In CMDB, you can see different events that occur for a configuration item over a period of time.Configure the appearance and time range of your Timeline with these properties.Select event handlers to configure the action \(event\) provided with the Timeline component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/timeline-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Timeline component setup

Timeline shows different activities in chronological order spread over a set time range. In a case record, agents can see a time line view of case activity. In CMDB, you can see different events that occur for a configuration item over a period of time.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Timeline that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "timeline-content-tree.png"\] Alt text: Shows the timeline component in the UI Builder content tree

2.  Select the Timeline component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "timeline-properties.png"\] Alt text: Shows a portion of the configurable properties for the timeline component in the config tab


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Timeline component properties

Configure the appearance and time range of your Timeline with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Properties

<table id="table_nnk_v4t_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Compact view\[isCompactView\]

</td><td>

Displays the timeline on one line without the legend and title.Default: **false**

</td></tr><tr><td>

Formatted start date\[formattedStartDate\]

</td><td>

Formatted string of the minimum date that can be displayed in the timeline.

 Case – Usually the date/time the case was opened.

 CI – Usually the date/time the CI was installed.

 Default: **2019-01-01 05:00:00**

</td></tr><tr><td>

Formatted end date\[formattedEndDate\]

</td><td>

Formatted string of the maximum date that can be displayed in the timeline.

 Case – Usually the date/time the case was closed.

 CI – Usually either the current time \(if the CI is still operating\) or the date/time the CI was uninstalled.

 Default: **2020-06-01 05:00:00**

</td></tr><tr><td>

Formatted display start date\[formattedDisplayStartDate\]

</td><td>

Formatted string of an optional start date that can be displayed on the timeline.

 For example, for a CI, activities only in the last two or four weeks might be the most useful information to display. You can set this property to display the most useful start date for a range.

 Default: **2019-06-17 09:00:00**

</td></tr><tr><td>

Formatted display end date\[formattedDisplayEndDate\]

</td><td>

Formatted string of an optional end date that can be displayed on the timeline.

 For example, for a CI, activities only in the last two or four weeks might be the most useful information to display. You can set this property to display the most useful start date for a range.

 Default: **2019-12-14 09:00:00**

</td></tr><tr><td>

Locale\[locale\]

</td><td>

Language code string, such as 'ja' or 'de'.Default: **en**

</td></tr><tr><td>

Event data\[eventData\]

</td><td>

The activities to display on the timeline. Case - Usually when the customer or agent adds comments.

 CI – Usually the events or outages that have happened on a CI.

 Items in the array:

-   name
-   icon
-   iconHref
-   color
-   label
-   labelPlural
-   events

</td></tr><tr><td>

Range data\[rangeData\]

</td><td>

Array that defines the ranges to display on the timeline bar. For a case, this is usually the changes in the case state.Items in the array:

-   name
-   color
-   label
-   ranges

</td></tr><tr><td>

Display popover\[displayPopover\]

</td><td>

Controls how to display details for a point on the timeline. Set to **true** to display a popover when the timeline is clicked. Set to **false** to display a tooltip when the user hovers on the timeline.When set to true the **Display popover macroponent** property appears, enabling you to enter the component you want to appear in the popover.

 Default: **false**

</td></tr><tr><td>

Display popover macroponent\[popoverMacroponent\]

</td><td>

Adds a macroponent that renders inside the popover. Select from macroponent definitions in the `sys_ux_macroponent` table. This property is available when the **Display popover** property is set to **true**.

</td></tr><tr><td>

Hide padding\[hidePadding\]

</td><td>

Hides the padding for the timeline component.Default: **false**

</td></tr><tr><td>

Menu bar position\[menuBarPosition\]

</td><td>

Determines the position of the menu bar. The menu bar has the zoom in and zoom out buttons.Choices are:

-   Top right
-   Bottom right
-   Bottom left

Default: Top right

</td></tr><tr><td>

Enable markers\[enableMarkers\]

</td><td>

Displays markers in the component.Review the marker's configuration specified in the **Markers configuration** field when enabling markers.

</td></tr><tr><td>

Markers configuration\[markersConfig\]

</td><td>

The configuration of the markers in the component.Items in the array:

-   icon
-   color
-   markerType
-   markerTimestamps
-   datePickerConfiguration

</td></tr><tr><td>

Show close button\[showCloseButton\]

</td><td>

Displays the close button. The position of this button is fixed \(top right\).Default: **false**

</td></tr></tbody>
</table><table id="table_n1g_dp5_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Title to display at the top of the timeline.Default: **Timeline**

</td></tr><tr><td>

Label heading level\[labelHeadingLevel\]

</td><td>

Defines the HTML &lt;hx&gt; heading element used to render the label.Choices are **1-6:**

 Default: **3**

</td></tr><tr><td>

Label style\[labelStyle\]

</td><td>

Header text style.Choices are:

-   header-primary
-   header-secondary
-   header-tertiary
-   title-primary
-   title-secondary
-   title-tertiary

 Default: **title-tertiary**

</td></tr></tbody>
</table><table id="table_kzx_dq5_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide pan and zoom\[hidePanZoom\]

</td><td>

Hides the pan and zoom buttons from the timeline display.Default: **false**

</td></tr><tr><td>

Min. zoom spread\[minZoomSpread\]

</td><td>

The minimum display range allowed for the zoom-in action.

 Choices are:

-   Y=Year
-   M=Month
-   D=Day
-   H=Hour
-   M=Minute
-   S=Second
-   MS=Millisecond

 Default: **Day**

</td></tr><tr><td>

Hide now button\[hideNow\]

</td><td>

Hides the NOW button in the timeline display. The NOW button resets the timeline to the default state that existed on page load.Default: **true**

</td></tr></tbody>
</table><table id="table_yql_fr5_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Legend title\[legendTitle\]

</td><td>

Title in the legend used for events.Default: **Legend**

</td></tr><tr><td>

Legend event title\[legendEventTitle\]

</td><td>

Event title that displays in the legend drop-down list.Default: **Timeline Indicators**

</td></tr><tr><td>

Legend range title\[legendRangeTitle

</td><td>

Range title that displays in the legend drop-down list.Default: **Timeline Ranges**

</td></tr><tr><td>

Hide legend toggle\[hideToggle\]\[

</td><td>

Hides the legend toggle in the timeline display.Default: **false**

</td></tr></tbody>
</table><table id="table_nvk_fs5_c5b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show empty state\[isEmpty\]

</td><td>

Shows an empty state indication.Default: **false**

</td></tr><tr><td>

Show error state\[isError\]

</td><td>

Shows an error state indication.Default: **false**

</td></tr><tr><td>

Show loading state\[isLoading\]

</td><td>

Shows a loading state indication.Default: **false**

</td></tr></tbody>
</table>## Timeline component events

Select event handlers to configure the action \(event\) provided with the Timeline component.

The Events tab shows the events used by the Timeline component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Timeline actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "timeliine-component-events.png"\] Alt text: Shows the events available for the timeline component

### Event descriptions

<table id="table_tnj_yvv_24b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data selected

</td><td>

Triggers when the user selects an event, range, or marker on the timeline.Payload contains the following depending upon the type of data:

-   Event \(`selectedEvents`\):
    -   `eventName`
    -   `timestamp`
    -   `description`
    -   `data`
-   Range \(`selectedRanges`\):
    -   `rangeName`
    -   `start`
    -   `end`
    -   `description`
    -   `data`
-   Marker: `timestamp`

</td></tr><tr><td>

Popover link clicked

</td><td>

Triggers when the user selects a link in the popover.Payload contains `popoverLinkPayload`

</td></tr><tr><td>

Initialized

</td><td>

Triggers when timeline is initialized.Payload:

-   `startingTimestamp`
-   `endingTimestamp`

</td></tr><tr><td>

Range changed

</td><td>

Triggers when the user changes the display range.Payload:

-   `startingTimestamp`
-   `endingTimestamp`

</td></tr><tr><td>

Legend item updated

</td><td>

Triggers when an event or range item is toggled in the **Show legend** dropdown.Payload:

-   `dataType`
-   `data`

</td></tr><tr><td>

Close button clicked

</td><td>

Triggers when the user selects the close button.There is no payload.

</td></tr><tr><td>

Marker added

</td><td>

Triggers when the user adds a marker in the timeline.Payload contains `timestamp`.

</td></tr><tr><td>

Marker cleared

</td><td>

Triggers when the user clears or removes a marker from the timeline.Payload contains `timestamp`.

</td></tr><tr><td>

Marker timestamp invalid

</td><td>

Triggers when marker timestamps are not valid.Payload contains `timestamp`.

</td></tr></tbody>
</table>