---
title: Alert modal setup
description: The Alert modal provides information relating to a component action and a button to close the modal. For example, an alert modal can advise a user who has selected a delete action that the action can't be undone.Using the modal template for reference, configure the properties that define the message and control the behavior of the Alert modal.Select event handlers to configure the events provided with the Alert modal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/alert-modal-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Alert modal setup

The Alert modal provides information relating to a component action and a button to close the modal. For example, an alert modal can advise a user who has selected a delete action that the action can't be undone.

## Before you begin

This task assumes you have placed a component on the page and are ready to select and configure a modal for that component.

Role required: admin

## Procedure

1.  In the UI Builder content pane, select the component from which the modal will open.

2.  Add a modal to the component.

    For instructions, see [Add modal to component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/modals-uib.md).

3.  Select the Alert modal type from the panel that appears.

    \[Omitted image "select-alert-modal.png"\] Alt text: Modal selection panel with the Alert modal selected

    The template for the Alert modal appears on the canvas.

    \[Omitted image "alert-modal-template.png"\] Alt text: Shows the template that appears when configuring the Alert modal


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Alert modal properties

Using the modal template for reference, configure the properties that define the message and control the behavior of the Alert modal.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_l2q_wl5_nvb"><thead><tr><th>

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

Button label\[buttonTitle\]

</td><td>

Label describing the action of the button in the modal footer.

</td></tr><tr><td>

Modal size\[size\]

</td><td>

Size of the modal. The options are:-   Small
-   Medium \(default\)
-   Large
-   Fullscreen

</td></tr><tr><td>

Prevent Default Button Action\[preventDefaultAction\]

</td><td>

Prevents the default behavior of the button from closing the modal.Default: **false**

</td></tr><tr><td>

Defer modal content loading\[defer\]

</td><td>

When set to **false**, connects the modal content when the page loads.Default: **true**

</td></tr></tbody>
</table>## Alert modal events

Select event handlers to configure the events provided with the Alert modal.

The Events tab shows the events used by the modal. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the modal actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

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