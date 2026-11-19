---
title: Search Results component setup
description: The Search Results component enables users to browse through search results that match their search term.Configure the Search Results data and metadata.Select event handlers to configure the actions \(events\) provided with the Search Results component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/search-results-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Search Results component setup

The Search Results component enables users to browse through search results that match their search term.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Search Results that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "search-results-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the Search Results component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Search Results label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Search Results component properties

Configure the Search Results data and metadata.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Is component loading|isLoading|Option to show the loading state of the search results component.|
|Search result metadata|searchResultMetadata|Metadata for the search results component.|
|Genius results|geniusResults|Data source from which to pull search results.|
|Search results|searchResults|Data source from which to pull search results.|
|Search context config|searchContextConfigId|Name of the search context configuration record to reference.|

## Search Results component events

Select event handlers to configure the actions \(events\) provided with the Search Results component.

The Events tab shows the events used by the Search Results component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Search Results actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|PAGINATION\_BUTTON\_CLICKED|User selects to view next or previous page of search results.|
|SEARCH\_EXECUTED|After the component displays results for the correct spelling of search term, the user clicks the **Show results for...** link.|
|DECLARATIVE\_ACTION|User clicks on a declarative action control or search result card.|

