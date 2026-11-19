---
title: Schedule Recurrence component setup
description: The Schedule Recurrence enables you to automate repetitive, or recurring, tasks by configuring their frequency, exceptions to their occurrence, and overrides. This component also enables you to use custom patterns for such events.Properties in the Schedule Recurrence component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/schedule-recurrence-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 10
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Schedule Recurrence component setup

The Schedule Recurrence enables you to automate repetitive, or recurring, tasks by configuring their frequency, exceptions to their occurrence, and overrides. This component also enables you to use custom patterns for such events.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

**Role required**: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Schedule Recurrence that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

2.  Select the Schedule Recurrence component using one of these methods:

    -   Click anywhere within the component.
    -   Select the Action bar label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

3.  Either select **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Select a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Schedule Recurrence component properties

Properties in the Schedule Recurrence component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Bind Recurrence Schedule__**

    This preset interacts with the global schedules available in the platform. This preset requires the `cmnSchedule` controller.

    **Caution:**

    This preset interacts with the `cm_schedule`, `cmn_schedule_span`, and `cmn_other_schedule` tables to perform operations. Ensure that you have read, write, and execute permissions for the tables.

    Properties included in this preset are:

    -   All Day
    -   Available time zones
    -   create
    -   Date format
    -   Days in week
    -   Disable skip dates
    -   Title
    -   Expand advance settings
    -   First day of week
    -   From time
    -   Month type
    -   Exceptions
    -   Skip dates
    -   Repeat count
    -   Repeat type
    -   Repeat until
    -   Time zone
    -   Series end
    -   Start date
    -   Time format
    -   To date
    -   To time
    -   Validations
    -   Year type
    The following events correspond to this preset:

    -   Handled events:
        -   CREATE\_SCHEDULE\_RECURRENCE
        -   DELETE\_SCHEDULE\_RECURRENCE
    -   Dispatched events:
        -   CREATE\_SCHEDULE\_RECURRENCE\_SUCCESS
        -   ON\_DELETE\_SCHEDULE\_RECURRENCE

### Properties

<table id="table-uib-props"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[eventTitle\]

</td><td>

Title of the recurring event.

</td></tr><tr><td>

Date format\[dateFormat\]

</td><td>

Sets the format for all date fields in the component like **Start date** and **End date**.Available options:

-   **yyyy-MM-dd**
-   **MM-dd-yyyy**
-   **dd/MM/yyyy**
-   **dd-MM-yyyy**
-   **dd.MM.yyyy**

Default: **dd-MM-yyyy**

</td></tr><tr><td>

Start date\[startDate\]

</td><td>

Sets the start date for the recurring event. If not specified, the component uses the current date.

</td></tr><tr><td>

To date\[toDate\]

</td><td>

Date on which the recurring event ends. Available when **All Day** is set to **true**.

</td></tr><tr><td>

All Day\[allDay\]

</td><td>

To mark the duration of the event as an all-day event, set to **true**. **Note:** Enabling this property enables the **To date** property and disables the **From time** and **To time** properties.

Default: **false**

</td></tr><tr><td>

Time format\[timeFormat\]

</td><td>

Sets the format for all time fields in the component like **From time** and **To time**. Supports all DGS \(Directorate General of Shipping\) formats.Available options:

-   **HH:mm**
-   **HH:mm a**
-   **hh:mm**
-   **hh:mm a**

Default: **hh:mm a**

</td></tr><tr><td>

From time\[fromTime\]

</td><td>

Time at which the recurring event starts. If not specified, the component uses the nearest upcoming half hour.

</td></tr><tr><td>

To time\[toTime\]

</td><td>

Time at which the recurring event ends. If not specified, the component uses one hour after the **From time**.

</td></tr><tr><td>

Available time zones\[availableTimezones\]

</td><td>

List of time zones available to the user when configuring a recurring event as a JSON object. **Note:**

-   If adding more time zones, ensure that you use the DGS-recognised ID for the time zone.
-   Floating time zone shows the same time slot in the user's time zone, instead of adjusting the time based on time differences. For example, if the user configures an event to occur at 10:00 AM PST, then Floating time zone schedules the event to occur at 10:00 AM in the end user's time zone.

</td></tr><tr><td>

Time zone\[selectedTimezone\]

</td><td>

Sets the time zone to display when the component loads. The user can select other time zones from the available options based on the **Available time zones** property's configuration.Default: &lt;local time zone&gt;

</td></tr><tr><td>

Repeat type\[repeatType\]

</td><td>

Sets the frequency of the event.Available options are:

-   **Never**
-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Yearly**

Default: **Never**

</td></tr><tr><td>

Repeat count\[repeatCount\]

</td><td>

Sets the number of times the event must repeat. Available when **Repeat type** is set to any value other than **Never**.Default: **1**

</td></tr><tr><td>

Repeat until\[repeatUntil\]

</td><td>

Sets the last date for the event to repeat. Available when **Repeat type** is set to any value other than **Never**.

</td></tr><tr><td>

Days in week\[daysInWeek\]

</td><td>

Available when **Repeat type** is **Weekly**. An array with the days in which the event occurs.

</td></tr><tr><td>

Month type\[monthType\]

</td><td>

Available when **Repeat type** is **Monthly**. Sets whether the user selects the date or day on which the event recurs. Available options are:

-   **Date**: Date on which the event recurs.
-   **Day**: Day on which the event recurs, like second Tuesday every month.

Default: **Day**

</td></tr><tr><td>

Year type\[yearType\]

</td><td>

Available when **Repeat type** is **Yearly**. Sets whether the user selects the date or day on which the event recurs.Available options:

-   **Date**: Date on which the event recurs
-   **Day**: Day on which the event recurs

Default: **Date**

</td></tr></tbody>
</table><table id="table_xhx_nsl_gfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable skip dates\[disableSkipDate\]

</td><td>

To disable the **Skip dates** feature, set to **true**. Enabling this property ignores the **Skip dates** configuration.Default: **false**

</td></tr><tr><td>

Skip dates\[recurrenceSkipDates\]

</td><td>

Array with the dates on which to skip the event. Configure this property with the date format specified in the **Date format** property.Default: \[\]

</td></tr><tr><td>

Exceptions\[recurrenceExceptions\]

</td><td>

JSON object array with the exception rules for the skip dates. Exceptions specified here are applied to the skip date rule. For example, if a skip date happens to be 3rd April and the same date is specified in the exceptions, the component adds the recurring event on \(doesn't skip\) 3rd April.Object properties:

-   `allDay`: Boolean
-   `eventTitle`: String
-   `daysInWeek`: String
-   `fromTime`: String
-   `monthType`: String
-   `repeatCount`: Number
-   `repeatType`: String
-   `repeatUntil`: String
-   `startDate`: String
-   `toDate`: String
-   `toTime`: String
-   `yearType`: String

Default: \[\]

**Tip:** The attributes in this object correspond to the properties in Schedule recurrence. Refer to their descriptions for information about their configuration.

</td></tr><tr><td>

Validations\[validationMessages\]

</td><td>

JSON object array with the configuration for validation rules.Object properties:

-   `header`: Heading text for the validation rule.
-   `message`: Body text for the validation rule.
-   `type`: The type of message to show. Available options are:
    -   `critical`
    -   `high`
    -   `info`
    -   `low`
    -   `moderate`
    -   `positive`
    -   `warning`

Default: \[\]

</td></tr><tr><td>

First day of Week\[firstDayOfWeek\]

</td><td>

First day of the week in the calendar.Default: **Monday**

</td></tr><tr><td>

Series end\[seriesEndFields\]

</td><td>

Array with the configuration of the options for when the event series can end. You can modify the array to remove options or add removed options but not add unrecognized options.Object properties:

-   `never`: Enables the user to specify that the recurring event series never ends.
-   `after`: Enables the user to select number of occurrences after which the series ends.
-   `on`: Enables the user to specify the date on which the series ends \(last date for the series\).

Default:

```json
[
    "never",
    "after",
    "on"
]
```

</td></tr><tr><td>

Expand advance settings\[expandAdvancedSettings\]

</td><td>

To expand the advanced settings on component load, set to **true**.Default: **false**

</td></tr></tbody>
</table>### Manual configuration

To configure properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Schedule Recurrence component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Schedule Recurrence component. Events with presets are marked with the **Preset** badge. To show events that do not have preset configurations, select **+ Add event mapping**. If the component has only one event and that event does not have a preset, the event is displayed and is ready for configuration.

### Event handlers

Event handlers work with data resources to link the Schedule Recurrence actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Bind Recurrence Schedule__**

    This preset provides data handlers for these events:

    -   Handled events:
        -   Create or update schedule recurrence \(CREATE\_SCHEDULE\_RECURRENCE\): Used to create or update a recurring event.

            Payload:

            -   `eventRecurrence`: Object with event details.
            -   `sysId`: Sys ID of the event to update, empty when creating the event.
        -   Delete schedule recurrence \(DELETE\_SCHEDULE\_RECURRENCE\): Used to delete a recurring event.

            Payload: `sysID`, sys ID of the event to delete.

    -   Dispatched events:
        -   Create or update successful schedule recurrence \(CREATE\_SCHEDULE\_RECURRENCE\_SUCCESS\): Dispatched when the create or update operation is successful.

            Payload: `scheduleSysId`, Sys ID of the event created or updated.

        -   Schedule recurrence deletion \(ON\_DELETE\_SCHEDULE\_RECURRENCE\): Dispatched when the delete operation i successful.

            Payload: `isScheduleDeleted`, boolean indicator showing the status of deletion.


### Event descriptions

<table id="table_yjj_zbl_gfc"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EVENT\_RECURRENCE\#EVENTS\_SAVE

</td><td>

Triggered when save button is clicked inside recurrence component.Payload:

-   `event`: Object
-   `skipDates`: Array
-   `exceptions`: Array

</td></tr><tr><td>

EVENT\_RECURRENCE\#EVENTS\_CANCEL

</td><td>

Triggered when cancel button is clicked inside recurrence component. It doesn't have any payload.

</td></tr></tbody>
</table>### Recommended reading

-   [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md)
-   [Learning UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/learning-uib.md)
-   [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)
-   [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

