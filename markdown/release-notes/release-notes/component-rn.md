---
title: Next Experience Components
description: The ServiceNow Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Next Experience Components

The ServiceNow® Next Experience Components are the components used to build custom user interfaces. Next Experience Components was enhanced and updated in the Zurich release.

## Next Experience Components highlights for the Zurich release

-   Build rich UI experiences with prebuilt system or custom components. To view the Next Experience Components API reference, usage guidance, and ServiceNow® UI Builder setup documentation, visit the [Horizon site Next Experience Components doc](https://horizon.servicenow.com/workspace/components?release=zurich).
-   Use common web component patterns and principles, such as a JavaScript framework, immutable data, and simple action handlers.
-   Reuse components across multiple user interfaces to create a cohesive experience for your end users.
-   Use preset property values to configure properties and event handlers automatically for a component so that the component is ready to work when you add it to a page. Presets can connect to a controller that acts as a data resource for the component. For more information, see [Automatically configure components using presets](https://www.servicenow.com/docs/access?context=presets&version=zurich&pubname=zurich-application-development&ft:locale=en-US) and [Bind data to UI Builder pages using controllers \(advanced feature\)](https://www.servicenow.com/docs/access?context=controllers&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## New in the Zurich release

|Component|Description|
|---------|-----------|
|AI Summary Card|Organizes AI-generated summary information into a simple, easily scannable format.|
|Animated icon|Animated sparkle icon that indicates an entry point for a Now Assist flow or event.|
|Carousel Text|Cycles through a series of text messages with animated transitions. Provides visual feedback during loading states with customizable message content.|
|Catalog browse|Enables users to explore, search, and find the catalog items they want across multiple catalogs and categories. Users choose a catalog from a dropdown and then a category in a side panel. A selectable card for each available item in the category is displayed in the main view.|
|Filter overview|Provides a summary of the filters currently applied to the page. Primarily used on the list page in combination with condition builder.|
|Flyout menu|Organizes multiple levels of options within a hierarchical structure.|
|Now Assist context menu|Provides actions like generating text, creating incident or task summaries, or refining content.|
|Schedule Recurrence|Enables users to create and to manage recurring events with daily, weekly, monthly, and yearly frequency. Users can add additional rules like skip dates, exceptions, and validations.|
|Simple timer|Displays elapsed time with an optional leading icon.|

|Bundle|Description|
|------|-----------|
|Activity stream compose with modeless dialog|Component bundle that contains all the functionality of Activity Stream Compose with the added functionality of modeless dialog pop-up. To add modeless dialog capabilities to the compose experience, replace the Activity Stream Compose component with this component bundle.|

## Changed in this release

<table id="table_comp_list"><thead><tr><th>

Component

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Activity Stream

</td><td>

-   Dynamic translation support for emails in Activity Stream
-   Events show AI agent as author on behalf of user
-   Hide the title and move the setting toggle to compose tabs line
-   Live Presence in Activity Stream

</td></tr><tr><td>

Activity Stream Compose

</td><td>

Increased agent productivity by reducing scroll time and seamlessly stacking the compose experience with Activity Stream

</td></tr><tr><td>

Appointment calendar

</td><td>

-   Updated UI Builder property labels and UI
-   Date-Time replaces mini calendar
-   Changing the month doesn't automatically select the current selected date
-   Disable categories
-   Disable previous dates and unavailable slots
-   Show event duration in event slots
-   Disable truncation in screens with resolution lower than 640 pixels

</td></tr><tr><td>

Attachments

</td><td>

-   Enable uploading multiple files
-   Set restrictions on file types and size
-   Preview upload modal for viewing the selected attachments before upload
-   Rename or remove files during upload preview
-   Single-click upload for multiple files

</td></tr><tr><td>

Button

</td><td>

Enable the animated sparkle icon

</td></tr><tr><td>

Button bare

</td><td>

-   Multi-line label text available
-   Enable the animated sparkle icon

</td></tr><tr><td>

Button circular

</td><td>

Enable the animated sparkle icon

</td></tr><tr><td>

Button iconic

</td><td>

Enable the animated sparkle icon

</td></tr><tr><td>

Calendar

</td><td>

-   Add multiple columns in timeline views
-   Date-Time replaces mini calendar in timeline views

</td></tr><tr><td>

Carousel

</td><td>

Expose a badge on the side of the title, by adding optional text and any 1 of a variety of colors

</td></tr><tr><td>

Checkbox

</td><td>

Display the label slot before or after the check box

</td></tr><tr><td>

Checklist

</td><td>

Control size of the checklist

</td></tr><tr><td>

Date-time

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Date-time-interval

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Email composer

</td><td>

-   Enable user mentions in the compose area
-   Enable digital signing and encryption of emails
-   Selecting a user pill displays user contact card

</td></tr><tr><td>

Email composer mini

</td><td>

-   Option to pop out to modeless dialog
-   Enable user mentions in the compose area
-   Enable digital signing and encryption of emails
-   Selecting a user pill displays user contact card

</td></tr><tr><td>

Email viewer

</td><td>

Selecting a user pill displays user contact card.

</td></tr><tr><td>

Feedback

</td><td>

Configure the character limit in the text area of the component

</td></tr><tr><td>

Form

</td><td>

-   Unsaved field indicator: An unsaved indicator that displays a black dot next to field names that have unsaved changes.
-   Field context menu hide option: Provide admins access to hidden field context menu options.
-   Label wrapping and width limit: Have field labels on a form wrap instead of truncate when the container width you specify is reached.

</td></tr><tr><td>

Form record presence

</td><td>

Select an active viewer's avatar to launch a customer card pop-up that contains their contact info.

</td></tr><tr><td>

Heading

</td><td>

Change the text alignment from **start** to **center**, **end**, or **justify**.

</td></tr><tr><td>

iFrame

</td><td>

Enforce consistent practices, as well as more safely compose third-party content by selecting what functionality is available to the iFrame.

</td></tr><tr><td>

Input

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Input password

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Input phone

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Input URL

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Kanban board

</td><td>

-   Maximum of 3 highlighted values, 3 to 5 icons, and 1 hyperlink supported on the VTB card
-   Drag multiple, selected cards at once

</td></tr><tr><td>

Label value tabbed

</td><td>

-   Set fixed width instead of auto-sizing to content
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Modeless dialog

</td><td>

By default, the dialog dynamically resizes when the user types beyond the height of the dialog.

</td></tr><tr><td>

Node map

</td><td>

-   Horizontal type layout that supports all key capabilities such as, custom nodes, node animation, and all edge types
-   Enhanced spacing behavior for layouts that improves spacing utilization
-   Expose unified node in UI Builder
-   Enhanced knowledge graphs with dynamic edge positioning, optimized label handling, and intuitive edge highlighting

</td></tr><tr><td>

Playbook

</td><td>

Improved navigation and user interface based on feedback from users.

</td></tr><tr><td>

Playbook activity picker

</td><td>

Improved navigation and user interface based on feedback from users.

</td></tr><tr><td>

Playbook stage picker

</td><td>

Improved navigation and user interface based on feedback from users.

</td></tr><tr><td>

Predicate builder

</td><td>

Configuration for read only

</td></tr><tr><td>

Radio buttons

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Select

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Split button

</td><td>

Enable the animated sparkle icon

</td></tr><tr><td>

Textarea

</td><td>

-   Disable the minimum height constraint of 64 pixels
-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Typeahead

</td><td>

-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr><tr><td>

Typeahead multi

</td><td>

-   Pills can display a custom tooltip on hover
-   Configurable slot for unsaved field indicator
-   Enable label text wrapping instead of truncation

</td></tr></tbody>
</table><table id="table_bundle_enhancements"><thead><tr><th>

Bundle

</th><th>

Enhancement

</th></tr></thead><tbody><tr><td>

Record list

</td><td>

-   Display the list in cards
-   HTML fields can be viewed without HTML tags in the list view
-   Export to Google Sheets
-   Images and icons display in the list
-   Enable live lists on a per table basis
-   Scrollable and inline editable HTML fields

</td></tr></tbody>
</table>## Activation information

Next Experience Components is a ServiceNow AI Platform feature that is active by default.

## Accessibility information

To view Next Experience Components accessibility conformance information, refer to the components section of the [Horizon site Components section](https://horizon.servicenow.com/workspace/components). The Overview for each component contains accessibility \(A11y\) information.

## Related ServiceNow applications and features

-   **[UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    UI Builder is a low-code tool that helps enable you to build pages for workspace and portal web-based experiences.

-   **[Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    Use components to build custom workspace experiences for agents who solve internal or external customer issues.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

