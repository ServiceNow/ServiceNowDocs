---
title: Workspace Global Search Tab component setup
description: The Workspace Global Search Tab component displays global search results.Configure the display of the Workspace Global Search Tab results.Select event handlers to configure the actions \(events\) provided with the Workspace Global Search Tab component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/global-search-tab-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Workspace Global Search Tab component setup

The Workspace Global Search Tab component displays global search results.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Workspace Global Search Tab that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "global-search-tab-config-content-tree.png"\] Alt text: Workspace global search tab component in the content tree

2.  Select the Workspace Global Search Tab component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Workspace Global Search Tab label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Workspace Global Search Tab component properties

Configure the display of the Workspace Global Search Tab results.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Search term|term|Searched term.|
|Global search view config|globalSearchViewConfigId|Reference to a record in the workspace global search configuration \[sys\_aw\_global\_search\_config\] table.|
|Global search data config|globalSearchDataConfigId|Reference to a record in the search application \[sys\_search\_context\_config\] table.|
|Hide search results count|hideSearchResultsCount|Select to hide the total results count. Defaults to false.|

## Workspace Global Search Tab component events

Select event handlers to configure the actions \(events\) provided with the Workspace Global Search Tab component.

The Events tab shows the events used by the Workspace Global Search Tab component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Workspace Global Search Tab actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Record clicked|Dispatched when a user clicks a search result record.|
|Search succeeded|Dispatched when the search is completed.|

