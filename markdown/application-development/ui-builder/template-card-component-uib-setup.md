---
title: Template card component setup
description: The Template card component displays a summary of an assist record. Configure a Template card component to highlight relevant information from an assist record, to help the user make a decision, or to provide context.Configure the appearance and features of the Template card component.Select event handlers to configure the actions \(events\) provided with the Template card component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/template-card-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Template card component setup

The Template card component displays a summary of an assist record. Configure a Template card component to highlight relevant information from an assist record, to help the user make a decision, or to provide context.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Template card that differentiates it from other components in the [Customize UI pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "template-card-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Template card component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Template card label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Template card component properties

Configure the appearance and features of the Template card component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_pzk_bkz_znb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tagline

</td><td>

tagline

</td><td>

Object to configure a tagline or title for the card. The object consists of these elements.-   **label** - Text to display as tagline
-   **icon** - Icon that appears before the tagline label

</td></tr><tr><td>

Actions

</td><td>

actions

</td><td>

Array that defines the actions displayed at the top of the card.

</td></tr><tr><td>

Heading

</td><td>

heading

</td><td>

Text description of the card. This text is the most prominent.

</td></tr><tr><td>

Content

</td><td>

content

</td><td>

Array of objects that define how to display label values in the content. Each object consists of these elements.-   **label** - Text to display as label
-   **value** - Text or object to display as a value

</td></tr><tr><td>

Footer content

</td><td>

footerContent

</td><td>

Object that defines how to display label values in the footer.

</td></tr><tr><td>

Selected

</td><td>

selected

</td><td>

Selection state of the card.

</td></tr><tr><td>

Content item min width

</td><td>

contentItemMinWidth

</td><td>

Minimum width of a line of content items. Content items past this point wrap to a new line. The default value is 300.

</td></tr><tr><td>

ARIA properties

</td><td>

configAria

</td><td>

Object to set the ARIA properties for the specified HTML element within the button. The value of each key is an object that contains an ARIA property \(or properties\) and corresponding values. These ARIA properties are set on a specified element.

</td></tr></tbody>
</table>## Template card component events

Select event handlers to configure the actions \(events\) provided with the Template card component.

The Events tab shows the events used by the Template card component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Template card actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Template card assist selected set|Dispatched when a user clicks the card body.|

