---
title: Activity Stream component setup
description: Activity Stream provides a history of each record, which includes things such as field changes, communication with requesters or fellow agents via comments, and work notes or email depending on the workflow.Properties in the Activity Stream component have preset configuration values. You can accept these values or override them manually.If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/activity-stream-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Activity Stream component setup

Activity Stream provides a history of each record, which includes things such as field changes, communication with requesters or fellow agents via comments, and work notes or email depending on the workflow.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Activity Stream that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "activity-stream-content-tree.png"\] Alt text: Shows the label for the Activity Stream component in the UI Builder content tree

2.  Select the Activity Stream component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Activity Stream label you created for your component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "activity-stream-presets.png"\] Alt text: Shows the list of presets for the Activity Stream component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "activity-stream-preset-config.png"\] Alt text: Shows the preset configuration screen for connecting the preset to the controller for Activity Stream

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Activity Stream component properties

Properties in the Activity Stream component have preset configuration values. You can accept these values or override them manually.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record activity stream__**

    This preset shows record activity. This activity can be record field changes, journal entries, attachments, and attached knowledge articles. This preset requires the **Record** controller.

    Properties included in this preset are:

    -   table
    -   Sys ID
    -   Workspace view
    -   New record
    -   Events
    -   Supplemental
    -   AMB Channels
    -   User references
    -   Filter options
    -   Timestamp
    -   Suppress preview record for email actions
    -   Bare

### Properties

<table id="table_npf_sps_5tb"><thead><tr><th>

Field \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title\[title\]

</td><td>

Title of the activity stream. Default: **Activity**

</td></tr><tr><td>

Table\[table\]

</td><td>

Table name for the record.Default: **incident**

</td></tr><tr><td>

App Id\[appId\]

</td><td>

Identifier used to separate some of the stored data to prevent conflicts across multiple workspaces using the same records, please bind to @context.app.appId

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Unique identifier for the record.

</td></tr><tr><td>

Workspace view\[view\]

</td><td>

Fields that show.

</td></tr><tr><td>

New record\[isNewRecord\]

</td><td>

Displays that a record is newly created.

</td></tr><tr><td>

Show conversation filter\[showConversationFilter\]

</td><td>

Displays the conversation filter. **Note:** Doesn't imply a true/false value.

</td></tr><tr><td>

Show avatars\[showTileAvatars\]

</td><td>

Displays avatars.**Note:** Doesn't imply a true/false value.

</td></tr><tr><td>

Show tile icons\[howTileIcons\]

</td><td>

Displays tile icons.**Note:** Doesn't imply a true/false value.

</td></tr><tr><td>

Show tags\[showTags\]

</td><td>

Indicates that tags should be enabled.Default: **true**

</td></tr><tr><td>

Tag panel is visible\[tagEditorIsVisible\]

</td><td>

Enables custom tag editor to hide / show \(Not part of the component only used for UIB UI only\).Default: **true**

</td></tr><tr><td>

Data source\[tagsDataSource\]

</td><td>

How the data for tags is provided.

</td></tr><tr><td>

Tag List\[availableTags\]

</td><td>

List of visible tags for activity stream.

</td></tr><tr><td>

Events\[events\]

</td><td>

Optional array of events. When an event is provided, it saves the first request to the server. Property can be bound to a form data resource.

</td></tr><tr><td>

Supplemental\[supplemental\]

</td><td>

Supplemental data for activity events.

</td></tr><tr><td>

Fields\[fields\]

</td><td>

Reads field-level information, such as dictionary attributes, definitions, and field states. Tiles use this information to read configurations.

</td></tr><tr><td>

AMB Channels\[ambChannels\]

</td><td>

Optional array of AMB channels to connect to. Property can be binded to a form data resource to save initial queries.

</td></tr><tr><td>

User references\[userReferences\]

</td><td>

Optional array of user information to reuse across events. Property can be binded to a form data resource to save initial queries.

</td></tr><tr><td>

Feature flags\[featureFlags\]

</td><td>

Array of feature flags in the format \{name: 'name', value: 'value'\}

</td></tr><tr><td>

Filter options\[filterOptions\]

</td><td>

Optional array of filter options in the shape of \{isSelected: true, label: 'Filter label', name: 'name'\}. Property can be binded to a form data resource to save initial queries.

</td></tr><tr><td>

Timestamp\[timestamp\]

</td><td>

Current timestamp that's used to know when new data is coming in.

</td></tr><tr><td>

Suppress preview record for email actions\[suppressPreviewRecordForEmailActions\]

</td><td>

Stops propagation of the REVIEW\_RECORD and PREVIEW\_RECORD\_REQUESTED email events.Default: **true**

</td></tr><tr><td>

User session information\[userSession\]

</td><td>

Object containing the user session information.Default: @context.session.user

</td></tr><tr><td>

Bare\[bare\]

</td><td>

Removes the padding and background from the component.Default: **true**

</td></tr><tr><td>

Show Email Options\[showEmailOptions\]

</td><td>

Enables email features.Default: true

</td></tr><tr><td>

enableLineSeparator\[Enable Line Separator\]

</td><td>

Enables line separatorDefault: **false**

</td></tr><tr><td>

Suppress Global Events\[supressGlobalEvents\]

</td><td>

Suppress events that rely on parent elements handling, and only dispatch events with the component prefix that are manually binded.Default: **false**

</td></tr><tr><td>

Attachment tile component\[attachmentTileComponent\]

</td><td>

Overwrites component used to render attachment tiles.

</td></tr><tr><td>

Audit tile component\[auditTileComponent\]

</td><td>

Overwrites component used to render audit tiles.

</td></tr><tr><td>

Audit relation tile component\[auditRelationTileComponent\]

</td><td>

Overwrites component used to render audit relation tiles.

</td></tr><tr><td>

Email tile component\[emailTileComponent\]

</td><td>

Overwrites component used to render email tiles.

</td></tr><tr><td>

Journal tile component\[journalTileComponent\]

</td><td>

Overwrites component used to render journal tiles.

</td></tr><tr><td>

Refresh requested\[refreshRequested\]

</td><td>

Timestamp of activity refresh request.

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Activity Stream component events

If you have chosen a preset containing events, data handlers for those events are pre-selected by the controller, and no manual configuration is required. If the component has events that aren't included in the preset, you must add data handlers manually to configure those events.

The Events tab shows the events used by the Activity Stream component. Events with presets are marked with the **Preset** badge. To show events that don't have preset configurations, select **+ Add event mapping**.

\[Omitted image "activity-stream-events.png"\] Alt text: Shows the events included with Activity Stream. None of the events are included with the preset

### Event handlers

Event handlers work with data resources to link the Activity Stream actions to the data you want to display to your users. Select the event in the list to add one or more event handlers. For information about event handlers, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "activity-stream-add-event-handler.png"\] Alt text: Shows events for Activity Stream that have been selected to allow adding event handlers

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record activity stream__**

    This preset doesn't have any events.


### Event descriptions

<table id="table_zjp_wqg_4nb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email action requested

</td><td>

User has selected **Reply**, **Reply-all**, or **Forward** from the email tile.Payload:

-   **table**: Table for the email record `sys_email_draft` or `sys_email`.
-   **sysId**: Value of Sys ID. Use -1 for new email record.
-   **targetTable**: Table for the record to which the email relates.
-   **targetRecord**: Sys ID for the record to which the email relates.
-   **replyId**: Contains the original Sys ID for a reply action.
-   **replyType**: One of `replyAll`, `reply`, or `forward`.

</td></tr><tr><td>

Preview record requested

</td><td>

The action to open a record was initiated by the component.Payload:

-   **table**: Table name of the record requested
-   **sysId**: Sys ID of the record requested
-   **params**: Optional parameters

</td></tr><tr><td>

Journal entry post succeeded

</td><td>

User successfully posted a journal entry.

</td></tr></tbody>
</table>