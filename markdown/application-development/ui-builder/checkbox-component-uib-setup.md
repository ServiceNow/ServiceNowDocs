---
title: Checkbox component setup
description: The Checkbox component is an input for users to select whether an option is true, false, or indeterminate. This component can be used on its own or in a set of other options.Configure how a user interacts with the Checkbox component with these properties.Select event handlers to configure the actions \(events\) provided with the Checkbox component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/checkbox-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Checkbox component setup

The Checkbox component is an input for users to select whether an option is true, false, or indeterminate. This component can be used on its own or in a set of other options.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Checkbox component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "checkbox-content-tree.png"\] Alt text: Checkbox component in content tree showing custom label

2.  Select the Checkbox component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Checkbox label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Checkbox component properties

Configure how a user interacts with the Checkbox component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_jhv_xz3_znb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

label

</td><td>

Text label to display next to the checkbox

</td></tr><tr><td>

Size

</td><td>

size

</td><td>

Size of the checkbox: Small \("sm"\) or Medium \("md"\)

</td></tr><tr><td>

Field layout configuration

</td><td>

fieldLayout

</td><td>

Determines whether the labels, field, and slotted content are arranged vertically or horizontally. This property also determines the respective proportions of each element in a horizontal container. The field layout has two configuration properties:

-   **layout** \(string\):
    -   **"layout":"horizontal"**: Horizontally aligns the label with the field; the label displays to the left of the field.
    -   **"layout":"vertical"** \(default\): Vertically aligns the label with the field; the label displays above the field.
-   **columns** \(array\): If the layout is horizontal, the component uses the **columns** array to set the grid template column width for the containers.

</td></tr><tr><td>

Checked

</td><td>

checked

</td><td>

User selects from **true**, **false**, or **Indeterminate**. The **Indeterminate** value shows a horizontal line in the checkbox. If one or more of the children under a parent option are selected, but not all of them, this shows **Indeterminate**.Default: false

</td></tr><tr><td>

Disabled

</td><td>

disabled

</td><td>

When true, turns off user actions.Default: false

</td></tr><tr><td>

Invalid

</td><td>

invalid

</td><td>

When true, the initial value of the checkbox that you set in **Checked** is treated as invalid. An error displays and the visual style changes accordingly.Default value: false

</td></tr><tr><td>

Read only

</td><td>

readonly

</td><td>

When true, the user cannot select the checkbox. However the checkbox otherwise displays as active.Default: false

</td></tr><tr><td>

Required

</td><td>

required

</td><td>

When true, the user must select the checkbox before they can submit the form.

</td></tr><tr><td>

Identifier

</td><td>

name

</td><td>

Name of the checkbox. Dispatched along with the field value on user interaction.

</td></tr><tr><td>

Aria properties

</td><td>

configAria

</td><td>

Configures ARIA properties in JSON.Default: `{}`

</td></tr></tbody>
</table>## Checkbox component events

Select event handlers to configure the actions \(events\) provided with the Checkbox component.

The Events tab shows the events used by the Checkbox component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Checkbox actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Checkbox checked set|Dispatched when the user interacts with the checkbox and neither **Disabled** nor **Read only** are true. Contains the **Identifier** and the **Checked** property values.|
|Checkbox invalid set|Dispatched when the user changes the value of the **Invalid** property. Contains the new value of the property.|

