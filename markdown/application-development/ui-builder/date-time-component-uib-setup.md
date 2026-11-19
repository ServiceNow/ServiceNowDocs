---
title: Date-Time component setup
description: The Date-Time component is a form control that enables users to input or select a date, time, or date and time value.Configure the properties that define a date and time for this component.Select event handlers to configure the events provided with the Date-Time component. Event handlers work with data resources to link the Date-Time actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/date-time-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Date-Time component setup

The Date-Time component is a form control that enables users to input or select a date, time, or date and time value.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Date-Time that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). \[Omitted image "date-time-content-tree.png"\] Alt text: Shows the date-time component in the UI Builder content tree

2.  Select the Date-time component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Date-time label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Date-Time component properties

Configure the properties that define a date and time for this component.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Schedule run start date__**

    This preset requires the **Data Manager Policy Form** controller.

    Properties included in this preset are:

    -   Component visibility \(size, type, disabled, read only, auto-focus, field layout configuration\)
    -   Value
    -   Label
    -   Validation
    -   Format
    -   Picker
    -   Accessibility
-   **__Schedule run time datetime__**

    This preset requires the **Data Manager Policy Form** controller.

    Properties included in this preset are:

    -   Component visibility \(size, type, disabled, read only, auto-focus, field layout configuration\)
    -   Value
    -   Label
    -   Validation
    -   Format
    -   Accessibility

### Properties

<table id="table-uib-prop-labels"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Size\[size\]

</td><td>

Sets the input text size. The choices are **small** or **medium**.Default: **medium**

</td></tr><tr><td>

Type\[type\]

</td><td>

Type of calendar to use with the form field. The choices are:-   **Date**
-   **Date-time**
-   **Time**
-   **Month**
-   **Year**
-   **Quarter**
-   **Week-year**

**Note:** The selection of a calendar type can change the properties available for configuration.

</td></tr><tr><td>

Disabled\[disabled\]

</td><td>

Disables the input field to prevent the user from interacting with it or changing its value.Default: **false**

</td></tr><tr><td>

Read only\[readonly\]

</td><td>

Makes the input field read-only to prevent users from modifying the value.Default: **false**

</td></tr><tr><td>

Auto-focus\[autofocus\]

</td><td>

Automatically puts focus in the input field when the page loads.Default: **false**

</td></tr><tr><td>

Field layout configuration \[fieldLayout\]

</td><td>

Sets the input field layout. **Vertical** displays the label above the input field and **horizontal** displays the label in line with the input field.

</td></tr></tbody>
</table><table id="table_r15_2yb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Value\[value\]

</td><td>

Value of the input field. Unless the input field has pre-populated data, leave this property empty.

</td></tr><tr><td>

Manage value\[manageValue\]

</td><td>

If set to **true**, overrides automatic updates to the **Value** property. Use the **Date time value set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Placeholder text\[placeholder\]

</td><td>

Placeholder text for the input field that helps the user understand what input is expected.

</td></tr><tr><td>

Identifier\[name\]

</td><td>

Name of the input field. This value is dispatched with the event when a user interacts with the field.

</td></tr><tr><td>

Text align \[align\]

</td><td>

Text alignment of input field value. The choices are **start**, **center**, and **end**.

</td></tr></tbody>
</table><table id="table_k11_hyb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label\[label\]

</td><td>

Label describing the overall purpose of the input field.Default: **Select date**

</td></tr><tr><td>

Wrap label\[wrapLabel\]

</td><td>

If the label doesn't fit on one line, wraps the label.

</td></tr><tr><td>

Required\[required\]

</td><td>

Indicates whether or not the input field is a required field.Default: **false**

</td></tr><tr><td>

Hide required indicator\[hideRequiredIndicator\]

</td><td>

Shows or hides the required indicator on the input field. Use this for forms where most fields are required, together with the "optional" flag for any fields that are not required.Default: **false**

**Note:** This property is available when the **Type** property is set to **Time**.

</td></tr><tr><td>

Optional\[optional\]

</td><td>

Indicates that the input field is optional.Default: **false**

</td></tr><tr><td>

Helper content\[helperContent\]

</td><td>

Provides additional hint text for the user, such as password requirements or other instructions for setting the field. When you provide content in this field, an iconic button appears next to the field label to trigger a popover containing the content. Use plain text to allow for translation. If you do not want to add helper content, leave this property empty.

</td></tr></tbody>
</table><table id="table_n3t_3yb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invalid\[invalid\]

</td><td>

Enables the input field to indicate when it's in an incorrect state. This state is reflected in the field display.Default: **false**

</td></tr><tr><td>

Manage invalid\[manageInvalid\]

</td><td>

If set to **true**, overrides automatic updates to the **Invalid** property. Use the **Date time invalid set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Alert messages\[messages\]

</td><td>

Array of alert messages that display below the field. The following list describes each object's properties:-   `content`: The text of the alert message.
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
</table><table id="table_bb3_kyb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Format pattern\[format\]

</td><td>

Format used for the date and time input value, based on the Unicode Technical Standard \(UTS\). An example of a date format is **dd/mm/yyyy**, and an example of a time format is **hh:mm:ss**. A time zone token \(z\) can be added to enable time zones in an **hh:mm:ss z** format.

</td></tr></tbody>
</table><table id="table_p4d_nyb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Opened\[opened\]

</td><td>

Indicates if the calendar is open \(**true**\) or closed \(**false**\).Default: **false**

</td></tr><tr><td>

Manage opened\[manageOpened\]

</td><td>

If set to **true**, overrides automatic updates to the **Opened** property. Use the **Date time opened set** event to intercept the requested change and handle it manually.Default: **false**.

</td></tr><tr><td>

Show default footer actionsshowDefaultFooterActions

</td><td>

Shows the default footer actions in the component. The **footerActions** property overrides this property.Default: **false**

**Note:** This property is available when the Type property is set to **Month**, **Year**, **Quarter**, or **Week-year**.

</td></tr><tr><td>

Default footer action labels\[defaultFooterActionLabels\]

</td><td>

Custom names for default footer action buttons.

</td></tr><tr><td>

Footer actions\[footerActions\]

</td><td>

Array of objects that define the buttons that appear in the calendar footer. You can define up to two buttons, set from right to left. The following list describes each object's properties:-   `label`: Text displayed on the button.
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

Hide footer\[hideFooter\]

</td><td>

Hides the footer in the calendar panel.Default: **false**

</td></tr><tr><td>

Hide adjacent months\[hideAdjacentDates\]

</td><td>

Hides dates outside the displayed month interval when set to **true**.Default: **false**

**Note:** This property is available when the Type property is set to **Date** or **Date-time**.

</td></tr><tr><td>

Panel fit props\[panelFitProps\]

</td><td>

Keys to set to configure the calendar picker. Use these keys to position and scale the panel relative to the panel target.Valid keys:

-   **position**: Array of possible positions in which to place the panel relative to its target. Choices are: \["bottom-start top-start","top-start bottom-start","bottom-end top-end","top-end bottom-end"\]
-   **offset**: Number of pixels to offset the panel from its associated trigger.

</td></tr><tr><td>

Day of week headings\[weekdayHeadings\]

</td><td>

Sets the length of the weekday headings.Valid values:

-   **short**: Two-character headings, such as, Su, Mo, Tu, We, and Th
-   **narrow**: One-character headings, such as, S, M, T, W, and T

**Note:** This property is hidden when the Type property is set to **Month**, **Year**, or **Quarter**.

</td></tr><tr><td>

First day of week\[firstDayOfWeek\]

</td><td>

Sets the first day of the week on the calendar panel. The value can range from 0 \(Sunday\) to 6 \(Saturday\). The value in this property only applies when the value in the **Format pattern** property is set to a day or week pattern, and the **Type** property is set to **Date** or **Date-time**.**Note:** This property is hidden when the Type property is set to **Month**, **Year**, or **Quarter**.

</td></tr><tr><td>

Disable weekends\[disableWeekends\]

</td><td>

Disables weekend days for the **Date** calendar type. The actual values used are determined by the **Weekend days** property.Default: **false**

**Note:** This property is hidden when the Type property is set to **Month**, **Year**, or **Quarter**.

</td></tr><tr><td>

Weekend days\[weekendDays\]

</td><td>

Sets which days are weekend days.Defaults: **0 \(Sunday\)** and **6 \(Saturday\)**.

**Note:** This property is hidden when the Type property is set to **Month**, **Year**, or **Quarter**.

</td></tr><tr><td>

Default time\[initialTime\]

</td><td>

Configures the initial time for the date-time format. If a start time isn't configured, the time defaults to midnight of the same day. **Note:** This property is available when the Type property is set to **Date-time**.

</td></tr><tr><td>

Disabled items\[disabledItems\]

</td><td>

An array of objects representing disabled dates. String values must be date strings matching those defined in the **Format pattern** property.Valid values:

-   Value: An example of a value is:`{value: "2020/01/01"}`
-   Interval: An example of an interval is:`{start: "2020/01/01", end: "2020/12/31"}`
-   Before-interval: An example a before interval is: `{before: "2020/01/01"}`
-   After-interval: An example of an after interval is: `{after: "2020/01/01"}`

</td></tr></tbody>
</table><table id="table_ng2_qyb_4fc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ARIA properties\[configAria\]

</td><td>

Object whose keys reference a specific HTML element within the component. The value of each key is an object that contains ARIA properties and corresponding values. These ARIA properties are set on the specified element. See [https://www.w3.org/](https://www.w3.org/) for properties and accepted values.

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Date-Time component events

Select event handlers to configure the events provided with the Date-Time component. Event handlers work with data resources to link the Date-Time actions to the data you want to display to your users.

The Events tab shows the events used by the Date-Time component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Date-Time actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_smd_cwv_g1c"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date time invalid set \[NOW\_DATE\_TIME\#INVALID\_SET\]

</td><td>

The user moves focus away from the field. Payload:

-   name \(string\)
-   value \(boolean\) Value of the `invalid` property, which is based on the values of the `required` and `format` properties.
-   fieldValue \(string\)
-   type \(string\)
-   format \(string\)

</td></tr><tr><td>

Date time value set\[NOW\_DATE\_TIME\#VALUE\_SET\]

</td><td>

The user moves focus away from the field, and the value is valid. Payload:

-   name \(string\)
-   value \(string\)
-   format \(string\)
-   type \(string\)
-   date \(date\)
-   isoDate \(string\)

</td></tr><tr><td>

Date time input\[NOW\_DATE\_TIME\#INPUT\]

</td><td>

The user enters data in a field by typing or pasting text. The system does not validate the content or update the `value` property.Payload:

-   name \(string\)
-   data \(string\) Value entered in the field that caused the event to occur.
-   fieldValue \(string\) Current value of the field when the event occurred.

</td></tr><tr><td>

Date time enter keydown\[NOW\_DATE\_TIME\#ENTER\_KEYDOWN\]

</td><td>

The user presses the Enter key while focus is inside the input field.Payload:

-   name \(string\)
-   fieldValue \(string\)
-   type \(string\)

</td></tr><tr><td>

Date time opened set\[NOW\_DATE\_TIME\#OPENED\_SET\]

</td><td>

Automatically updates when the user opens or closes the visual calendar picker.Payload: value \(boolean\)

</td></tr><tr><td>

Date time items set\[NOW\_DATE\_TIME\#ITEMS\_SET\]

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

Date time footer action clicked\[NOW\_DATE\_TIME\#FOOTER\_ACTION\_CLICKED\]

</td><td>

The user selects a footer action item. The payload includes a reference to the selected item and action.Payload: action \(JSON\)

-   variant \(string\)
-   label \(string\)
-   bare \(boolean\)
-   disabled \(boolean\)
-   tooltipContent \(string\)
-   clickActionType \(string\)

</td></tr></tbody>
</table>