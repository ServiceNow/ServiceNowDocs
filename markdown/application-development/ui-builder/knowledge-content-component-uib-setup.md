---
title: Knowledge Content component setup
description: Use the Knowledge Content component to handle knowledge templates and knowledge blocks.Configure the content and layout of your Knowledge Content component.The Knowledge Content component has no configurable events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/knowledge-content-component-uib-setup.html
release: brazil
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [UIB Setup Information, UI Builder, Builder library, Developing your application, Classic app development, Building applications]
---

# Knowledge Content component setup

Use the Knowledge Content component to handle knowledge templates and knowledge blocks.

## Before you begin

This task assumes you have placed the component on the page and are ready to configure the properties and events. For instructions on accessing and using features in UI Builder, see [Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-components.md).

**Note:** This document describes the latest component functionality. Go to the store to make sure you have the latest version of the component.

Role required: admin or ui\_builder\_admin

## Procedure

1.  Define a label for your Knowledge Content that differentiates it from other components in the content tree.

    A label makes finding the component easier in a large list of components. For instructions on using the content tree, see [Manage UI pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/work-pages.md). For instructions on using the content tree, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-tutorial.md).

    \[Omitted image "knowledge-content-content-tree.png"\] Alt text: Knowledge Content component in content tree.

2.  Select the Knowledge Content component, using one of these methods:

    -   Click anywhere within the component.
    -   Select the Knowledge Content label you created for your component in the content tree.
    The property fields appear in the **Config** tab in the setup panel on the right.


**Parent Topic:**[UIB Setup Information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/uib-setup-information.md)

## Knowledge Content component properties

Configure the content and layout of your Knowledge Content component.

To configure the properties, enter either static or dynamic input. Enter dynamic input by selecting the input type.

-   **Data binding**: Creates dynamic property values from multiple sources. Sources include state variables \(@state\), URL variables \(@context\), or data resource payloads \(@data\). For details, see [Add and configure data resources to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/add-data-resources.md).
-   **Scripting**: Creates a scripted property value. For details on scripted values, see [Create and bind a client state parameter to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder/state-parameters.md).

|Field|Property|Description|
|-----|--------|-----------|
|Article details|articleDetails|Information about the article record, such as the short description and version.|
|Hide article header|hideArticleHeader|Option to hide the article header.|
|Secondary fields|secondaryFields|Secondary fields to include in the article header.|
|Hide category information|hideKbCategoryInfo|Option to hide the category breadcrumb in the article header.|
|Hide number link|hideNumberLink|Option to hide the article number link in the header. This option is automatically selected.|
|Hide author information|hideAuthorInfo|Option to hide author information in the footer.|
|Hide article actions|hideActions|Option to hide article actions in the article header.|
|Hide block information|hideBlocksInformation|Option to hide knowledge block information. This option is applicable only when the Knowledge Blocks \(com.snc.knowledge\_blocks\) plugin is active. This option is automatically selected.|
|Block information|blocksInformation|Knowledge block information. This field is applicable only when the Knowledge Blocks \(com.snc.knowledge\_blocks\) plugin is active.|

## Knowledge Content component events

The Knowledge Content component has no configurable events.

