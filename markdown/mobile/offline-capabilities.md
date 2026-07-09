---
title: Mobile experience components available in offline mode
description: Use the tables to view the various components and features that are either fully, partially or not supported in offline mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/offline-capabilities.html
release: australia
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 6
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile experience components available in offline mode

Use the tables to view the various components and features that are either fully, partially or not supported in offline mode.

The three table listed are categorized as follows:

-   Component is fully supported, and the behavior is the same for both online and offline.
-   Component is partially supported in offline with certain limitations.
-   Component is not supported in offline.

## Supported offline components

<table id="table_fwk_jf5_njc"><thead><tr><th>

Component

</th><th>

Sub-component

</th><th>

Conditions requited for offline flows to work

</th><th>

Optional dedicated offline configuration

</th><th>

Design considerations

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

Mobile application

</td><td>

Now Mobile app, Mobile Agent app, Custom app, and Mobile Publishing

</td><td>

Set the application to support offline mode.**Note:** Enabling the mobile app as offline is not sufficient, as every screen and function involved must also be configured for offline use.

</td><td>

n/a

</td><td>

n/a

</td><td>

Mobile Agent app: Used by employees such as technicians or support agents to view, update, and complete assigned tasks, incidents, or work orders while on the go.

 Now Mobile app: Used by employees to submit requests, report issues, and track the status of their tickets or service requests.

</td></tr><tr><td>

Navigation tab

</td><td>

Launcher screen / screen

</td><td>

The launcher screen or screen configured for the tab must be set as available offline.

</td><td>

n/a

</td><td>

n/a

</td><td>

Mobile home screen, navigation to different screens.

</td></tr><tr><td>

UI section

</td><td>

Record UI section, icon UI section, legacy UI icon section, content UI section

</td><td>

For the icon UI section and legacy icon UI section, the screen or function must be set as available offline.

</td><td>

n/a

</td><td>

Record UI section displays only cached records.

</td><td>

My tasks, recent records, quick navigation tiles.

</td></tr><tr><td>

Record screen

</td><td>

Related list segment, record sections segment, activity stream segment

</td><td>

Related records must be cached.

</td><td>

n/a

</td><td>

Limited to cached records.

</td><td>

Child records, task history.

</td></tr><tr><td>

Screen

</td><td>

List screen, calendar screen

</td><td>

Screen must be set as available offline.

</td><td>

n/a

</td><td>

Limited to 1000 records.

</td><td>

Scheduled tasks

</td></tr><tr><td>

Mobile cards

</td><td>

UI rules

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td></tr><tr><td>

Execution

</td><td>

Function instance

</td><td>

n/a

</td><td>

By default, all button instance locations are available offline; a specific location can be inactive.

</td><td>

n/a

</td><td>

The location of the button within the screen, for example the footer area, top menu, or a specific field.

</td></tr><tr><td>

Execution of operations on records while offline

</td><td>

Action items such as write-back actions and write-back action steps

</td><td>

n/a

</td><td>

-   An offline step must be configured to support offline local database modifications that affect button conditions, displayed list records, or similar logic.
-   If an offline step is configured, an online step must also be configured to apply local database changes to the instance once the device returns online.

</td><td>

-   Scripted write-back action step is not supported.
-   The offline step supports declarative configuration only and can modify only the record currently used as context by the write-back action.

</td><td>

When a user performs an action offline, changes are marked for later sync with the instance. To confirm these changes are immediately reflected in app workflows such as list filtering and conditional button visibility, the admin must define logic for handling insert, update, or delete operations, keeping the local database consistent with the expected flow.

</td></tr><tr><td>

Input form

</td><td>

Data source

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td><td>

Enables the download of input form data for elements such as descriptive fields, input values, and values of input actions such as comments and attachments.

</td></tr><tr><td>

Input form

</td><td>

Input actions

</td><td>

Scripted write-back action required.

</td><td>

n/a

</td><td>

n/a

</td><td>

Add attachments, add a comment, navigate to another screen in the context of the input.

</td></tr><tr><td>

Input form

</td><td>

Descriptive element

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td><td>

Used to provide instructions to the user on how to respond to a question when completing questionnaires.

</td></tr><tr><td>

Input form

</td><td>

String input, number input, Boolean input, date/datetime input, barcode input

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td></tr><tr><td>

Input form

</td><td>

Attachment input

</td><td>

Scripted write-back action required.

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td></tr><tr><td>

Input form

</td><td>

Auto-fill inputs and input actions

</td><td>

Dependent data cached.

</td><td>

n/a

</td><td>

May fail if reference data is missing.

</td><td>

Forms pre-populated with data downloaded from the instance.

</td></tr><tr><td>

Input form

</td><td>

Save progress

</td><td>

Local save write-back action step is required.

</td><td>

n/a

</td><td>

n/a

</td><td>

n/a

</td></tr></tbody>
</table>## Partially supported offline components

<table id="table_lx5_nnj_rjc"><thead><tr><th>

Component

</th><th>

Sub-component

</th><th>

Conditions requited for offline flows to work

</th><th>

Optional dedicated offline configuration

</th><th>

Design considerations

</th><th>

Use case

</th></tr></thead><tbody><tr><td>

UI section

</td><td>

Media UI section

</td><td>

Media assets must be available locally.n/a

</td><td>

n/a

</td><td>

Remote media assets, for example YouTube videos, aren't available offline.

</td><td>

Campaigns with banners and images.

</td></tr><tr><td>

Record screen

</td><td>

Details segment

</td><td>

Record data must exist locally.

</td><td>

n/a

</td><td>

Checklist field type not supported.

 Video field type not supported.

</td><td>

Fields that represent the record, such as description, assignment group, and attached files.

</td></tr><tr><td>

Screen

</td><td>

Map screen

</td><td>

Screen must be set as available offline.

</td><td>

n/a

</td><td>

List view only is supported.

 Limited to 1000 records.

</td><td>

Task location view.

</td></tr><tr><td>

Screen

</td><td>

Input forms

</td><td>

The screen and function that triggers the form must be set as available offline.

</td><td>

Enable merge of any consecutive outbox items.

</td><td>

Client scripts not supported.Dependent inputs may fail if reference data is not cached.

</td><td>

Create or edit records while offline.

</td></tr><tr><td>

Screen

</td><td>

Data item

</td><td>

Configured for offline caching.

</td><td>

Dedicated offline data item, pre-cached before device download.

</td><td>

-   Query limitations of 1000 records per screen segment.
-   Parameterized data item not supported.
-   Scripted data item conditions are evaluated only when the offline cache is generated. Once the data is downloaded and the user is offline, the script no longer runs. The app uses the pre-generated query string to filter the data as it was prepared at download time.

</td><td>

Record data retrieval

</td></tr><tr><td>

Screen

</td><td>

Mobile cards

</td><td>

n/a

</td><td>

n/a

</td><td>

Videos not supported.

</td><td>

UI components used to display a compact summary of a record or information block in a visually structured way inside mobile screens. Mobile cards are commonly implemented in list screen and home tab sections.

</td></tr><tr><td>

Execution

</td><td>

Function

</td><td>

Function must be set as available offline.

</td><td>

Offline conditions for button visibility.

</td><td>

Supported types: navigation, action item \(create, update, delete record\), upload attachment.

</td><td>

Used across different screens to define the action performed when the button is tapped.

</td></tr><tr><td>

Input form

</td><td>

UI rules

</td><td>

n/a

</td><td>

n/a

</td><td>

Client scripts not supported.

</td><td>

n/a

</td></tr><tr><td>

Input form

</td><td>

Reference input

</td><td>

n/a

</td><td>

Specific offline attributes for the control can be configured.

</td><td>

1000 records can be cached.

</td><td>

Assign a user to a task.

</td></tr></tbody>
</table>## Non-supported offline components

|Component|Sub-component|Conditions requited for offline flows to work|Optional dedicated offline configuration|Design considerations|Use case|
|---------|-------------|---------------------------------------------|----------------------------------------|---------------------|--------|
|UI section|Analytics section|n/a|n/a|n/a|KPI dashboards|
|Launcher screen|Search bar|n/a|n/a|n/a|n/a|
|Screen|Chart screen, mobile web screen|n/a|n/a|Performance analytics and embedded web content such as catalog items or knowledge articles aren't supported. Use a record screen with HTML content instead.|n/a|
|Input form|Signature input type, screen input type, custom map input type|n/a|n/a|n/a|n/a|
|Input form|AI summarization|n/a|n/a|AI capabilities not supported offline.|AI text summarization for resolution notes.|
|Action dialog|Mobile pop-ups|n/a|n/a|n/a|Warning message that prompts the user to choose whether to proceed with the flow or cancel it. For example, notifying the user that their shift is about to end when they attempt to accept a task.|
|Chat|Virtual agent \(VA\)|n/a|n/a|n/a|Self-service chat for employees or customers.|
|Chat|Sidebar|n/a|n/a|n/a|ServiceNow Sidebar is a real-time, record-based collaboration tool that allows agents to privately chat and share knowledge with subject matter experts to quickly resolve tasks, cases, and incidents.|

**Parent Topic:**[Offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-offline-mode.md)

