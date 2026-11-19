---
title: Pagination Control component setup
description: Use the Pagination Control component to divide large sets of content into consolidated pages. Users can navigate the pages using the navigation tool at the bottom of the page.Configure the appearance and number of pages for the Pagination Control component.Select event handlers to configure the actions \(events\) provided with the Pagination Control component.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/pagination-control-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Pagination Control component setup

Use the Pagination Control component to divide large sets of content into consolidated pages. Users can navigate the pages using the navigation tool at the bottom of the page.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

This component contains preset configuration values that are intended for use with the Record List component bundle only. Some preset values for Pagination Control won’t function as expected if used with the standalone component. When using this component outside of the Record List bundle, configure it manually.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Pagination Control that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md).

    \[Omitted image "pagination-control-content-tree.png"\] Alt text: Content tree with the Pagination Control component.

2.  Select the Pagination Control component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Pagination Control label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.

3.  If using Pagination Control as a standalone component \(not in a bundle\), select **None** in the Config panel to remove preset values.

    \[Omitted image "pagination-control-preset-panel.png"\] Alt text: Shows the preset panel for the pagination control component


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Pagination Control component properties

Configure the appearance and number of pages for the Pagination Control component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Page sizes|pageSizes|Sets the choices for the page size list. Default is \[10,20,50,100\].|
|Selected page index|selectedPage|Sets the initial page index to load.|
|Page size|selectedPageSize|Sets the number of records shown on the page. The value must be one of the values set in the page sizes field.|
|Total records|total|Total number of records.|
|Visible pages|visiblePages|Number of pages that can be directly selected. Max is 5.|
|Hide first page button|hideGoToFirst|Hides the go to first page button.|
|Hide last page button|hideGoToLast|Hides the go to last page button.|
|Hide next page button|hideGoToNext|Hides the next page button.|
|Hide previous page button|hideGoToPrevious|Hides the previous page button.|
|Hide page numbers|hidePageNumbers|Hides the visible pages numbers.|
|Hide page size|hidePageSizeControl|Hides the page size choice control and page size number.|
|Hide range|hideRange|Hides the text describing the current range of total records.|
|Pages override|pages0verride|Overrides the number set for visible pages.|
|Page size label|pageSizeLabel|Text describing the page size. Default is Records per page.|
|Range label|rangeLabel|Text describing the current range of total records. Default is Showing.|

## Pagination Control component events

Select event handlers to configure the actions \(events\) provided with the Pagination Control component.

The Events tab shows the events used by the Pagination Control component. To view the available events, select **+ Add event mapping**. Select the event in the list to add one or more event handlers.

### Event handlers

Event handlers work with data resources to link the Pagination Control events to the data you want to display to your users. Select the event in the list to add one or more event handlers.

For instructions on adding event handlers to an event, see [Configure an event handler](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/event-handler.md).

### Event descriptions

|Event|Description|
|-----|-----------|
|Pagination control selected page set|User selects a page number on the selected page index.|
|Pagination control selected page size set|User selects the page size control.|

