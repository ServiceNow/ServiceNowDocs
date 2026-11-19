---
title: Attachments component setup
description: The Attachments component is used in the standard record page's contextual sidebar tab to enable a user to add, preview, download, or remove attachments from a record.Properties in the Attachments component have a choice of preset or manual configuration values.If you have chosen a preset, data handlers for the component events are pre-selected by the controller, and no manual configuration is required. However, you can add additional data handlers to an event or disable the event.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/attachment-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Attachments component setup

The Attachments component is used in the standard record page's contextual sidebar tab to enable a user to add, preview, download, or remove attachments from a record.

## Before you begin

This component contains a preset configuration. Presets automatically configure properties and event handlers for a component, making the component ready to work when you add it to a page. You can apply one preset to a single instance of a component on a page. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

A preset connects to a controller, which acts as a data resource for the component. Controllers provide the configuration data and event binding the component needs to function in your experience. For more information see [Bind data to UI pages using controllers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md).

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for Attachments that differentiates it from other components in the content tree.

    A descriptive label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "attachments-content-tree.png"\] Alt text: Shows a renamed attachment component in the content tree

2.  Select the Attachments component, using one of these methods:

    -   Click anywhere within the component on the page.
    -   Select the label you created for your Attachments component in the content tree.
    The preset selection panel appears in the pane on the right.

    \[Omitted image "attachments-preset-panel.png"\] Alt text: Shows the preset selection panel for the component

3.  Select either **None** to configure the component properties manually, or select one of the available presets to use pre-configured properties and events for the component.

    When you select the first preset on a page, a configuration panel appears with instructions for configuring the required controller for that preset. For more information, see [Automatically configure components using presets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md)

    \[Omitted image "attachments-preset-controller-config.png"\] Alt text: Shows the panel for connecting the preset to the controller

4.  Supply the data that connects a preset to its controller and select **Use**.

    UI Builder automatically configures any other presets in the page to use the same controller with the same configuration. For more information, see [Add a controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/controllers.md)


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Attachments component properties

Properties in the Attachments component have a choice of preset or manual configuration values.

Presets are intended to suit a specific use case. However, you can override a property that has a preset value with a custom configuration if necessary for your design. For details on overriding and resetting presets, see [Override a component preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/presets.md).

**Important:** Preset values that you override aren't updated automatically when you upgrade the instance.

### Available presets

-   **__Record attachments__**

    This preset enables users to browse for and select local files to add to a record as an attachment. All common file types are supported. This preset requires the **Form** controller.

    Properties included in this preset are:

    -   Table
    -   Sys ID
    -   View
    -   Action Configuration ID
    -   Is form read only?
    -   Is uploading Attachment disabled?
    -   Should skip preview for unsupported file types?
    -   Layout mode
    -   Refresh requested

### Properties

<table id="table_c2r_nnc_ptb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table\[table\]

</td><td>

Table name for the record header.

</td></tr><tr><td>

Sys ID\[sysId\]

</td><td>

Sys ID for the record header.

</td></tr><tr><td>

Action Configuration ID\[actionConfigId\]

</td><td>

Sys ID of the configuration for getting attachment actions.

</td></tr></tbody>
</table><table id="table_kdf_3sq_tfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View\[view\]

</td><td>

Specifies the view to which attachment actions should resolve.

</td></tr><tr><td>

Is form read only?\[isReadOnly\]

</td><td>

To denote the form as read-only, set to **true**.Default: **false**

</td></tr><tr><td>

Is uploading attachment disabled?\[isAttachmentUploadDisabled\]

</td><td>

To disable uploading attachments, set to **true**. The option is set in the Form Data Broker.Default: **false**

</td></tr><tr><td>

Is editing attachment disabled?\[isEditingAttachmentDisabled\]

</td><td>

To disable users from editing attachments, set to **true**.Default: **false**

</td></tr><tr><td>

Should skip preview for unsupported file types\[skipPreviewForUnsupportedFileTypes\]

</td><td>

To directly download attachments of unsupported file types without preview, set to **true**.Default: **false**

</td></tr><tr><td>

Layout mode\[mode\]

</td><td>

The layout to use to render the component. The options include: -   **Full**: Has a search bar and a button for attachment sorting
-   **Compact**: Has smaller text and attachment card with no search bar or attachment sorting button
-   **Custom**: Replaces the component with an empty slot configurable with an icon or button representing the component. The icon or button event is configurable with the `ATTACHMENT_FILE_UPLOAD_EXTERNAL` action to initial attachment upload when the user selects it.

Default: **Full**

</td></tr><tr><td>

Refresh requested\[refreshRequested\]

</td><td>

Timestamp to force a re-fetch of form data.Default: \{\}

</td></tr><tr><td>

Record display value\[recordDisplayValue\]

</td><td>

The record display value to show in the upload overlay.

</td></tr></tbody>
</table><table id="table_w2r_ksq_tfc"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Maximum file size allowed\[maxFileSizeAllowed\]

</td><td>

Defines the maximum size allowed for an attached file, in megabytes \(MB\). Component uses a default maximum file size of 1024MB if left blank.

</td></tr><tr><td>

Allowed file types\[allowedFileTypes\]

</td><td>

Defines the file types allowed to be uploaded. Allows all file types if left blank.

</td></tr><tr><td>

Allow multiple file upload\[isMultiFileUpload\]

</td><td>

To enable users to upload multiple files, set to **true**. If set to **false**, the user can upload one file at a time.Default: **true**

</td></tr><tr><td>

Show preview modal during upload\[previewModalOnUpload\]

</td><td>

To display the preview modal when uploading files, set to **true**. Default: **true**

</td></tr></tbody>
</table>### Manual configuration

To configure the properties manually, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Enables you to create dynamic property values derived from multiple sources, such as state variables \(@state\) in the page, URL variables \(@context\), or payloads from a data resource \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

## Attachments component events

If you have chosen a preset, data handlers for the component events are pre-selected by the controller, and no manual configuration is required. However, you can add additional data handlers to an event or disable the event.

For information about how data handlers work, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

The Events tab shows the events used by the Attachments component, marked with the **Preset** badge.

\[Omitted image "attachments-event-list.png"\] Alt text: Shows the event list for the Attachments,the preset indicator, and the action for adding event handlers

For instruction on how to add and delete event handlers with presets and how to disable an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md) and [Disable preset event mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/disable-preset-event-mappings.md).

### Preset events

-   **__Record attachments__**

    This preset provides data handlers for the **Add notification** event.


### Event descriptions

<table id="table_qwn_hlw_rnb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add notification

</td><td>

Action to add a notification to a page. Notifications inform the user of errors while interacting with the component.

</td></tr><tr><td>

Attachment upload succeeded\[UPLOAD\_SUCCEEDED\]

</td><td>

The user uploads an attachment successfully.

</td></tr><tr><td>

Attachment delete succeeded\[DELETE\_SUCCEEDED\]

</td><td>

The user deletes an attachment successfully.

</td></tr><tr><td>

Attachment downloaded\[ATTACHMENT\_FILE\_DOWNLOADED\]

</td><td>

The user starts an attachment download.

</td></tr><tr><td>

Attachment previewed\[ATTACHMENT\_FILE\_PREVIEWED\]

</td><td>

The user starts to preview an attachment.

</td></tr></tbody>
</table>