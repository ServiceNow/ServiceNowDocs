---
title: Card Base Header component setup
description: The Card Base Header subcomponent provides multi-line headings and captions, a tagline for categories and identifiers, and the option to include multiple dropdowns and action menus.Configure the tagline, heading, caption, dropdowns, and actions of the Card Base Header.Select event handlers to configure the actions \(events\) provided with the Card Base Header component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/card-header-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Card Base Header component setup

The Card Base Header subcomponent provides multi-line headings and captions, a tagline for categories and identifiers, and the option to include multiple dropdowns and action menus.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Card Base Header that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "card-header-content-tree.png"\] Alt text: Card Base Header component in the content tree, as a subcomponent of a Card Base Container.

2.  Add a graphic component to the `identifier` slot and a Badge, Highlighted Value, or string component to the `metadata` slot.

3.  Select the Card Base Header component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Card Base Header label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Card Base Header component properties

Configure the tagline, heading, caption, dropdowns, and actions of the Card Base Header.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_lzz_1pd_2sb"><thead><tr><th>

Label \[property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tagline\[tagline\]

</td><td>

An object with properties to configure a tagline for the card. Default key values, if any, are shown:-   `label`: Text contents of the tagline
-   `icon`: Icon that appears before the tagline's label
-   `variant = 'tertiary'`: Color of the icon and label

 Default value: \{\}

</td></tr><tr><td>

Heading\[heading\]

</td><td>

An object with properties to configure a heading for the card. Default key values, if any, are shown:-   `label`: Text contents of the heading
-   `lines = 1`: Number of lines the heading extends to before truncating
-   `level = 3`: HTML heading element number used to render the heading
-   `size = 'sm'`: Size of the heading
-   `variant = 'primary'`: Visual styling for the heading

</td></tr><tr><td>

Caption\[caption\]

</td><td>

An object with properties to configure an optional caption for the card. Default key values, if any, are shown:-   `label`: Text content of the caption
-   `lines = 1`: Number of lines the caption extends to before truncating
-   `size = 'sm'`: Size of the caption

 Default value: \{\}

</td></tr><tr><td>

Dropdowns\[dropdowns\]

</td><td>

An array of objects that define one or more action dropdowns. Displayed before `actions` in the card header. Default key values, if any, are shown:-   `id`: \(Required\) An ID for the dropdown used to correctly update `aria-expanded`.
-   `label`: \(Required\) Description of the dropdown used as the tooltip content and `aria-label` of the dropdown.
-   `items`: \(Required\) Array of objects describing each item in the dropdown.
-   `disabled`: When **true**, disables the dropdown trigger.
-   `icon`: Icon that appears in the dropdown trigger.

</td></tr><tr><td>

Actions\[actions\]

</td><td>

Array of objects that define the iconic buttons displayed after the heading and caption. By default, buttons render from right to left \(for LTR languages\). Buttons beyond the first three appear in an overflow dropdown. Configure the label of this overflow dropdown with the `actionsOverflowLabel` property. Default key values, if any, are shown:-   `icon`: \(Required\) Icon for the action
-   `label`: \(Required\) Description of the action used for the tooltip content and `aria-label`
-   `disabled`: When **true**, mutes the button color and disables user click interactions.
-   `clickActionType = "NOW_CARD_HEADER#ACTION_CLICKED"`: Overrides the default action type dispatched when the user selects the action.

 Default value: \[ \]

</td></tr><tr><td>

Actions overflow dropdown label\[actionsOverflowLabel\]

</td><td>

Label displayed in tooltip on dropdown menu with overflow actions. For more information, see Actions.Type: string

</td></tr></tbody>
</table>### Configuration for a card base header

The following card base header includes a tagline, heading, caption, and dropdowns.

-   Tagline: `{"label":"Article","icon":"document-outline"}`
-   Heading: `{"label":"Configuring wireless security","size":"md"}`
-   Caption: `{"label":"4000 Series Router"}`
-   Dropdowns: `[{"id":"actions","label":"Actions","icon":"ellipsis-v-outline","items":[{"id":"open","label":"Open"}]}]`

This configuration, along with an Icon in the `identifier` slot and a Highlighted Value in the `metadata` slot, produces the following card heading:

\[Omitted image "card-header-runtime-example.png"\] Alt text: A card header in runtime.

## Card Base Header component events

Select event handlers to configure the actions \(events\) provided with the Card Base Header component.

The Events tab shows the events used by the Card Base Header component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Card Base Header actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|Card header action clicked|Dispatched when the user clicks an action button or selects an action from the action dropdown. Payload includes a reference to the clicked action's configuration and the dropdown ID, if specified. You can override the action type by setting `action.clickActionType`.|

