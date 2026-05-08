---
title: Next Experience Components release notes
description: The ServiceNow Next Experience Components application provides the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
---

# Next Experience Components release notes

The ServiceNow® Next Experience Components application provides the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Australia release.

## Next Experience Components highlights for the Australia release

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Horizon site Components section](https://horizon.servicenow.com/workspace/components).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so that the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see Automatically configure components using presets and Bind data to UI Builder pages using controllers \(advanced feature\).

## New in the Australia release

|Component|Description|
|---------|-----------|
|Activity timer|Tracks time spent on an activity, such as working on a record, and creates time log entries for reporting.|
|Card data security container|Provides secure, encrypted handling of card details and supports uploading and viewing sensitive documents.|
|Contextual sidebar|Sidebar that enables users to initiate real-time collaboration through chats and calls to resolve tasks.|
|Grouped button|Multiple related buttons presented in a unified layout. Interactions for the component are similar to that of button stateful.|
|Sheet|Container that slides in from the edge of the screen to present related content or actions, designed for mobile experiences.|

|Template|Description|
|--------|-----------|
|Dashboard library|Includes all dashboards available to users. Users can filter dashboards by various criteria, such as recently opened, bookmarked, certified, by category, and ones the user owns. The Library section also lets users create dashboards. Users with analytics admin roles have an enhanced library view, enabling them to access usage data and other metadata. Admins can also deactivate, activate, or delete dashboards from this view.|
|Data visualization library|Includes all data visualizations available to users. Users can filter dashboards by various criteria, such as bookmarked, certified, and ones that the user owns. The Library section also lets users create dashboards. Users with analytics admin roles have an enhanced library view, enabling them to access usage data and other metadata. Admins can also deactivate, activate, or delete dashboards from this view.|

## Changed in this release

<table id="table_comp_list"><thead><tr><th>

Component

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Activity Stream

</td><td>

-   Enable users to edit or delete journal posts.
-   Add a dropdown with check boxes for author names using the Posted by filter that enables users to filter posts by author, select all, or clear all. Users can also filter for any AI-generated posts.

</td></tr><tr><td>

Alert

</td><td>

-   Enable keyboard focus to move to the alert when it appears.
-   Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Alert list

</td><td>

Enable keyboard focus to move to the **Show alerts** button when the alert list appears.

</td></tr><tr><td>

Button

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Button iconic

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Button circular

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Calendar

</td><td>

-   Hide time zone dropdown in the calendar header.
-   Hide time lapsed indicator or time zone indicators.
-   Add section-based time zones.

</td></tr><tr><td>

Card base container

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Checklist

</td><td>

-   Edit or delete items on hover.
-   Edit checklist items inline.
-   Edit, delete, and reorder checklist items.
-   Configure empty state checklists to add new items.

</td></tr><tr><td>

Dropdown

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Dropdown list

</td><td>

The mobile version uses the sheet component instead of a popover.

</td></tr><tr><td>

Form

</td><td>

-   Place each form field label in line with the input field and adjacent to other field labels using the “Tabbed” \(horizontal\) layout.
-   Highlight form fields with unsaved changes using a background color, in addition to the existing field indicator, which is now selected by default.

</td></tr><tr><td>

Form Templates

</td><td>

-   Show that the preview option displays modal preview to help agents understand all the fields affected when they apply a particular template.
-   Alert to inform users if a template has already been applied to a record.

</td></tr><tr><td>

Highlighted value

</td><td>

-   Enter additional text to display in a popover when the highlighted value is selected.
-   Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Icon

</td><td>

Support for theme-specific custom icon uploads.

</td></tr><tr><td>

Input

</td><td>

Display persistent placeholder text to guide users in entering data in the correct format.

</td></tr><tr><td>

Kanban

</td><td>

Use keyboard shortcuts to drag and drop cards between columns and rows.

</td></tr><tr><td>

List selector

</td><td>

Disable the selection feature for a chosen array of list selector items.

</td></tr><tr><td>

Node map

</td><td>

-   Use radial layout to arrange nodes in a ring-like pattern.
-   Use content slots to add components.
-   Disable node dragging.

</td></tr><tr><td>

Schedule recurrence

</td><td>

-   Automatically update all recurring events in a series.
-   Fill in event details using AI.

</td></tr><tr><td>

Split button

</td><td>

Add AI variants with updated color palettes for generative AI workflows.

</td></tr><tr><td>

Tabs

</td><td>

Hide padding on the sides of each tab for horizontal \(Top\) tab position, to provide more room for additional tabs.

</td></tr></tbody>
</table><table id="table_data_visualizations"><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Bar \(including Pareto\)

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Removed the display setting for Height, which can be configured in the **UI Builder Styles** tab.
-   Align title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Box plot

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Bubble

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Dial

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Gauge

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Geomap

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Heatmap

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Indicator Scorecard

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.

</td></tr><tr><td>

Pie/Donut

</td><td>

-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Pivot table

</td><td>

-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Single score

</td><td>

-   Align the title horizontally to the Start, Center, or End. The default is Start.
-   Wrap chart elements instead of truncating.
-   Align the title horizontally to the **Start**, **Center**, or **End**. Default is **Start**.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr><tr><td>

Time series

</td><td>

-   Removed the display setting for Height, which can be configured in the **UI Builder Styles** tab.
-   Show or hide a tooltip that displays on hover showing the percentage of total for a data point.
-   Align the title horizontally to the **Start**, **Center**, or **End**. The default is **Start**.
-   Align all chart content to the starting edge, center, or ending edge of the visualization.
-   Set the line of truncation to 2 or 3 lines instead of truncating long titles after 1 line.
-   Wrap long titles to a second line, instead of truncating.
-   Hide the refresh action that is available to users in the More options menu.
-   Show incomplete periods for a data snapshot indicator when selecting Metric.
-   Enable Auto aggregation to have the most appropriate aggregation level determined based on the selected date range, applied date filters, or data availability.

</td></tr></tbody>
</table>|App shell|Enhancement|
|---------|-----------|
|Agent Workspace app shell|Configure alt text for a ServiceNow or customer logo button.|

## Deprecations

|UI Element|Description|
|----------|-----------|
|Dashboard overview template|Moved under "Legacy templates" and renamed to "Deprecated - Dashboard overview." This template can still be used, but you should use the new "Dashboard library" template instead, because the Dashboard overview template is marked for eventual deprecation.|

## Activation information

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

## Plugin information

The following plugins are planned for deprecation in a future release.

sn-component-account-hierarchy \(com.sn\_component\_account\_hierarchy\): Planned for deprecation in the C release. Beginning with the Australia release, this plugin migrate to a store application. Upgrade your instance to Australia or later release versions and the store applications automatically installs.

## Accessibility information

To view Next Experience Components accessibility conformance information, refer to the components section of the [Horizon site Components section](https://horizon.servicenow.com/workspace/components). The Overview for each component contains accessibility \(A11y\) information.

## Related ServiceNow applications and features

-   **UI Builder**

    UI Builder is a low-code tool that helps enable you to build pages for workspace and portal web-based experiences.

-   **Configurable Workspace UI**

    Use components to build custom workspace experiences for agents who solve internal or external customer issues.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

