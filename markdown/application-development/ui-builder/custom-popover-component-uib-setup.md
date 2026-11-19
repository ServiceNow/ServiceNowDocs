---
title: Custom popover component setup
description: A Custom popover is a temporary panel that floats over other content to provide contextual help and information when a user selects a triggering element.Configure the contents of your Custom popover component and its orientation relative to the trigger.Select event handlers to configure the events provided with the Custom popover component. Event handlers work with data resources to link the Custom popover actions to the data you want to display to your users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/custom-popover-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Custom popover component setup

A Custom popover is a temporary panel that floats over other content to provide contextual help and information when a user selects a triggering element.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: workspace\_admin or ui\_builder\_admin

## Procedure

1.  Create a Custom popover for a component in UI Builder using the procedures in [Add popover to a UI Builder page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-popover.md).

2.  Define a label for your Custom popover that differentiates it from other popovers in the content tree.

    A descriptive label makes finding the correct popover easier when there are multiple popovers. For instructions on using the content tree, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    \[Omitted image "popover-content-tree.png"\] Alt text: Shows the popover in the content tree

3.  Select the popover you created by clicking its label in the content tree.

    The configuration options appear in the panel on the right.

    \[Omitted image "popover-config.png"\] Alt text: Shows the available properties for the custom popover component in the Config panel


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Custom popover component properties

Configure the contents of your Custom popover component and its orientation relative to the trigger.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Links the property to data from another component by using data resources. For details, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_ixr_fz4_qxb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Positioning to trigger\[positioningToTrigger\]

</td><td>

Sets the popover position relative to the trigger.Possible positions are:

-   Auto
-   Top
-   Right
-   Bottom
-   Left

**Note:** The Auto selection places the popover in the best position relative to the trigger depending on the available space and the location of the trigger on the page.

</td></tr><tr><td>

Hide tail\[hideTail\]

</td><td>

Option to hide the visual tail of the popover that points to the trigger.Default: **false**

</td></tr><tr><td>

Disable scroll\[disableScroll\]

</td><td>

Option to disable scrolling in the popover panel when content outgrows the available space. Set this property to **true** if your Popover content already contains a custom scrolling container for handling overflowed content.Default: **false**

</td></tr><tr><td>

Aria properties\[configAria\]

</td><td>

Configures the Aria properties for Popover. Available Aria properties are:

-   aria-braillelabel
-   aria-brailleroledescription
-   aria-colindextext
-   aria-description
-   aria-label
-   aria-placeholder
-   aria-roledescription
-   aria-rowindextext
-   aria-valuetext

</td></tr></tbody>
</table>## Custom popover component events

Select event handlers to configure the events provided with the Custom popover component. Event handlers work with data resources to link the Custom popover actions to the data you want to display to your users.

The Events tab shows the events used by the Custom popover component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Custom popover actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

\[Omitted image "popover-events.png"\] Alt text: Shows the available events for the popover component

### Event descriptions

<table id="table_z3k_pgw_c5b"><thead><tr><th>

Event

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Popover content hidden\[NOW\_POPOVER\#CONTENT\_HIDDEN\]

</td><td>

The user closes the popover, and the content disappears.

</td></tr><tr><td>

Popover content visible\[NOW\_POPOVER\#CONTENT\_VISIBLE\]

</td><td>

The user opens the popover, and the content renders.Payload:

-   name: content
-   label: Content
-   fieldType: json
-   typeMetadata: array

</td></tr></tbody>
</table>