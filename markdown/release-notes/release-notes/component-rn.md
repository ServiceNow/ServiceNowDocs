---
title: Next Experience Components release notes
description: The ServiceNow Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Next Experience Components release notes

The ServiceNow® Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Yokohama release.

## Next Experience Components highlights for the Yokohama release

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## New in the Yokohama release

|Component|Description|
|---------|-----------|
|Active call|Handles phone calls as part of the Interaction controls component \(ICC\). Manages call functions, including actions such as disconnect, mute, hold, record, and transfer.|
|Animation|Places Lottie animations in Next Experience pages or components created in UI Builder.|
|Dialpad|Dial a phone number in Workspace.|
|Feedback|Captures detailed feedback from users for AI products or skills through a series of pre-determined options or free-text responses.|
|Filter group|Groups up to 3 filter components into a single container with configurable **Apply**, **Clear**, and **Reset** buttons that apply to all filters in the group.|
|Flyout menu|Menu that organizes multiple levels of options within a hierarchical structure.|
|Knowledge view|Embeddable container that renders a Next Experience Knowledge article view.|
|Loader custom|Renders custom animations with an optional progress bar and label.|
|Skeleton loader|Decorative placeholder for generated content.|

## Changed in this release

<table id="table_qvp_xdg_zcd"><thead><tr><th>

Component

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

-   Select multiple slots
-   Add customizable categories for appointment slots
-   Hide past and unavailable slots
-   Add contextual tags in appointment slots
-   Configure number of rows displayed in each slot in the Day and DAYMOBILE views
-   Configure container height adjustment

</td></tr><tr><td>

Attachments

</td><td>

-   Option to download all attachments
-   Revised delete attachment confirmation popup message

</td></tr><tr><td>

Avatar

</td><td>

Configure avatar to behave as a button or a link.

</td></tr><tr><td>

Calendar

</td><td>

-   DST support with multiple time zones in the Calendar and Timeline views
-   Hide header
-   Multiple time zones in the Timeline view
-   Scroll control for the Calendar and Timeline views

</td></tr><tr><td>

Email composer

</td><td>

Now Assist generative AI suggestions for all email scenarios, email templates, response templates, and quick messages.

</td></tr><tr><td>

Email composer \(mini\)

</td><td>

Now Assist generative AI suggestions for all email scenarios, email templates, response templates, and quick messages.

</td></tr><tr><td>

Form

</td><td>

-   Configuration panel updates
-   Form controller configuration panel updates

</td></tr><tr><td>

Form templates

</td><td>

-   Sort templates alphabetically and by last used.
-   New tab for Favorites for you to add and remove templates.
-   Larger cards that don't truncate template name and description, and show Last used timestamp.

</td></tr><tr><td>

Highlighted value

</td><td>

-   Medium size variant.
-   Custom tooltip property.

</td></tr><tr><td>

iFrame

</td><td>

Send messages to iframed document.

</td></tr><tr><td>

Kanban Board

</td><td>

-   Multi-select in cards
-   Configure selecting dependency lines
-   Add secondary header

</td></tr><tr><td>

Modeless dialog

</td><td>

Make the dialog dynamic and automatically resize to fit the content.

</td></tr><tr><td>

Node Map

</td><td>

-   Force layout for representing graphs without structure or hierarchy
-   Custom popover configuration in Hierarchical, Layered, and Force layouts
-   Customizable nodes in non-unified layouts
-   Self-referencing nodes denoted with edges looping back to the node
-   Export maps in JPG and PNG
-   Aggregate or segregate multiple connections between the same nodes

</td></tr><tr><td>

Pill

</td><td>

Display the selected pill state which doesn't display by default.

</td></tr><tr><td>

Quick filter

</td><td>

-   Configure section headers in typeahead dropdown
-   Configure footer action button
-   Configure placeholder text value for input field

</td></tr><tr><td>

Record lookup

</td><td>

-   Search for contacts by name, phone, or email
-   Preview shortlisted results in a paginated form
-   Quickly link or unlink a shortlisted contact to a case
-   Edit details for a record without accessing the parent record
-   Hide record header
-   Configure search results
-   Render highlighted values in the linked card
-   Qualify search results using specific conditions \(reference qualifiers\)
-   Hide fields with empty values
-   Hide link button
-   Expand or collapse card

</td></tr><tr><td>

Stepper

</td><td>

-   Standardized font size \(small or medium\) for all steps
-   By default, pagination adjusts to display the current selected step

</td></tr></tbody>
</table><table id="table_eqq_1fg_zch"><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Bar

</td><td>

Percent \(%\) information added to chart tooltips and data table below chart.

</td></tr><tr><td>

Bubble

</td><td>

Percent \(%\) information added to chart tooltips.

</td></tr><tr><td>

Geomap

</td><td>

Percent \(%\) information added to chart tooltips and data table below chart.

</td></tr><tr><td>

Heatmap

</td><td>

-   Percent \(%\) information added to chart tooltips and data table below chart.
-   When the metric value is set to "Count," show a zero \(0\) when no data is available.

</td></tr><tr><td>

Pivot table

</td><td>

-   When there's no value in the selected dataset or for the configuration, choose the display format.
-   Data sources limit increased from 10 to 15.

</td></tr><tr><td>

Time series

</td><td>

-   Percent \(%\) information added to chart tooltips and data table below chart.
-   Support for business calendars such as Gregorian, fiscal, and any manually added calendar.
-   For all chart formats, except "column:"
    -   When there's no value in the selected dataset or for the configuration, choose the display format.
    -   For table data sources, when there's no data for a specific time on the chart, show a continuous line without gaps.
-   Show a chart and graph data table for easier screen reader access.
-   For line, spline, area, and step charts, have a marker show at each data point on the chart including where values are zero \(0\) or missing.
-   For a chart with up to 3 metrics, you can add alternative Group by's for each metric for the user to select from.
-   Sorting when data is grouped.
-   New Date range option to set the period end date to update automatically to the current date.

</td></tr></tbody>
</table><table id="table_y2f_x1z_4dc"><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dashboards

</td><td>

-   Pills at the top of the page display any categories assigned to the dashboard
-   User avatars at the top of the page indicate real-time editing

</td></tr></tbody>
</table><table id="table_cr1_bfg_zce"><thead><tr><th>

Bundle

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Record list

</td><td>

-   Condition builder available in the list header
-   If live list is enabled, infinite scrolling is enabled by default

</td></tr></tbody>
</table>## Activation information

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

For Next Experience Components accessibility conformance, refer to the ServiceNow [Horizon site Components section](https://horizon.servicenow.com/workspace/components).

## Related ServiceNow applications and features

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    UI Builder is a low-code tool that enables you to build pages for workspace and portal web-based experiences.

-   **[Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    Use components to build custom workspace experiences for agents who solve internal or external customer issues.


**Parent Topic:**[Features and changes by product](../new-features-changes.md)

