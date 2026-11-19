---
title: Breadcrumbs component setup
description: Breadcrumbs provide a browser path to navigate a hierarchy of linked pages with related content. The component provides a digital trail from the user's starting point to the current content, with the ability to navigate to each link.​Configure the display characteristics and overflow behavior of your Breadcrumbs component.Select event handlers to configure the actions \(events\) provided with the Breadcrumbs component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/breadcrumbs-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Breadcrumbs component setup

Breadcrumbs provide a browser path to navigate a hierarchy of linked pages with related content. The component provides a digital trail from the user's starting point to the current content, with the ability to navigate to each link.​

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Breadcrumbs component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "breadcrumbs-content-tree.png"\] Alt text: Content tree showing custom named breadcrumbs component

2.  Select the Breadcrumbs component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Breadcrumbs label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Breadcrumbs component properties

Configure the display characteristics and overflow behavior of your Breadcrumbs component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_txn_1dh_ynb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Items

</td><td>

items

</td><td>

List of breadcrumbs to display, in sorted order, from the first page to the current page.Default: `[{\"label\":\"First Item\",\"href\":\"#\",\"icon\":\"home-outline\",\"hideLabel\":true},{\"label\":\"Breadcrumbs1\",\"href\":\"#\"},{\"label\":\"Breadcrumbs2\",\"href\":\"#\"},{\"label\":\"Breadcrumbs3\"}]`

</td></tr><tr><td>

Delimiter

</td><td>

delimiter

</td><td>

Defines the symbol to use as a separator between breadcrumb items.Choices: **Chevron** or **Arrow**

 Default: **Chevron**

</td></tr><tr><td>

Overflow

</td><td>

overflow

</td><td>

Defines the overflow behavior.Choices:

-   **Collapse**: Collapses items into a dropdown when the breadcrumb is too large for its container and cannot remain on one line.
-   **Truncate-collapse**: First truncates text down to a minimum size, then collapses it into a dropdown.
-   **Wrap**: Causes the breadcrumb to wrap to multiple lines.

 Default: **Collapse**

</td></tr><tr><td>

Overflow menu position

</td><td>

overflowMenuPosition

</td><td>

Defines the position at which to display the overflow menu. When the breadcrumb overflow property is set to **collapse** or **truncate-collapse**, users can set the overflow position.Choices:

-   **Start**: Subpage links adjacent to the home page collapse into the overflow menu.
-   **End**: Subpage links adjacent to the current page collapse into the overflow menu.

Default: **Start**

</td></tr></tbody>
</table>## Breadcrumbs component events

Select event handlers to configure the actions \(events\) provided with the Breadcrumbs component.

The Events tab shows the events used by the Breadcrumbs component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Breadcrumbs actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Breadcrumbs item clicked|Action dispatched when a breadcrumb is selected. Contains the item from the `items` array that the user selected.|

