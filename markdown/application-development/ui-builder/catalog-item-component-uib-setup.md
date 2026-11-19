---
title: Catalog Item component setup
description: A Catalog Item component is an option enabling users to order goods and request services for themselves or for others.Configure the Catalog Item component with these properties.Select event handlers to configure the actions \(events\) provided with the Catalog Item component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/catalog-item-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Catalog Item component setup

A Catalog Item component is an option enabling users to order goods and request services for themselves or for others.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Catalog Item component that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "catalog-item-content-tree.png"\] Alt text: Catalog Item content tree

2.  Select the Catalog Item component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Catalog Item label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Catalog Item component properties

Configure the Catalog Item component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

<table id="table_vvg_m5d_h4b"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sys Id

</td><td>

sysId

</td><td>

Sys ID of the catalog item.

</td></tr><tr><td>

Requested For ID

</td><td>

requestedForId

</td><td>

Sys ID of the user that the catalog item is requested for.

</td></tr><tr><td>

Request For Header

</td><td>

showRequestForHeader

</td><td>

Option to change the position of the Requested For type variable.-   If set to true, the Requested For type variable is displayed at the header.
-   If set to false, the Requested For type variable is displayed along with other variables in the variable editor.

</td></tr><tr><td>

Submit Position

</td><td>

submitPosition

</td><td>

Aligns the request button in the container.

</td></tr></tbody>
</table>## Catalog Item component events

Select event handlers to configure the actions \(events\) provided with the Catalog Item component.

The Events tab shows the events used by the Catalog Item component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Catalog Item actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Request Generated|Dispatched when a request is generated.|

