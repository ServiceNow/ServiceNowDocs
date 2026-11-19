---
title: Document display component setup
description: The Document display component displays either HTML content or PDF attachments.Configure the type, location, and content of the document to display. Set the document's appearance and whether it's editable.Select event handlers to configure the actions \(events\) provided with the Document display component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/document-display-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Document display component setup

The Document display component displays either HTML content or PDF attachments.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Document display that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "document-display-content-tree.png"\] Alt text: Content tree showing a document display component.

2.  Select the Document display component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Document display label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Document display component properties

Configure the type, location, and content of the document to display. Set the document's appearance and whether it's editable.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

### Properties

<table id="table_dfb_trb_zrb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document type\[documentType\]

</td><td>

The type of document to be viewed.Choices:

-   **Attachment record**
-   **HTML**

 The other properties to configure vary, depending on the selection you make here.

</td></tr></tbody>
</table>### HTML document properties

<table id="table_b12_wsb_zrb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit HTML content \[htmlContent\]

</td><td>

Opens an editor where you write the HTML content.

</td></tr><tr><td>

Enable editing\[enableEditing\]

</td><td>

When true, runtime users can edit the HTML. The tab for the document display includes an HTML editor.

</td></tr></tbody>
</table>### Attachment record properties

<table id="table_r4c_nvb_zrb"><thead><tr><th>

Label \[property\]

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attachment content type \[attachmentType\]

</td><td>

 

</td><td>

The type of attachment to be viewed. Choices:

-   **PDF**
-   **Image**

</td></tr><tr><td>

Attachment sys\_id\[attachmentId\]

</td><td>

attachmentId

</td><td>

The `sys_id` of a document to be viewed. Instead of specifying the `sys_id`, you can begin typing the filename. The system gives you a list of matching files.

</td></tr><tr><td>

Target attachment sys\_id\[targetAttachmentId\]

</td><td>

targetAttachmentId

</td><td>

The `sys_id` of a new target document. If document display is opened in compare mode, this will be used to combine the source and target document into one, showing the changed text in red. This can be used to identify changes between two versions of the same document.

</td></tr><tr><td>

Hide toolbar \[hideToolbar\]

</td><td>

hideToolbar

</td><td>

In runtime, the user can have a toolbar with search, zoom, rotation, and other functions. When **Hide toolbar** is enabled, users don't have access to any of the toolbar features. Default: false

</td></tr><tr><td>

Hide search\[hideSearch\]

</td><td>

 

</td><td>

When true, hides the search function in the toolbar. PDF only.Requires **Hide toolbar** to be false and the attachment content type to be **PDF**.

 Default: false

</td></tr><tr><td>

Hide navigation\[hideNavigation\]

</td><td>

 

</td><td>

When true, hides the page navigator in the toolbar. PDF only.Requires **Hide toolbar** to be false and the attachment content type to be **PDF**.

 Default: false

</td></tr><tr><td>

Hide download\[hideDownload\]

</td><td>

 

</td><td>

When true, hides the download button in the toolbar.Requires **Hide toolbar** to be false.

 Default: false

</td></tr><tr><td>

Hide zoom\[hideZoom\]

</td><td>

 

</td><td>

When true, hides the zoom in and zoom out buttons in the toolbar. PDF only.Requires **Hide toolbar** to be false and the attachment content type to be **PDF**.

 Default: false

</td></tr><tr><td>

Hide rotation\[hideRotation\]

</td><td>

 

</td><td>

When true, hides the clockwise and counter-clockwise rotation buttons in the toolbar. PDF only.Requires **Hide toolbar** to be false and the attachment content type to be **PDF**.

 Default: false

</td></tr><tr><td>

Hide delete\[hideDelete\]

</td><td>

 

</td><td>

When true, hides the delete button on the toolbar.Requires **Hide toolbar** to be false.

 Default: false

</td></tr><tr><td>

Hide close\[hideClose\]

</td><td>

 

</td><td>

When true, hides the close button on the toolbar.Requires **Hide toolbar** to be false.

 Default: false

</td></tr></tbody>
</table>## Document display component events

Select event handlers to configure the actions \(events\) provided with the Document display component.

The Events tab shows the events used by the Document display component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Document display actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_zx2_czb_zrb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Close button clicked

</td><td>

Dispatched when user clicks the close button or the delete button. This event doesn't have a payload.

</td></tr><tr><td>

Delete confirmation submitted

</td><td>

Dispatched when the user confirms deleting the document.Payload includes `sysId`: The `sys_id` of the deleted record.

</td></tr><tr><td>

HTML updated

</td><td>

Dispatched when the user edits HTML.Payload includes `value`: The updated HTML value

</td></tr></tbody>
</table>