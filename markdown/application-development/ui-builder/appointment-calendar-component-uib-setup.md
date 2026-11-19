---
title: Appointment Calendar component setup
description: The Appointment Calendar component enables you to visualize time-related events in various calendar views.Configure the Appointment Calendar time and date formats with these properties.Select event handlers to configure the events provided with the Appointment Calendar component. Event handlers work with data resources to link the Appointment Calendar actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/appointment-calendar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 11
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Appointment Calendar component setup

The Appointment Calendar component enables you to visualize time-related events in various calendar views.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Appointment Calendar that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "appointment-calendar-content-tree.png"\] Alt text: Appointment Calendar content tree.

2.  Select the Appointment Calendar component, using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the Appointment Calendar label that you created for your component in the content tree.
    The properties appear in the Config tab in the setup panel on the right.\[Omitted image "appointment-calendar-props.png"\] Alt text: Shows the configuration properties for the Appointment Calendar component


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Appointment Calendar component properties

Configure the Appointment Calendar time and date formats with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_bb3_rfz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[appTitle\]

</td><td>

Title of the appointment booking.

</td></tr><tr><td>

View\[view\]

</td><td>

View to display when the appointment calendar loads.Available choices:

-   **Day**: Displays the day with corresponding date in a selected month.
-   **Week**: Displays the week containing the configured selected date.

Default: **Day****Note:** This property only impacts the view shown when the calendar loads. Users can switch between the day and week view if you enable **Show View selector**.

</td></tr><tr><td>

Time zone\[timezone\]

</td><td>

Time zone to display in the calendar. This property's configuration impacts the time and date displayed in the calendar.Some of the available options are:

-   America/Argentina/Jujuy
-   America/Argentina/La\_Rioja
-   America/Argentina/Mendoza
-   America/Edmonton
-   America/Ensenada
-   America/Fort\_Nelson
-   Asia/Calcutta
-   Asia/Chita
-   Asia/Chongqing
-   Asia/Gaza
-   Asia/Harbin
-   Asia/Hebron
-   Atlantic/Azores
-   Atlantic/Bermuda
-   Atlantic/Canary
-   Atlantic/Cape\_Verde
-   Australia/ACT
-   Australia/Adelaide
-   Australia/Brisbane
-   Australia/Broken\_Hill
-   CET
-   CST6CDT
-   Canada/Atlantic
-   Canada/Central
-   Canada/Eastern
-   EET
-   EST
-   EST5EDT
-   Egypt
-   Eire
-   Etc/GMT
-   Etc/GMT+0
-   Europe/Amsterdam
-   Europe/Andorra
-   Europe/Astrakhan
-   Europe/Athens
-   GMT
-   MST
-   MST7MDT
-   Mexico/BajaNorte
-   Mexico/BajaSur
-   Mexico/General
-   NZ
-   NZ-CHAT
-   Navajo
-   PRC
-   PST8PDT
-   Pacific/Apia
-   Pacific/Auckland
-   US/Mountain
-   US/Pacific
-   US/Samoa
-   UTC
-   Universal
-   W-SU
-   WET
-   Zulu

Default: **GMT**

</td></tr><tr><td>

Locale\[locale\]

</td><td>

Language in which to display the calendar.Some of the available options are:

-   en
-   af
-   ar-dz
-   ar-kw
-   ar-ly
-   en-au
-   en-ca
-   en-gb
-   eu
-   fa
-   fi
-   fil
-   fo
-   fr-ca
-   fr-ch
-   fr
-   ku
-   ky
-   lb
-   lo
-   oc-lnc
-   pa-in
-   pl
-   pt-br
-   tl-ph
-   tlh
-   tr
-   tzl
-   tzm-latn
-   uk
-   ur
-   uz-latn
-   x-pseudo
-   yo
-   zh-cn
-   zh-hk
-   zh-mo
-   zh-tw

Default: **en**

</td></tr><tr><td>

Selected date\[contextDate\]

</td><td>

Starting contextual date to show in the calendar.Supported formats:

-   UTC MS
-   ISO \(YYYY-MM-DD\)
-   GlideDate internal format \(yyyy-MM-dd HH:mm:ss\)
-   Moment \(moment object\)

Default: **2023-07-05**

**Note:** The default value in this field is to indicate the supported format. Update it based on your requirements when configuring the component.

</td></tr><tr><td>

Calendar entries\[events\]

</td><td>

Array of appointments. Edit the objects in the array based on your requirements.Object structure:

-   `start`: Start date and time range of the event slot.

Format: YYYY-MM-DD HH:mm:ss

-   `end`: End date and time range of the event slot.

Format: YYYY-MM-DD HH:mm:ss

-   `type`: Slot type.

Choices:

    -   `available`
    -   `unavailable`
    -   `selected`
-   `category`: Unique identifier for the category object \(category ID\). Use number or string.
-   `hasConflict`: Availability status.

Choices:

    -   `true`
    -   `false`
-   `tooltip`: Hover text to display for the event slot.
-   `title`: Label to display for the event slot.
-   `primaryInfoData`: Contextual tag to display in the time slot. You can use up to two of the following tags.

Choices:

    -   `label`: Tag label
    -   `color`: Label color
    -   `icon`: Tag icon
-   `secondaryInfoData`: Additional information to display in the event slot. Supports a maximum of one secondary tag - `label`.

Default:

```json
[
                           
    {
        "start": "2023-07-05 08:00:00",
        "end": "2023-07-05 10:00:00",
        "type": "available",
        "primaryInfoData": [
            {
                "color": "warning",
                "icon": "clock-outline"
            },
            {
                "color": "critical",
                "icon": "clock-outline"
            }
        ]
    },
    {
        "start": "2023-07-05 10:00:00",
        "end": "2023-07-05 12:00:00",
        "type": "unavailable",
        "category": "morning",
        "hasConflict": true
    },
    ...
    ...
        "start": "2023-07-01 12:00:00",
        "end": "2023-07-01 14:00:00",
        "type": "unavailable",
        "category": "afternoon"
    },
    {
        "start": "2023-07-01 14:00:00",
        "end": "2023-07-01 16:00:00",
        "type": "unavailable",
        "category": "afternoon"
    },
    {
        "start": "2023-07-15 08:00:00",
        "end": "2023-07-15 10:00:00",
        "type": "available"
    }
]
```

**Note:** The default value is to indicate the supported format, structure, and properties. Update it based on your requirements when configuring the component.

</td></tr><tr><td>

Next available slot\[nextAvailableEvent\]

</td><td>

Next available event outside the view range as a JSON object.Object structure:

-   `start`: Start date and time range of the event slot.

Format: YYYY-MM-DD HH:mm:ss

-   `end`: End date and time range of the event slot.

Format: YYYY-MM-DD HH:mm:ss


Default:

```json
{
    "start": "2023-07-15 08:00:00",
    "end": "2023-07-15 10:00:00",
    "title": "Title for next event"
    }
```

**Note:** The default value in this field is to indicate the supported format, structure, and properties. Update it based on your requirements when configuring the component.

</td></tr></tbody>
</table><table id="table_bds_tfz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Date format\[dateFormat\]

</td><td>

Format for display dates.Supported formats:

-   MMMM D, YYYY
-   D MMMM, YYYY
-   MMMM DD, YYYY
-   DD MMMM, YYYY
-   YYYY-DD-MM
-   YYYY-MM-DD
-   DD-MM-YYYY
-   MM-DD-YYYY

Default: **MMMM D, YYYY**

</td></tr><tr><td>

Apply selected date format to all dates \[applyDateFormatGlobally\]

</td><td>

To apply the selected date format to all dates displayed in the calendar, set to **true**.Default: **false**

</td></tr><tr><td>

Time format\[timeFormat\]

</td><td>

Format in which to display the time.Available options are:

-   HH:mm
-   hh:mm A
-   hh:mm a

Default: **hh:mm A**

</td></tr><tr><td>

First day of the week\[firstDayOfWeek\]

</td><td>

Day to show as the first day of the week in the date-time picker and the week view.Available options are:

-   Sunday
-   Monday
-   Tuesday
-   Wednesday
-   Thursday
-   Friday
-   Saturday

Default: **Sunday**

</td></tr><tr><td>

Enable categories\[enableCategories\]

</td><td>

To show appointment slot categories in the calendar, set to **true**. Default: **false**

</td></tr><tr><td>

Categories\[categories\]

</td><td>

Slot categories to display in the calendar. All slots are automatically distributed to the categories based on the configuration of this JSON array.Array properties:

-   `id`: Unique identifier for the category
-   `label`: Category label
-   `order`: Order of the category among the other categories
-   `icon`: Icon to use for the category

Default:

```json
[
    {
        "id": "morning",
        "order": 1
    },
    {
        "id": "afternoon",
        "order": 2
    },
    {
        "id": "evening",
        "order": 3
    },
    {
        "id": "night",
        "order": 4
    },
    {
        "id": "other"
    }
]
```

**Note:** `other` ID is for events that do not have a designated category value set. In such cases, you can overwrite the label from "Other" with another value and icon. Ensure that you also include values for `order`, `label`, and `icons` for such categories as needed.

</td></tr><tr><td>

Show View selector\[showViewSelector\]

</td><td>

To display the view selector in the calendar header, set to **true**.View selector enables the user to switch between day and week view in the calendar. Current calendar configurations are automatically applied to the selected view.

Default: **false**

</td></tr><tr><td>

Show slot duration\[showDurationInEvents\]

</td><td>

To display the duration of each event slot, set to **true**.If set to **true**, the slot duration displays in each slot pill. Enable this property if slots have varying durations.

Default: **false**

</td></tr><tr><td>

Do not show time duration \[disableTimeDuration\]

</td><td>

To hide the time duration from both the calendar header and appointment slot pills, set to **true**.Default: **false**

</td></tr><tr><td>

Show end time in slot\[showEndTimeInEvents\]

</td><td>

To display the end time \(in addition to the start time\) in each appointment slot pill, set to **true**.Default: **false**

</td></tr><tr><td>

Select multiple slots\[enableMultiSelectSlot\]

</td><td>

To enable the user to select multiple event slots, set to **true**.Default: **false**

</td></tr><tr><td>

Row slot count\[numberOfEventsInEachRow\]

</td><td>

Number of event slots to show in each row in the day view. Maximum allowed value is **5** and the minimum value is **1**.

 Configure based on the typical width of smaller screens. This property impacts how event titles and contextual information are displayed. Displaying fewer slots in each row enables displaying the event text with minimal truncation or wrapping.

 Default: **5**

</td></tr></tbody>
</table><table id="table_wht_5fz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable previous slots\[disablePreviousSlotDates\]

</td><td>

To disable all dates before the current date in the mini-calendar and mark all previous events as unavailable, set to **true**. Enabling this property also marks all available slots before the current slot as unavailable.Default: **false**

</td></tr><tr><td>

Disable non available dates\[disableNonAvailableSlotDates\]

</td><td>

To disable all dates where there are no available slots in the date-time picker, set to **true**.Default: **false**

</td></tr></tbody>
</table><table id="table_gcy_vfz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configure ARIA\[configAria\]

</td><td>

ARIA labels for the calendar.-   `ariaTitle`: ARIA title for the entire Calendar.
-   `ariaBodyTitle`: ARIA title for the section under the header.

Default:

```
{"ariaTitle": "Appointment calendar", "ariaBodyTitle": "Appointment calendar"}
```

</td></tr></tbody>
</table><table id="table_idw_wfz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable padding\[bare\]

</td><td>

To disable the padding \(8px\) around the calendar, set to **true**.**Note:** To configure other style elements like shadow, width, and so on, select the **Style** tab.

Default: **false**

</td></tr></tbody>
</table><table id="table_yxl_xfz_bfc"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable truncation\[disableTruncation\]

</td><td>

Applies to screen sizes lower than 640px.To wrap text instead of truncating it when the characters exceed screen width, set to **true**.

Default: **false**

</td></tr></tbody>
</table>## Appointment Calendar component events

Select event handlers to configure the events provided with the Appointment Calendar component. Event handlers work with data resources to link the Appointment Calendar actions to the data you want to display to your users.

The Events tab shows the events used by the Appointment Calendar component. Events with presets are marked with the **Preset** badge. To show events that don’t have preset configurations, select **+ Add event mapping**. If the component has only one event and that event doesn’t have a preset, the event is displayed and is ready for configuration.\[Omitted image "appointment-calendar-events.png"\] Alt text: Shows the events for the Appointment Calendar component

### Event handlers

Event handlers work with data resources to link the Appointment Calendar actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Event descriptions

<table id="table_ajl_1vv_rnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cancel selected

</td><td>

Triggers when the user selects the **Cancel** button.

</td></tr><tr><td>

Context date changed

</td><td>

Triggers when the current selected date changes on the calendar.Payload:

-   `fromMoment`: Old selection date, as a moment object.
-   `fromMS`: Old selection date in UTC milliseconds.
-   `toMoment`: New selection date as a moment object.
-   `toMS`: New selection date in UTC milliseconds.

Payload type:

```json
{fromMoment: Moment, toMoment: Moment, fromMS: number, toMS: number}
```

</td></tr><tr><td>

Event selected

</td><td>

Triggers when the user selects an event.Payload:

-   `event`: Event object that is selected.
-   `chunkStartDateMoment`: Moment object with the start date of the selected part of the event.
-   `chunkEndDateMoment`: Moment object with the end date of the selected part of the event.
-   `chunkStartDateMS`: Start date of the selected part of the event in UTC milliseconds.
-   `chunkEndDateMS`: End date of the selected part of the event in UTC milliseconds.

Payload type:

```json
{event: Object, chunkStartDateMoment: Moment, chunkEndDateMoment: Moment, chunkStartDateMS: number, chunkEndDateMS: number}
```

</td></tr><tr><td>

Propose appointment slots

</td><td>

Triggers when the user proposes a slot for appointment.Payload: `events`. An array object with the selected events.

Payload type:

```
(events: Array<Object>)
```

</td></tr><tr><td>

Range updated

</td><td>

Triggers when the range of visible dates on the calendar change.Payload:

-   `startMoment`: Start date seen in view as a moment object.
-   `endMoment`: End date seen in view as a moment object.
-   `startMS`: Start date seen in view in UTC milliseconds.
-   `endMS`: End date seen in view in UTC milliseconds.

</td></tr><tr><td>

Reschedule appointment

</td><td>

Triggers when the appointment is rescheduled.Payload:

-   `startMoment`: Start date seen in view as a moment object.
-   `endMoment`: End date seen in view as a moment object.
-   `startMS`: Start date seen in view in UTC milliseconds.
-   `endMS`: End date seen in view in UTC milliseconds.

Payload type:

```json
{startMoment: Moment, endMoment: Moment, startMS: number, endMS: number}
```

</td></tr><tr><td>

Schedule appointment

</td><td>

Triggers when an appointment event is scheduled.Payload: `event`. Object that represents the event chosen. For example, start, end, type.

Payload type:

```
{event: Object}
```

</td></tr><tr><td>

View updated

</td><td>

Triggers when the user changes the view.Payload:

-   `from`: Previous view
-   `to`: Current view

</td></tr></tbody>
</table>