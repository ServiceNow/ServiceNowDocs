---
title: Combined Next Experience Components release notes for upgrades from Washington DC to Australia
description: Consolidated page of all release notes for Next Experience Components from Washington DC to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-washingtondc-australia/australia-washingtondc-nextexperiencecomponents-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 31
breadcrumb: [Products combined by family]
---

# Combined Next Experience Components release notes for upgrades from Washington DC to Australia

Consolidated page of all release notes for Next Experience Components from Washington DC to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Next Experience Components release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Next Experience Components to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Next Experience Components.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

|Component|Description|
|---------|-----------|
|Color selector|A color library that can be used to search for, select, and save colors. Hexcodes, RGB, and HSL values are accepted, and custom colors can be used.|
|Related Items|Information related to a case record displayed with cards in the side panel and categorized in an expandable accordion. Optionally, the user can display the data as a full-featured list with sorting and filtering capabilities.|

|Template|Description|
|--------|-----------|
|Confirm Publish Modal|Modal used as a page template that enables Knowledge Management users to publish articles to the Knowledge Base.|
|Record page vertical|Page template used to manage related lists and UI pages on a record page within groups. This page template contains preset values that make the page work without requiring complex configuration.|
|Retire Confirmation Modal|Modal used as a page template that enables Knowledge Management users to retire obsolete articles from the knowledge base and select replacement articles.|
|Standard List|Page template built with a record list bundle and a list menu contained in a resizable panes component, all with preset configuration values. Users can export records in different formats and share custom lists with other users. The List Controller used in this page template contains configurable properties.|

|Bundle|Description|
|------|-----------|
|Record list|The record list bundle is a combination of components that include a list header, list body, and pagination component. This new iteration of the list component includes preset configuration values and a list controller.|

</td></tr><tr><td>

Xanadu

</td><td>

|Component|Description|
|---------|-----------|
|Custom illustration|Insert theme-able, inline Scalable Vector Graphics \(SVG\)s on a Workspace page.|
|Feedback|Capture granular user feedback for AI products through a series of pre-determined options or free-text responses.|

</td></tr><tr><td>

Yokohama

</td><td>

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

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

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

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Next Experience Components features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

<table><thead><tr><th>

Component

</th><th>

Enhancements

</th></tr></thead><tbody><tr><td>

Activity Stream

</td><td>

-   Hide the discard draft, pop-out button, create email, and view drafts buttons.
-   Change the send email button style from primary to secondary.
-   Display email subject when there are multiple modeless dialogs or when they are minimized.
-   Insert email template and insert KB link with modeless dialog.

</td></tr><tr><td>

Attachments

</td><td>

New property for defining the maximum allowable size for an attachment.

</td></tr><tr><td>

Date - Time

</td><td>

**Default time** \[initialTime\] property that sets the default start time for the component. If not set, the time defaults to midnight.

</td></tr><tr><td>

Date-Time-interval

</td><td>

Customize the range of dates to display on the calendar using a relative date time picker.

</td></tr><tr><td>

Dropdown

</td><td>

Added a configurable label property.

</td></tr><tr><td>

Email Composer

</td><td>

-   Attach Knowledge articles inline or as PDFs using Agent assist.
-   Auto-save drafts, discard drafts, save, and create drafts.
-   Improved page design density.
-   Added support for Modeless dialog experience.

</td></tr><tr><td>

Email Composer \(mini\)

</td><td>

-   Attach Knowledge articles inline or as PDFs using Agent assist.
-   Auto-save drafts, discard drafts, save, and create drafts.
-   Improved page design density.
-   Support for Modeless dialog experience.

</td></tr><tr><td>

Heading

</td><td>

-   Font header sizes decreased in Workspace to increase data density.
-   Hero heading size alternative to primary for users who still prefer the original, larger heading size.

</td></tr><tr><td>

Icon

</td><td>

Use custom icons in any standard image format. Custom icons aren’t added to the library on the instance and aren’t cached.

</td></tr><tr><td>

Image

</td><td>

Use custom images in any standard image format. Custom icons aren't added to the library on the instance and aren't cached.

</td></tr><tr><td>

Input

</td><td>

AI Indicator signals to users when a form field uses AI recommendations and provides more information about AI functionality.

</td></tr><tr><td>

Kanban board

</td><td>

-   Enable dependency lines to indicate relationships between cards on the board.
-   Show the swimlane header in the row.

</td></tr><tr><td>

List selector

</td><td>

-   Popovers triggered from items in the Available items and Selected items lists display details of the current record. You can configure the content of the popovers and select the items that show the trigger icon.
-   Select how the component is displayed. The choices are as follows:
    -   Compact
    -   2 panels
    -   Dotwalk \(default\)
-   Prevent users from reordering items in the Selected Items list.
-   Reveal all hidden controls inside the component.

</td></tr><tr><td>

Modeless dialog

</td><td>

-   Define the header text that wraps to 2 lines and truncates after the second line.
-   Replace the initial variant color type with a primary or secondary type that adds color to the heading.
-   Add a button icon that triggers an action in the optional button slot.
-   Change where the modeless dialog appears when triggered by a user. By default it appears in the center, but you can have the dialog appear in the top left or right, or bottom left or right.
-   Use keyboard shortcuts to move the dialog up, down, left, and right.

</td></tr><tr><td>

Recommended Actions

</td><td>

-   Configurable panel title and tab headings.
-   Configurable tab order.
-   New Search tab that contains a search input field and cards for search results.
-   History moved from a tab to a new panel triggered from an iconic button.
-   Background color for hint text and an icon in the search results cards.

</td></tr><tr><td>

Resizable panes

</td><td>

Keyboard key combination to change the layout to only left pane, both panes, and only right pane.

</td></tr><tr><td>

Select

</td><td>

AI Indicator to signals to users when a form field uses AI recommendations and provides more information about AI functionality.

</td></tr><tr><td>

Textarea

</td><td>

AI Indicator to signal to users when a form field uses AI recommendations and to provide more information about AI functionality.

</td></tr><tr><td>

Typeahead

</td><td>

AI Indicator to signal to users when a form field uses AI recommendations and to provide more information about AI functionality.

</td></tr><tr><td>

Typeahead-multi

</td><td>

AI Indicator to signal to users when a form field uses AI recommendations and to provide more information about AI functionality.

</td></tr></tbody>
</table><table><thead><tr><th>

Chart

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Bar visualization

</td><td>

Pareto type of bar visualization. A Pareto chart is similar to the vertical bar chart, but it also includes a line graph. A Pareto chart displays vertical bars that represent individual values \(frequency or cost\) in descending order, and a line with data points that represent the cumulative total. The Pareto chart also marks the 80% point on the y-axis with a horizontal line, which the user can hide.

</td></tr><tr><td>

Indicator scorecard visualization

</td><td>

-   Latest score bar that you can display for a graphical representation of the most recent indicator score. A blue bar for score of 1 or above, an orange bar for -1 and below, and no bar for 0 \(zero\) score. Score value displays upon hover.
-   Maximum number of groups can be specified \(1-20\).
-   Only breakdowns can be specified to be shown, and then you can also show all groups for the first breakdown.

</td></tr><tr><td>

Time series visualization

</td><td>

Date range picker that adds a date range drop-down that the user can use to change quickly the time range displayed to one of the predefined date ranges.

</td></tr></tbody>
</table>

</td></tr><tr><td>

Xanadu

</td><td>

<table><thead><tr><th>

Component

</th><th>

Enhancements

</th></tr></thead><tbody><tr><td>

Appointment calendar

</td><td>

Reflow support in higher browser zoom levels of up to 400% in day and week view.

</td></tr><tr><td>

Badge

</td><td>

Option to enable partial number counts and additional characters, including the plus "+" symbol.

</td></tr><tr><td>

Breadcrumbs

</td><td>

Improved breadcrumb orientation experience with option to enable overflow menu.

</td></tr><tr><td>

Calendar

</td><td>

-   Extra content slot in the header to add buttons.
-   Column width control in the timeline view.

</td></tr><tr><td>

Checkbox

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Checklist

</td><td>

-   Additional configuration options like Disabled, Read Only, and Invalid.
-   Font size customization.
-   Option to configure mandatory field indicator.
-   Error notification appears when the user attempts to submit a form with an incomplete required field.

</td></tr><tr><td>

Contextual sidebar

</td><td>

Improved configuration with vertical tabs structure.

</td></tr><tr><td>

Date-time

</td><td>

-   Time zone displays for users.
-   Horizontal layout option for date-time input field.

</td></tr><tr><td>

Email composer

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Email composer \(mini\)

</td><td>

-   Improved draft management experience with email footer and side panel action buttons.
-   Improved drafting experience with larger compose area and enhancements to save vertical space.
-   Option to enable auto-load of most recent draft.
-   Option to suppress "Send email" button.
-   Support for international characters in email IDs.

</td></tr><tr><td>

Form

</td><td>

Support for 2 or more forms on a page. **Note:** If you want to add a form to a legacy page with an existing form, see the [Form UIB Setup documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-record-form-section-column-layout/uib-setu).

</td></tr><tr><td>

Highlighted value

</td><td>

Improved display of long text with text wrapping functionality.

</td></tr><tr><td>

Input

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Node map

</td><td>

In the hierarchical layout:-   Movable nodes in the map.
-   Customizable control panel.
-   Customizable node connections in new nodes.
-   Improved reflow in higher browser zoom levels.
-   Support for pausing node map layout refresh \(re-layout\).

</td></tr><tr><td>

Radio button

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Related items

</td><td>

-   Show or hide the heading.
-   Configure the background color.
-   Refresh a specific list along with all other lists in the container.

</td></tr><tr><td>

Select

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Text area

</td><td>

-   Customizable slot after the information button for inserting additional elements.
-   Added a caret slot that follows the user's text cursor.

</td></tr><tr><td>

Toggle

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr><tr><td>

Typeahead multi

</td><td>

Customizable slot after the information button for inserting additional elements.

</td></tr></tbody>
</table>

</td></tr><tr><td>

Yokohama

</td><td>

<table><thead><tr><th>

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
</table><table><thead><tr><th>

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
</table><table><thead><tr><th>

Template

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Dashboards

</td><td>

-   Pills at the top of the page display any categories assigned to the dashboard
-   User avatars at the top of the page indicate real-time editing

</td></tr></tbody>
</table><table><thead><tr><th>

Bundle

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Record list

</td><td>

-   Condition builder available in the list header
-   If live list is enabled, infinite scrolling is enabled by default

</td></tr></tbody>
</table>

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

<table><thead><tr><th>

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
</table><table><thead><tr><th>

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Next Experience Components features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Next Experience Components features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

|UI Element|Description|
|----------|-----------|
|Dashboard overview template|Moved under "Legacy templates" and renamed to "Deprecated - Dashboard overview." This template can still be used, but you should use the new "Dashboard library" template instead, because the Dashboard overview template is marked for eventual deprecation.|

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Next Experience Components.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Xanadu

</td><td>

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Next Experience Components we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Next Experience Components we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Next Experience Components, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

The following accessibility enhancements were made to the Next Experience Components in the Washington DC release.

-   **Support for magnification software and screen readers**

The following Next Experience Components were updated to match programmatic labels to visual labels. This enhancement provides improved support for ZoomText \(a type of magnification software\) and other types of Assistive Technology \(for example, screen readers\).

This enhancement supports users with cognitive and physical disabilities, such as low vision or mobility limitations, who use the ServiceNow platform.

    -   Agent chat \[sn-agent-chat\]
    -   Agent inbox \[sn-agent-inbox\]
    -   Canvas tabs \[sn-canvas-tabs\]
    -   Chat input \[sn-chat-input\]
    -   Chat mention suggestion \[sn-chat-mention-suggestion\]
    -   Checklist \[now-checklist\]
    -   Date time calendar \[now-date-time-calendar\]
    -   Document viewer \[sn-document-viewer\]
    -   Drag and drop \[sn-drag-and-drop\]
    -   Field select \[sn-record-field-list-reorder-list\]
    -   List selector \[sn-list-selector\]
    -   Notification setting popover content \[notification-setting-popover-content\]
    -   Presence popover content \[sn-presence-popover-content\]
-   **Support for reflow**

The following components were updated to support reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=washingtondc&ft:locale=en-US) for details.

    -   Action bar \[now-record-common-uiactionbar\]
    -   Agent chat \[sn-agent-chat\]
    -   Appointment calendar \[now-appointment-calendar\]
    -   Bar chart \[now-vis-bar\]
    -   Bubble visualization \[now-vis-bubble-wrapper\]
    -   Calendar \[now-calendar\]
    -   Carousel \[sn-carousel\]
    -   Checklist \[now-checklist\]
    -   Contact card \[sn-contact-card\]
    -   Content tree \[now-content-tree\]
    -   Contextual sidebar \[now-contectual-sidebar\]
    -   Customer activity \[sn-customer-activity\]
    -   Date range picker \[now-date-range-picker\]
    -   Dial chart \[now-vis-dial\]
    -   Document display \[sn-document-display\]
    -   Document intelligence \[sn-docintel-iframe\]
    -   Express list \[sn-itom-aiops-list\]
    -   Filter \[now-filter\]
    -   Form \[now-record-form-selection-column-layout\]
    -   Gauge chart \[now-vis-gauge\]
    -   Geomap visualization \[now-vis-geomap-wrapper\]
    -   Heatmap visualization \[now-vis-heatmap-wrapper\]
    -   ITOM Metric Explorer \[sn-itom-metric-explorer\]
    -   Kanban board \[now-visual-board\]
    -   Knowledge blocks \[sn-knowledge-blocks-connected-uib\]
    -   Knowledge content \[sn-knowledge-content\]
    -   List selector \[sn-list-selector\]
    -   Pagination control \[now-pagination\]
    -   Pie/donut visualization \[now-vis-pie-wrapper\]
    -   Pivot table visualization \[sn-multipivot\]
    -   Playbook activity viewer \[now-playbook-activity-viewer\]
    -   Playbook experience \[now-playbook-experience-connected\]
    -   Playbook modals \[now-playbook-modals\]
    -   Playbook stage picker \[now-playbook-stage-picker\]
    -   Service Health Dashboard New \[sn-itom-service-dashboard\]
    -   Single score \[now-score-advanced\]
    -   Timeseries visualization \[now-vis-timeseries-wrapper\]
-   **Support for speech-to-text**

The following Next Experience Components were updated to match visual labels to their accessible labels. If the accessible label is different from the visual label, speech-to-text software can't identify and activate the interactive element. Matched visual and accessible labels enable speech-to-text software, such as Dragon Naturally Speaking, to identify these components in the user interface rather than doing a slow grid-based navigation offered by the speech-to-text assistant technologies.

    -   Dropdown \[now-dropdown\]
    -   Input \[now-input\]
    -   Record list \[now-record-list\]
    -   Record number \[now-record-number\]
    -   Text link \[now-text-link\]
    -   Toggle \[now-toggle\]
    -   Typeahead \[now-typeahead\]
    -   Typeahead multi \[now-typeahead-multi\]
-   **General accessibility enhancements**

The following components were updated to meet internationally recognized accessibility standards.

    -   Appointment calendar \[now-appointment-calendar\]
    -   Calendar \[now-calendar\]
    -   Checklist \[now-checklist\]
    -   Contact card \[sn-contact-card\]
    -   Content tree \[now-content-tree\]
    -   Kanban \[now-visual-board\]
    -   Playbook activity picker \[now-playbook-activity-picker\]
    -   Radio group \[now-radio-group\]

</td></tr><tr><td>

Xanadu

</td><td>

Next Experience Components are updated for accessibility in the Xanadu release.

-   **Updated components**

The following components were updated to support Web Content Accessibility Guidelines \(WCAG\) 2.1 level AA:

    -   360 degree visualization \[sn-grc-360-degree-visualization\]
    -   Agent Messaging \[sn-agent-messaging\]
    -   Analytics Q&amp;A \[sn-nlq-analytics\]
    -   Appointment calendar \[now-appointment-calendar\]
    -   Audio player \[sn-audio-player\]
    -   BCM Crisis map \[sn-bcm-crisis-map-connected\]
    -   Calendar \[now-calendar\]
    -   Capacity Planning \[sn-capacity\]
    -   Catalog Wizard \[sn-catalog-wizard-connected\]
    -   Chat Popover \[now-requestor-chat-popover\]
    -   Circuit map \[sn-circuit-map\]
    -   Confirmation message \[now-confirmation-message\]
    -   Q1 Dashboards Overview \[sn-dashboards-overview\]
    -   Data Grid UI Component \[sn-datagrid\]
    -   Data Visualization Designer \[sn-viz-designer\]
    -   DevOps Pipeline \[sn-devops-pipeline\]
    -   Display Only Form \[now-record-form-section-connected\]
    -   Email composer \[now-email-client-composer-connected\]
    -   FAM Map \[sn-fam-map\]
    -   Form record presence \[now-record-common-record-presence\]
    -   Funnel \[sn-va-funnel\]
    -   Gantt Chart \[now-gantt\]
    -   Geo Map \[sn-geo-map\]
    -   Guided Decisions App Shell Header \[sn-gd-app-shell-header\]
    -   Guided Decisions Builder \[sn-guided-decisions-builder\]
    -   Guided Decisions Experience \[sn-guided-decisions-card\]
    -   Indoor Mapping \[sn-map-component\]
    -   Metric datatable component \[sn-metric-datatable\]
    -   Node map \[sn-node-map\]
    -   OHS Injury Picker \[sn-ohs-injury-picker-connected\]
    -   PaCE dynamic form for inputing variables \[sn-pace-policy-dynamic-form\]
    -   PaCE Policy Builder \[sn-pace-policy-builder\]
    -   PaCE Policy Input \[sn-pace-policy-builder-io\]
    -   PAR Component Builder \[sn-par-component-builder\]
    -   Playbook Activity Picker \[now-playbook-activity-picker\]
    -   Playbook Form \[now-playbook-experience-form-connected\]
    -   Policy as Code Engine Test Playground Control \[sn-pace-test-playground-control\]
    -   Presentational List \[now-list\]
    -   Process Mining - Automation Discovery Report \[sn-promin-automation-discovery-report\]
    -   Process Mining - Improvement Initiatives \[sn-promin-initiatives-connected\]
    -   Process Mining - Improvement Opportunities \[sn-promin-process-findings-connected\]
    -   Process Mining - Notes \[sn-promin-notes-connected\]
    -   Process Mining - Projects List \[sn-promin-process-list-connected\]
    -   Process Mining - Routes \[sn-promin-process-routes-connected\]
    -   Process Mining Workbench \[sn-promin-workbench-connected\]
    -   Process Optimization - Map \[sn-promin-process-map-connected\]
    -   Quick Filter \[sn-quick-filter\]
    -   Quick Filter Popover \[sn-quick-filter-popover\]
    -   Reference Selector using Condition Builder \[sn-pace-policy-reference-selector-cb\]
    -   Risk Heatmap \[sn-risk-heatmap\]
    -   Roadmap \[sn-roadmap\]
    -   Scheduled Export \[sn-par-scheduled-export\]
    -   Search facets \[sn-search-facets\]
    -   Search input \[sn-search-combobox\]
    -   Search Result Wrapper \[sn-search-result-wrapper\]
    -   Split view \[split view\]
    -   Tab filter \[sn-tab-filter\]
    -   Task Planner \[sn-task-planner\]
    -   VA Analytics Chart Container \[sn-va-slotted-tile\]
    -   VA Analytics Event Property Set \[sn-va-custom-event-props\]
    -   VA Analytics Trend Score \[sn-va-score-trend\]
    -   Workplace Stack Plan \[sn-wsd-stackplan\]

</td></tr><tr><td>

Yokohama

</td><td>

For Next Experience Components accessibility conformance, refer to the ServiceNow [Horizon site Components section](https://horizon.servicenow.com/workspace/components).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

To view Next Experience Components accessibility conformance information, refer to the components section of the [Horizon site Components section](https://horizon.servicenow.com/workspace/components). The Overview for each component contains accessibility \(A11y\) information.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Next Experience Components we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Next Experience Components we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&family=washingtondc&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&family=washingtondc&ft:locale=en-US).
-   Upgraded components for accessibility. For more information, see the Accessibility information section in these release notes.

</td></tr><tr><td>

Xanadu

</td><td>

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&family=xanadu&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Developer site Next Experience Components doc](https://developer.servicenow.com/dev.do#!/reference/next-experience/components%3Freleases%5B%5D=washingtondc%26query=%26order_by=nameAsc%26limit=120%26offset=0%26categories%5B%5D=uib_component%26categories%5B%5D=uib_macroponent-component%26categories%5B%5D=uib_facades).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&family=yokohama&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Horizon site Components section](https://horizon.servicenow.com/workspace/components).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so that the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&family=australia&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-washingtondc-australia/rn-combined-intro.md)

