---
title: Custom modal setup
description: A modal displays a variety of information in a custom overlay window. For example, you can require the user to complete an action or provide information to return to the main application.Using the modal template for reference, configure the properties that control the behavior and appearance of the Custom modal.Select event handlers to configure the actions \(events\) provided with the Custom modal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/custom-modal-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Custom modal setup

A modal displays a variety of information in a custom overlay window. For example, you can require the user to complete an action or provide information to return to the main application.

## Before you begin

This task assumes you have placed a component on the page and are ready to select and configure a modal for that component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  In the UI Builder content pane, select the component from which the modal will open.

2.  Add the modal to the component.

    For instructions, see [Add modal to component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/modals-uib.md).

3.  Select the Custom modal type from the panel that appears.

    \[Omitted image "select-custom-modal.png"\] Alt text: Modal selection panel with the custom modal selected

    The template for the Custom modal appears on the canvas.

    \[Omitted image "custom-modal-template.png"\] Alt text: Shows the template that appears when configuring the custom modal


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Custom modal properties

Using the modal template for reference, configure the properties that control the behavior and appearance of the Custom modal.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_hkm_nrq_pvb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Modal size\[size\]

</td><td>

Size of the modal. The options are:-   Small
-   Medium \(default\)
-   Large
-   Fullscreen

</td></tr><tr><td>

Hide Padding\[hidePadding\]

</td><td>

When set to true, removes the default padding inside the modal.Default: **false**

</td></tr><tr><td>

Hide Close Button\[disableClose\]

</td><td>

When set to **true**, no close button displays in the modal, and closing the modal via the keyboard is disabled. If you enable this property, you must replace the close functionality elsewhere within the modal. Some valid use cases for setting this property would be a Session Timeout dialog or a Terms &amp; Conditions type modal where an explicit action is required to proceed.

</td></tr><tr><td>

Defer modal content loading\[defer\]

</td><td>

When set to false, connects the modal content when the page loads.Default: **true**

</td></tr><tr><td>

Aria labelledby\[aria-labelledby\]

</td><td>

Aria element that represents the modal label.

</td></tr></tbody>
</table>## Custom modal events

Select event handlers to configure the actions \(events\) provided with the Custom modal.

The Events tab shows the events used by the modal. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the modal actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_jvp_jsq_pvb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Modal closed

</td><td>

The user closes the modal.The payload contains `modalId`, the ID of the modal being closed.

</td></tr><tr><td>

Modal opened

</td><td>

The user opens the modal.The payload contains `modalId`, the ID of the modal being opened.

</td></tr></tbody>
</table>