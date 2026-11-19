---
title: Search Input component setup
description: The Search Input component gives users the ability to search your portal or workspace.Configure the search settings for the Search Input component.Select event handlers to configure the actions \(events\) provided with the Search Input component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/search-input-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Search Input component setup

The Search Input component gives users the ability to search your portal or workspace.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Search Input that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "search-input-config-content-tree.png"\] Alt text: Component with label displayed in the content tree

2.  Select the search input component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Search Input label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Search Input component properties

Configure the search settings for the Search Input component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Search term|searchTerm|Text that displays in the Search Input before a user enters their own search term. A user has to delete this text before entering their own text.|
|Search context config|searchContextConfigId|Search application configuration to use for this component. Select a record from the Search Application Configuration \[sys\_search\_context\_config\] table. For more information on search application configurations, see [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/defining-search-app-cfgs-ais.md).|
|Placeholder|placeholder|Text that displays in the Search Input before a user enters their own search term. This text disappears when a user starts entering their own text.|
|Disable auto-complete|disableAutocomplete|Option to disable auto-complete.|

## Search Input component events

Select event handlers to configure the actions \(events\) provided with the Search Input component.

The Events tab shows the events used by the Search Input component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Search Input actions to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

|Event|Description|
|-----|-----------|
|SEARCH\_EXECUTED|User searches for a term pressing or clicking on the search icon.|
|NAVIGATION\_EXECUTED|User clicks on a content item in the search suggestions.|

