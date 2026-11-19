---
title: Search Facets component setup
description: Give users a way to narrow down search results by clicking on the metadata value based on the current search results.Narrow down the search by defining the label and filters of your Search Facets component with these properties.Select event handlers to configure the actions \(events\) provided with the Search Facets component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/search-facets-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Search Facets component setup

Give users a way to narrow down search results by clicking on the metadata value based on the current search results.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Search Facets that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "search-facets-content-tree.png"\] Alt text: Image showing Search Facets content tree

2.  Select the Search Facetss component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Search Facets label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Search Facets component properties

Narrow down the search by defining the label and filters of your Search Facets component with these properties.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Facets|facets|Search Facets response received from data broker|
|Label|label|The text in the label|
|Selected options|selectedOptions|The options that are selected|
|Search context config|searchContextConfigId|sys\_id for the search application from sys\_search\_context\_config table|
|Search term|searchTerm|Term that has been searched|

## Search Facets component events

Select event handlers to configure the actions \(events\) provided with the Search Facets component.

The Events tab shows the events used by the Search Facets component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Search Facets actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|SN\_SEARCH\_FACETS\#SELECTIONS\_UPDATED|Dispatched when a user selects any of the facet options|

