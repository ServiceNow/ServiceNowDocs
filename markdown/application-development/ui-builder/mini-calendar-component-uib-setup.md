---
title: Mini Calendar component setup
description: The Mini Calendar component is used for calendars in which a user must select a specific date and time. Examples might be a date range, a calendar month or day view, or an appointment date.Configure the basic format for the Mini Calendar component and what features are displayed. This includes the optional time field.Select event handlers to configure the events provided with the Mini Calendar component. Event handlers work with data resources to link the Mini Calendar actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/mini-calendar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Mini Calendar component setup

The Mini Calendar component is used for calendars in which a user must select a specific date and time. Examples might be a date range, a calendar month or day view, or an appointment date.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Mini Calendar that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "mini-calendar-content-tree.png"\] Alt text: Shows the mini calendar component in the UI Builder content tree

2.  Select the Mini Calendar component using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your component in the content tree.
    The configuration options appear in the panel on the right.

    \[Omitted image "mini-calendar-properties.png"\] Alt text: Shows the available properties for the mini calendar component in the Config panel


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Mini Calendar component properties

Configure the basic format for the Mini Calendar component and what features are displayed. This includes the optional time field.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_ldn_zt5_25b"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Autofocus\[autofocus\]

</td><td>

Configures component to receive focus on mounting when set to **true**.Default: **false**

</td></tr><tr><td>

Description\[description\]

</td><td>

Additional content describing the field. Use this content to provide further instructions to the user.

</td></tr><tr><td>

First Day of Week\[firstDayOfWeek\]

</td><td>

Day of the week on which the calendar starts.Possible values are:

-   Sunday=0
-   Monday=1
-   Tuesday=2
-   Wednesday=3
-   Thursday=4
-   Friday=5
-   Saturday=6

</td></tr><tr><td>

Format\[format\]

</td><td>

Format describing how to format the date/time values. By default it is **YYYY-MM-DD** or **YYYY-MM-DD hh:mm:ss**, depending on whether you are showing a time picker.

</td></tr><tr><td>

Invalid\[invalid\]

</td><td>

Specifies whether the current value is not valid.

</td></tr><tr><td>

Label\[label\]

</td><td>

A label for the calendar.

</td></tr><tr><td>

Language\[language\]

</td><td>

User's preferred language.Default: **en**

</td></tr><tr><td>

Messages\[messages\]

</td><td>

Array of message objects that must contain the message and message type.

</td></tr><tr><td>

Name\[name\]

</td><td>

Name for the calendar. Any events dispatched by the calendar use this name.

</td></tr><tr><td>

ReadOnly\[readOnly\]

</td><td>

Specifies that the user cannot modify the value of the calendar.Default: **false**

</td></tr><tr><td>

Required\[required\]

</td><td>

Specifies if the user is required to supply a value for this calendar.Default: **false**

</td></tr><tr><td>

Reversed\[reversed\]

</td><td>

Specifies that the field should be rendered from right-to-left.Default: **false**

</td></tr><tr><td>

Show 'Ok' Button\[onOk\]

</td><td>

Specifies whether or not to show the **Ok** button.Default: **false**

</td></tr><tr><td>

Show 'Cancel' Button\[onCancel\]

</td><td>

Specifies whether or not to show the **Cancel** button.Default: **false**

</td></tr><tr><td>

Show Time Picker\[timePicker\]

</td><td>

Specifies whether or not to show the time picker, in addition to the calendar.Default: **false**

</td></tr><tr><td>

Value\[value\]

</td><td>

Underlying data for the component.

</td></tr></tbody>
</table>## Mini Calendar component events

Select event handlers to configure the events provided with the Mini Calendar component. Event handlers work with data resources to link the Mini Calendar actions to the data you want to display to your users.

The Events tab shows the events used by the Mini Calendar component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Mini Calendar actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

On Ok Click

</td><td>

The user selects the **Ok** button.Payload:

-   `name`
-   `event`

</td></tr><tr><td>

On Cancel Click

</td><td>

The user selects the **Cancel** button.Payload:

-   `name`
-   `event`

</td></tr><tr><td>

OnValueChange

</td><td>

The user selects a new value on the calendar.Payload includes: `value`

</td></tr></tbody>
</table>