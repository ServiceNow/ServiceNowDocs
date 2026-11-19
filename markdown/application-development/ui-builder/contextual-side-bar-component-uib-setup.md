---
title: Contextual Sidebar component setup
description: The Contextual Sidebar component shows a vertical set of tabs which each render custom UI content.Configure the Contextual Sidebar with these properties.Configure the Contextual Sidebar tabs using the Tab modal with these properties.Select event handlers to configure the actions \(events\) provided with the Contextual Sidebar component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/contextual-side-bar-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Contextual Sidebar component setup

The Contextual Sidebar component shows a vertical set of tabs which each render custom UI content.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Contextual Sidebar that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "contextual-sidebar-content-tree.png"\] Alt text: Contextual Sidebar tree.

2.  Select the Contextual Sidebar component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Contextual Sidebar label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Contextual Sidebar component properties

Configure the Contextual Sidebar with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

**Note:** The Tabs property can't be data-binded or scripted in the same way as other properties.

<table id="table_jbx_pvy_nnb"><thead><tr><th>

Field

</th><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tabs

</td><td>

 

</td><td>

Tabs displayed in the Contextual Sidebar tabs. The top tab is the lowest order tab. When a tab is created, a variant of the tab is created by default and displayed under the tab.Select **Edit content** to configure a tab, then select **Create a tab**.

</td></tr><tr><td>

Collapsible

</td><td>

 

</td><td>

Option to enable a collapsible Contextual Sidebar.

</td></tr></tbody>
</table>## Contextual Sidebar component tab setup

Configure the Contextual Sidebar tabs using the Tab modal with these properties.

|Field|Property|Description|
|-----|--------|-----------|
|Name of tab|Name of tab|Name of the tab.|
|Page template|Page template|Page templates are pre-defined pages that can be customized to fit your needs. You can choose to reference or copy a page template.|
|Icon|Icon|Icon selected for the tab.|
|Application scope|Application scope|Page or tab records are created in this default application scope. To switch scope, use the application scope picker.|
|Path|Path|Unique identifier for your page or tab.|
|Order|Order|Ordering of the tab. To give higher priority to this record, enter a lower number.|
|Domain|Domain|Domain selected for the tab. The variant is created in this domain. To switch domain scope, use the domain scope picker.|

## Contextual Sidebar component events

Select event handlers to configure the actions \(events\) provided with the Contextual Sidebar component.

The Events tab shows the events used by the Contextual Sidebar component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Contextual Sidebar actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Action button clicked|Action emitted when a sidebar icon button is clicked.|
|Viewport route changed|Action emitted when the route has changed.|
|Panel toggled|Action emitted when a Contextual Sidebar panel is toggled on and off.|

