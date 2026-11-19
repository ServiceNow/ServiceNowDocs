---
title: Date-Time-Interval component setup
description: The Date-Time-Interval component is a form control that enables users to select a range of dates and times.Properties in the Date-Time-Interval component have preset configuration values. You can accept these values or override them manually.Select event handlers to configure the events provided with the Date-Time-Interval component. Event handlers work with data resources to link the Date-Time-Interval actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/date-time-interval-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Date-Time-Interval component setup

The Date-Time-Interval component is a form control that enables users to select a range of dates and times.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Define a label for Date-Time-Interval that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "date-time-interval-content-tree.png"\] Alt text: Shows the Date-Time-Interval component in the UI Builder content tree.

2.  Select the Date-Time-Interval component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "date-time-interval-config.png"\] Alt text: Shows the Date-Time-Interval component in the UI Builder configuration panel.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Date-Time-Interval component properties

Properties in the Date-Time-Interval component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Default presets

The Date-Time-Interval component comes with the following default presets:

-   **Last 7 days**
-   **Last month**
-   **Last 3 months**
-   **Last 6 months**
-   **Year to date**
-   **Last year**

These presets are designed to provide quick access to commonly used time intervals.

### Custom presets

In addition to the default presets, users can create custom presets to define their own time intervals. Custom presets are configured using a set of keywords and types. The available keywords and types are as follows:

-   **Keywords \(string\)**
    -   Next: for future time intervals
    -   Last: for past time intervals
    -   Current: for the current time interval
    -   to date: for intervals up to the current date
-   **Types \(string\)**
    -   year/years
    -   month/months
    -   week/weeks
    -   day/days
    -   hour/hours
    -   minute/minutes
    -   second/seconds
    -   start
    -   end
    -   business

For example, users can create custom presets for:

-   **Last 14 days**
-   **Next 30 days**
-   **Current month**

To create a custom preset, users need to specify the following properties:

-   keyword \(string\): specifies whether the preset is for a future, past, or current time interval
-   presetType \(string\): the time unit
-   duration \(number\): the duration of the preset in the specified time unit
-   order \(number\): the order in which the preset appears in the options list
-   label \(string\): the display label for the preset
-   startDate \(string\): fixed start date for the preset
-   endDate \(string\): fixed end date for the preset

### Properties

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Adaptive\[adaptive\]

</td><td>

Defines whether the input layout is responsive to the viewport or always vertical.Default: **Adaptive**

</td></tr><tr><td>

Size\[size\]

</td><td>

Sets the input size.Default: **Medium**

</td></tr><tr><td>

Gap\[gap\]

</td><td>

Sets the input spacing.Default: **Small**

</td></tr><tr><td>

Type\[type\]

</td><td>

The type of calendar to use with the form field.Default: **Date**

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Select to prevent the user from interacting with the field or changing its value.

</td></tr><tr><td>

Read only\[readonly\]

</td><td>

Select to make the field read-only and prevent users from modifying the value.

</td></tr><tr><td>

Auto-focus

</td><td>

Select to automatically place the focus inside the input on page load.

</td></tr></tbody>
</table><table id="table_mh1_ncz_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start value\[valueStart\]

</td><td>

The value of the start input field. Unless the input field has pre-populated data, leave this property empty.

</td></tr><tr><td>

Manage value start\[manageValueStart\]

</td><td>

If set to **true**, overrides automatic updates to the **Start value** property. Use the **Date time interval value start set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

End value\[valueEnd\]

</td><td>

The value of the end input field. Unless the input field has pre-populated data, leave this property empty.

</td></tr><tr><td>

Manage value end\[manageValueEnd\]

</td><td>

If set to **true**, overrides automatic updates to the **End value** property. Use the **Date time interval value end set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Enable same day\[enableSameDay\]

</td><td>

Allows users to select duplicate values for start and end inputs.

</td></tr><tr><td>

Field layout configuration\[fieldLayout\]

</td><td>

Determines whether the labels, fields, and slotted content are arranged vertically or horizontally, and their respective proportion in a horizontal container.

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Name of the input field.

</td></tr><tr><td>

Start placeholder text\[placeholderStart\]

</td><td>

Placeholder text for the start input field that helps the user understand what input is expected.

</td></tr><tr><td>

End placeholder text\[placeholderEnd\]

</td><td>

Placeholder text for the end input field that helps the user understand what input is expected.

</td></tr></tbody>
</table><table id="table_a3k_12z_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start label\[labelStart\]

</td><td>

Label describing the overall purpose of the start select field.Default: **Select start date**

</td></tr><tr><td>

End label\[labelEnd\]

</td><td>

Label describing the overall purpose of the end select field.Default: **Select end date**

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Select to indicate that the field is required.

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

When true, the required indicator is hidden. Use this for forms where most fields are required, along with the **Optional** flag for any fields that are not required.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Select to indicate that the field is optional.

</td></tr><tr><td>

Start helper content\[helperContentStart\]

</td><td>

If set, an information icon with popover text appears next to the field start label to display help text to the user. Use plain text to allow for translation. If you don't want to add helper content, leave this property empty.

</td></tr><tr><td>

End helper content\[helperContentEnd\]

</td><td>

If set, an information icon with popover text appears next to the field end label to display help text to the user. Use plain text to allow for translation. If you don't want to add helper content, leave this property empty.

</td></tr></tbody>
</table><table id="table_opn_q2z_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

When true, indicates that the field is in an incorrect state, which is reflected in the field display.

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Date time interval invalid set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Alert messages\[messages\]

</td><td>

Array of inline alert messages that display below the field. The following list describes each object's properties:-   `content`: The text of the alert message.
-   `status`: The type of alert to display.
-   `icon`: Icon to display at the start of the alert message.

Default:

```

{
    "name": "content",
    "label": "Content",
    "fieldType": "string",
    "translatable": true
},
{
    "name": "status",
    "label": "Status",
    "fieldType": "choice",
    "typeMetadata": {
        "choices": [
            {
                "label": "Critical",
                "value": "critical"
            },
            {
                "label": "Warning",
                "value": "warning"
            },
            {
                "label": "Positive",
                "value": "positive"
            },
            {
                "label": "Info",
                "value": "info"
            },
            {
                "label": "Suggestion",
                "value": "suggestion"
            }
        ]
    }
},
{
    "name": "icon",
    "label": "Icon",
    "fieldType": "icon"
}

```

</td></tr></tbody>
</table><table id="table_frd_ffz_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Format pattern\[format\]

</td><td>

Configures the Unicode Technical Standard \(UTS\) format of the input value.

</td></tr></tbody>
</table><table id="table_rxq_3fz_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opened\[opened\]

</td><td>

Flag that indicates whether the calendar is open \(true\) or closed \(false\).

</td></tr><tr><td>

Manage opened\[manageOpened\]

</td><td>

If set to **true**, overrides automatic updates to the **Opened** property. Use the **Date time value opened set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Show default footer actions\[showDefaultFooterActions\]

</td><td>

Select to show default footer actions.

</td></tr><tr><td>

Default footer action labels\[defaultFooterActionLabels\]

</td><td>

Allows for custom naming of default footer action buttons.

</td></tr><tr><td>

Footer actions\[footerActions\]

</td><td>

Array of objects that define the buttons that appear in the calendar footer. The following list describes each object's properties:-   `label`: Text displayed on the button.
-   `variant`: Visual style of the button.
-   `tooltipContent`: Tooltip text that displays when the user hovers over the button.
-   `clickActionType`: Type of action to trigger when the button is selected.
-   `disabled`: Disables the button.
-   `bare`: Applies the bare button style.
-   `size`: Size of the button.
-   `configAria`: Defines ARIA attributes for the button.
-   `closeCalendar`: Determines whether selecting the button closes the calendar.

Default:

```

{
    "name": "label",
    "label": "Label",
    "fieldType": "string"
},
{
    "name": "variant",
    "label": "Variant",
    "fieldType": "string"
},
{
    "name": "tooltipContent",
    "label": "Tooltip content",
    "fieldType": "string"
},
{
    "name": "clickActionType",
    "label": "Click action type",
    "fieldType": "string"
},
{
    "name": "disabled",
    "label": "Disabled",
    "fieldType": "boolean"
},
{
    "name": "bare",
    "label": "Bare",
    "fieldType": "boolean"
},
{
    "name": "size",
    "label": "Size",
    "fieldType": "string"
},
{
    "name": "configAria",
    "label": "Config aria",
    "fieldType": "json"
},
{
    "name": "closeCalendar",
    "label": "Close calendar",
    "fieldType": "boolean"
}

```

</td></tr><tr><td>

Hide adjacent months\[hideAdjacentDates\]

</td><td>

When **true** and **Type** is **Date**, the calendar doesn't show dates outside the displayed month.

</td></tr><tr><td>

Panel fit props\[panelFitProps\]

</td><td>

Keys to set to configure the calendar picker.

</td></tr><tr><td>

Day of week headings\[weekdayHeadings\]

</td><td>

Configures the length of the weekday headings.

</td></tr><tr><td>

First day of week\[firstDayOfWeek\]

</td><td>

Sets the first day of the week on the calendar panel.

</td></tr><tr><td>

Disable weekends\[disableWeekends\]

</td><td>

Select to turn off weekend days. Weekend days are determined by the `weekendDays` property.

</td></tr><tr><td>

Weekend days\[weekendDays\]

</td><td>

Sets which days are weekend days. Defaults to **Saturday and Sunday**.

</td></tr><tr><td>

Disabled items\[disabledItems\]

</td><td>

Array of objects representing dates that can't be selected. These dates must be string values that match the specified `format` property.

</td></tr><tr><td>

Enable presets\[enablePresets\]

</td><td>

Enables the left hand panel containing various preset intervals for convenience.

</td></tr><tr><td>

Show preset groups\[showPresetGroups\]

</td><td>

Shows preset intervals grouped by their group label.

</td></tr><tr><td>

Custom presets\[customPresets\]

</td><td>

Array of objects representing preset intervals. Each object configures a time range using keywords, types, and optional fixed dates. Available preset intervals are displayed in the preset panel.Default:

```

{
  "keyword": {
    "type": "string",
    "enum": [
      "Next",
      "Last",
      "Current",
      "to date",
      "Custom"
    ]
  },
  "presetType": {
    "type": "string",
    "enum": [
      "year",
      "years",
      "quarter",
      "quarters",
      "month",
      "months",
      "week",
      "weeks",
      "day",
      "days",
      "hour",
      "hours",
      "minute",
      "minutes",
      "second",
      "seconds",
      "start",
      "end",
      "business"
    ]
  },
  "duration": {
    "type": "number"
  },
  "order": {
    "type": "number"
  },
  "label": {
    "type": "string"
  },
  "groupLabel": {
    "type": "string"
  },
  "startDate": {
    "type": "string"
  },
  "endDate": {
    "type": "string"
  },
  "group": {
    "type": "string"
  },
  "focused": {
    "type": "boolean"
  },
  "selected": {
    "type": "boolean"
  },
  "index": {
    "type": "number"
  },
  "position": {
    "type": "number"
  },
  "setSize": {
    "type": "number"
  },
  "type": {
    "type": "string"
  }
}

```

</td></tr><tr><td>

Active preset\[activePreset\]

</td><td>

Configures an active preset to be selected in the preset panel.

</td></tr><tr><td>

Set the custom preset position to the bottom\[customPresetPositionBottom\]

</td><td>

When selected, the **Custom** preset is placed at the bottom of the preset panel.

</td></tr></tbody>
</table><table id="table_ght_vhz_12c"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

ARIA properties that are set on innerHTML. See https://www.w3.org/WAI/ARIA/apg/example-index/combobox/combobox-datepicker.html for properties and accepted values.

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Date-Time-Interval component events

Select event handlers to configure the events provided with the Date-Time-Interval component. Event handlers work with data resources to link the Date-Time-Interval actions to the data you want to display to your users.

The Events tab shows the events used by the Date-Time-Interval component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

\[Omitted image "date-time-interval-events.png"\] Alt text: Shows the events available for the Date-Time-Interval component.

### Event handlers

Event handlers work with data resources to link the Date-Time-Interval actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date time interval custom presets set\[NOW\_DATE\_TIME\_INTERVAL\#CUSTOM\_PRESETS\_SET\]

</td><td>

The user sets custom presets for the component.Payload: value \(JSON\) Contains these properties:

-   keyword \(string\)
-   presetType \(string\)
-   duration \(number\)
-   order \(number\)
-   label \(string\)
-   groupLabel \(string\)
-   startDate \(string\)
-   endDate \(string\)

</td></tr><tr><td>

Date time interval enter keydown\[NOW\_DATE\_TIME\_INTERVAL\#ENTER\_KEYDOWN\]

</td><td>

The user presses the Enter key while focus is inside the input.Payload:

-   name \(string\)
-   fieldValue \(string\)
-   type \(string\)

</td></tr><tr><td>

Date time interval footer action clicked\[NOW\_DATE\_TIME\_INTERVAL\#FOOTER\_ACTION\_CLICKED\]

</td><td>

The user selects a footer action item. The payload includes a reference to the selected item and action.Payload: action \(JSON\)

-   variant \(string\)
-   label \(string\)
-   bare \(boolean\)
-   disabled \(boolean\)
-   tooltipContent \(string\)
-   clickActionType \(string\)

</td></tr><tr><td>

Date time interval input\[NOW\_DATE\_TIME\_INTERVAL\#INPUT\]

</td><td>

The user enters data in the field by typing or pasting text. The system does not validate the value or update the `value` property.Payload:

-   name \(string\)
-   data \(string\)
-   fieldValue \(string\)
-   type \(string\)

</td></tr><tr><td>

Date time interval invalid set \[NOW\_DATE\_TIME\_INTERVAL\#INVALID\_SET\]

</td><td>

The user moves focus away from the field. Payload:

-   name \(string\)
-   fieldValue \(string\)
-   valueStart \(string\)
-   valueEnd \(string\)
-   isStartInvalid \(boolean\)
-   isEndInvalid \(boolean\)
-   value \(boolean\)
-   type \(string\)
-   format \(string\)
-   errorId \(array\)

</td></tr><tr><td>

Date time interval items set\[NOW\_DATE\_TIME\_INTERVAL\#ITEMS\_SET\]

</td><td>

The user sets the component's visual date items. The payload is an array containing one or more arrays, each representing a row on the date grid. Each row contains items corresponding to a given date item.Payload: value \(JSON\) Contains these properties:

-   date \(object\)
-   label \(string\)
-   a11yLabel \(string\)
-   adjacent \(boolean\)
-   now \(boolean\)
-   selected \(boolean\)
-   range \(boolean\)
-   tween \(boolean\)
-   disabled \(boolean\)
-   id \(string\)

</td></tr><tr><td>

Date time interval opened set\[NOW\_DATE\_TIME\_INTERVAL\#OPENED\_SET\]

</td><td>

Automatically updates when the user opens or closes the visual picker.Payload: value \(boolean\)

</td></tr><tr><td>

Date time interval value end set\[NOW\_DATE\_TIME\_INTERVAL\#VALUE\_END\_SET\]

</td><td>

The user moves focus away from the second field upon manually entering a date, or the field value changes via a calendar selection.Payload:

-   name \(string\)
-   value \(string\)
-   type \(string\)
-   format \(string\)
-   date \(string\)
-   isoDate \(string\)

</td></tr><tr><td>

Date time interval value start set\[NOW\_DATE\_TIME\_INTERVAL\#VALUE\_START\_SET\]

</td><td>

The user moves focus away from the first field upon manually entering a date, or the field value changes via a calendar selection.Payload:

-   name \(string\)
-   value \(string\)
-   type \(string\)
-   format \(string\)
-   date \(object\)
-   isoDate \(string\)

</td></tr></tbody>
</table>