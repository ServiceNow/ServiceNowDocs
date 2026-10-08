---
title: Schedule pages
description: A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.To access schedule pages, navigate to System Scheduler Schedules Schedule Pages .A Timeline Schedule Page is a specific record that contains configuration information for displaying time based points and spans in a "timeline" like fashion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/scripts/c\_SchedulePages.html
release: brazil
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Write server-side scripts, Scripting, API implementation, API implementation and reference]
---

# Schedule pages

A schedule page is a record that contains a collection of scripts that allow for custom generation of a calendar or timeline display.

Creation of timeline schedule pages requires understanding of the page/event flow and the ability to write client and server side JavaScript.

**Parent Topic:**[Writing server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/scripts/server-side-scripting-overview.md)

## Schedule pages form

To access schedule pages, navigate to **System Scheduler** &gt; **Schedules** &gt; **Schedule Pages**.

The form provides the following fields, depending upon the View Type selected:

<table id="table_i4p_34j_lp"><thead><tr><th>

Field

</th><th>

Field Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

String

</td><td>

General name that is used to identity the current schedule page.

</td></tr><tr><td>

Schedule type

</td><td>

String

</td><td>

The schedule type is a string that is used to uniquely identity the schedule page via the "sysparm\_page\_schedule\_type" URI parameter. For example, a schedule page could be accessed as follows: `/show_schedule_page.do?sysparm_type=gantt_chart&sysparm_timeline_task_id=d530bf907f0000015ce594fd929cf6a4`

 Alternatively, the schedule page can also be accessed by setting the "**sysparm\_page\_sys\_id**" URI parameter to that of the unique 32 character hexadecimal system identifier of the schedule page.

</td></tr><tr><td>

View Type

</td><td>

Choice

</td><td>

Each view type displays different field combinations. There are two options available:-   Calendars
-   Timelines

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

General description that provides additional information about the current schedule page. This field is not necessary.

</td></tr><tr><td>

Init funciton name

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The init function name specifies the name of the JavaScript function to call inside the Client script function for calendar type schedule pages.

</td></tr><tr><td>

HTML

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The HTML field is a scriptable section that is parsed by Jelly and injected into the display page prior to the rest of the calendar. It can be used to pass in variables from the server and define extra fields.

</td></tr><tr><td>

Client script

</td><td>

String

</td><td>

The client script is a scriptable section that allows for configuring options of the schedule page display. The API is different depending on the schedule page view type and is discussed below.

</td></tr><tr><td>

Server AJAX processor

</td><td>

String

</td><td>

**Note:** This functionality is only used by Calendar type schedule pages.

The Server AJAX processor is specific to calendar type schedule pages that is used to return a set of schedule items and spans to be displayed.

</td></tr></tbody>
</table>## Timeline schedule pages

A Timeline Schedule Page is a specific record that contains configuration information for displaying time based points and spans in a "timeline" like fashion.

The timeline schedule page references a script include that extends from the AbstractTimelineSchedulePage class to perform dynamic modification to the timeline based on different events and conditions. Both the schedule page and the script include for timeline generation support customization and have a corresponding application programming interface \(API\).

The following steps outline the series of events that occur when a timeline schedule page is accessed. Once the timeline has been loaded, all subsequent events, such as events resulting from timeline interaction \(for example, moving a timeline span\), follow the same logic described with the getItems event.

1.  The client browser accesses a schedule page. The request is sent to the server.
2.  The server interprets the schedule page HTTP request and obtains information about the specific schedule page from either of the following URI parameters:
    -   sysparm\_page\_sys\_id
    -   sysparm\_page\_schedule\_type
3.  The server returns an HTTP response that contains the client script information from the specified schedule page.
4.  The client browser immediately parses the **Client script** section of the schedule page when loading the page and:
    -   sets configuration and display options
    -   registers event listeners
5.  With the getItems event:
    1.  The client timeline makes an AJAX request to the corresponding script include for the event registered with getItems to retrieve the set of items and spans to display on the timeline.
    2.  The server receives the request and executes the getItems code block inside the specified script include, which is an instance of the AbstractTimelineSchedulePage class. The server returns an XML document with TimelineItem objects.
    3.  The client receives the AJAX response with the specified TimelineItem objects and appropriately displays them on the screen.

### Applications that use schedule pages to generate time lines

-   Project Management
-   Maintenance Schedules
-   Group On-Call Rotation
-   Field Service Management

