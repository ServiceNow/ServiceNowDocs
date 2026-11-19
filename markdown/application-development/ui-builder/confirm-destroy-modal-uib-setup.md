---
title: Confirm and destroy modal setup
description: The Confirm and destroy modal notifies the user of the seriousness of an action, and asks them whether they want to proceed with the action. Usually this action is a direct one, such as deleting or erasing content.Using the modal template for reference, configure the properties that control the behavior and appearance of the Confirm and destroy modal.Select event handlers to configure the actions \(events\) provided with the Confirm and destroy modal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/confirm-destroy-modal-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Confirm and destroy modal setup

The Confirm and destroy modal notifies the user of the seriousness of an action, and asks them whether they want to proceed with the action. Usually this action is a direct one, such as deleting or erasing content.

## Before you begin

This task assumes you have placed a component on the page and are ready to select and configure a modal for that component.

Role required: admin

## Procedure

1.  In the UI Builder content pane, select the component from which the modal will open.

2.  Add the modal to the component.

    For instructions, see [Add modal to component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/modals-uib.md).

3.  Select the Confirm and destroy modal type from the panel that appears.

    \[Omitted image "select-confirm-destroy-modal.png"\] Alt text: Modal selection panel with the Confirm and destroy modal selected

    The template for the Confirm and destroy modal appears on the canvas.

    \[Omitted image "confirm-destroy-modal-template.png"\] Alt text: Shows the template that appears when configuring the Confirm and destroy modal


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Confirm and destroy modal properties

Using the modal template for reference, configure the properties that control the behavior and appearance of the Confirm and destroy modal.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_owz_f2b_4vb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header\[headerLabel\]

</td><td>

The modal title.

</td></tr><tr><td>

Content\[content\]

</td><td>

Message text to display in the modal.

</td></tr><tr><td>

Secondary button label\[secondaryButtonLabel\]

</td><td>

Label for the secondary button in the modal footer.

</td></tr><tr><td>

Primary button label\[primaryButtonLabel\]

</td><td>

Label for the primary button in the modal footer.

</td></tr><tr><td>

Modal size\[size\]

</td><td>

Size of the modal. The options are:-   Small
-   Medium \(default\)
-   Large
-   Fullscreen

</td></tr><tr><td>

Prevent default Primary Button Action\[preventDefaultPrimaryAction\]

</td><td>

Prevents the default behavior of the primary button from closing the modal.

</td></tr><tr><td>

Prevent Default Secondary Button Action\[preventDefaultSecondaryAction\]

</td><td>

Prevents the default behavior of the secondary button from closing the modal.

</td></tr><tr><td>

Defer modal content loading\[defer\]

</td><td>

When set to **false**, connects the modal content when the page loads.Default: **true**

</td></tr></tbody>
</table>## Confirm and destroy modal events

Select event handlers to configure the actions \(events\) provided with the Confirm and destroy modal.

The Events tab shows the events used by the Confirm and destroy component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Confirm and destroy actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_mbc_fgb_4vb"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Confirm button clicked

</td><td>

The user selects the primary button in the modal to confirm the action.

</td></tr><tr><td>

Cancel button clicked

</td><td>

The user selects the secondary button in the modal to cancel the action.

</td></tr><tr><td>

Modal closed

</td><td>

The user closes the modal.The payload contains `modalId`, the ID of the modal being closed.

</td></tr><tr><td>

Modal opened

</td><td>

The user opens the modal.The payload contains `modalId`, the ID of the modal being opened.

</td></tr></tbody>
</table>