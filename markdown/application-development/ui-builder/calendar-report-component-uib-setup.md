---
title: Calendar Report component setup
description: The Calendar Report component enables you to visualize date-driven events in selected view formats.Configure the Calendar Report properties.Select event handlers to configure the actions \(events\) provided with the Calendar Report component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/calendar-report-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Calendar Report component setup

The Calendar Report component enables you to visualize date-driven events in selected view formats.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## About this task

You can limit the number of events that may be returned when you browse backwards in a calendar visualization. There is a limit of 30 days into the past, starting from the first day in the current calendar view. Events that start more than 30 days before the first day visible on a calendar are not displayed. If you select **Year**, then the calendar includes events that start between December 1 of the previous year and December 31 of the current year.

The KB article [Weekly calendar view does not display all entries](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0598360) covers scenarios in which some expected entries do not display.

To show more or fewer days, edit the **glide.report.calendar.max\_days\_back** property. See [Reporting properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting-properties.md).

**Note:** Performance may degrade if this value is too large.

## Procedure

1.  Define a label for your Calendar Report that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "calendar-report-content-tree.png"\] Alt text: Calendar Report content tree.

2.  Select the Calendar Report component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Calendar Report label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Calendar Report component properties

Configure the Calendar Report properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="id_vn5_t1q_3qb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="3">

Component Header

</td></tr><tr><td>

Component title

</td><td>

componentTitle

</td><td>

Title you enter for the component.

</td></tr><tr><td>

Heading level

</td><td>

headingLevel

</td><td>

HTML heading tag level of the header title \(H1 to H6\)Default: H2

</td></tr><tr><td>

Use large font size

</td><td>

headingVariant

</td><td>

Defines the styles used to render the header title. When true, the non-bold Title-tertiary font is used. Otherwise, the bold Header-secondary font is used.Default: false

</td></tr><tr><td>

Component description

</td><td>

componentDescription

</td><td>

Description you enter for the component. This field has a limit of 250 characters.

</td></tr><tr><td>

Show description

</td><td>

showDescription

</td><td>

Adds an information icon \(\[Omitted image "icon-info.png"\] Alt text: Information icon\) to the visualization. This icon opens the component description in a popup.Default: true

</td></tr><tr><td colspan="3">

Data

</td></tr><tr><td>

Table

</td><td>

table

</td><td>

The table or database view with the records you want to show in a calendar.Default value: task

</td></tr><tr><td>

Predefined conditions

</td><td>

reportSource

</td><td>

A predefined condition from the Report Source \[sys\_report\_source\] table to use to filter the table. This filter is applied when the end user views the calendar. Users can filter further if a filter component is added to the page. **Note:** Report sources determine predefined conditions in the list. Select a predefined condition that matches the selected table or database view. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/c_ReportSources.md).

</td></tr><tr><td>

Edit filter table

</td><td>

encodedQuery

</td><td>

Conditions for filtering records. This filter is applied when the end user views the calendar. Users can filter further if a filter component is added to the page. **Note:** This property adds a filter condition in addition to the table and predefined conditions, if any are applied.

</td></tr><tr><td>

Start date field

</td><td>

startDateField

</td><td>

Field from the record to display as the starting event. You must select a date field. Default value: Opened \[opened\_at\]

</td></tr><tr><td>

End date field

</td><td>

endDateField

</td><td>

Field to report on as the ending event. You must select a date field. Default value: Closed \[closed\_at\]

</td></tr><tr><td>

Event display fields

</td><td>

eventDisplayFields

</td><td>

One or more fields you select to appear on all calendar events.Default value: number,short\_description

</td></tr><tr><td colspan="3">

Additional settings

</td></tr><tr><td>

Follow filters

</td><td>

followFilters

</td><td>

Choose whether to apply filters set on the dashboard or UI Builder page to this component.Default value: true

</td></tr><tr><td>

Show filter overview

</td><td>

showFilterOverview

</td><td>

Shows the icon for the Filter overview panel. This panel shows configuration filters, such as "Active is true," and any filters on the page that are being followed. Does not show predefined conditions.Default value: true

</td></tr><tr><td>

Default view

</td><td>

viewType

</td><td>

The calendar view format to apply as the default. Choose from:-   Day
-   Week
-   Work Week
-   Month

 Default value: Month

</td></tr></tbody>
</table>## Calendar Report component events

Select event handlers to configure the actions \(events\) provided with the Calendar Report component.

The Events tab shows the events used by the Calendar Report component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

The Events tab shows the events used by the Calendar Report component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

|Event|Description|
|-----|-----------|
|Event clicked|Action that is dispatched when a Calendar event is clicked.|

